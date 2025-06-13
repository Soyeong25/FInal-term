import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        final int MAX = 100; // 일정 최대 개수
        String[] titles = new String[MAX];
        String[] dates = new String[MAX];
        String[] categories = new String[MAX];
        int count = 0;

        Scanner sc = new Scanner(System.in);

        while (true) {
            System.out.println("\n[청주대 일정 관리 프로그램]");
            System.out.println("1. 일정 추가");
            System.out.println("2. 일정 보기");
            System.out.println("3. 일정 삭제");
            System.out.println("0. 종료");
            System.out.print("선택: ");
            int menu = sc.nextInt();
            sc.nextLine(); // 줄바꿈 제거

            if (menu == 1) {
                System.out.print("일정 제목: ");
                titles[count] = sc.nextLine();

                System.out.print("날짜 (예: 2025-06-13): ");
                dates[count] = sc.nextLine();

                System.out.print("카테고리 (수업/시험/과제 등): ");
                categories[count] = sc.nextLine();

                count++;
                System.out.println("✅ 일정이 추가되었습니다.");

            } else if (menu == 2) {
                if (count == 0) {
                    System.out.println("등록된 일정이 없습니다.");
                } else {
                    System.out.println("📅 등록된 일정 목록:");
                    for (int i = 0; i < count; i++) {
                        System.out.println(i + ". [" + categories[i] + "] " + titles[i] + " - " + dates[i]);
                    }
                }

            } else if (menu == 3) {
                if (count == 0) {
                    System.out.println("삭제할 일정이 없습니다.");
                } else {
                    System.out.print("삭제할 일정 번호 입력: ");
                    int index = sc.nextInt();
                    sc.nextLine();

                    if (index >= 0 && index < count) {
                        for (int i = index; i < count - 1; i++) {
                            titles[i] = titles[i + 1];
                            dates[i] = dates[i + 1];
                            categories[i] = categories[i + 1];
                        }
                        count--;
                        System.out.println("✅ 일정이 삭제되었습니다.");
                    } else {
                        System.out.println("⚠️ 유효하지 않은 번호입니다.");
                    }
                }

            } else if (menu == 0) {
                System.out.println("👋 프로그램을 종료합니다.");
                break;

            } else {
                System.out.println("⚠️ 잘못된 선택입니다.");
            }
        }

        sc.close();
    }
}
