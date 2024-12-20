# HotelreservationSystemByHimanshu
class Reservation{
    String name;
    int room_number;
    int date;
    int Amount;

    public Reservation(String name, int room_number, int date,int Amount) {
        this.name = name;
        this.room_number = room_number;
        this.date = date;
        this.Amount=Amount;
    }

    @Override
    public String toString() {
        return "Name = "+name+" Room Number = "+room_number+" Date = "+date+" amount = "+Amount+"\n";
    }
}

class Hotel10{
    ArrayList<Reservation> rs;


    public Hotel10(ArrayList<Reservation> rs) {
        this.rs = rs;
    }

    public void check()
    {
        System.out.println(rs);
    }

}
public class HotelReservation {
    public static void main(String[] args) {
        ArrayList<Reservation> bk = new ArrayList<>();
        Reservation b1 = new Reservation("Himanshu",101,20,2500);
        bk.add(b1);
        Reservation b2 = new Reservation("Harry",102,22,2200);
        bk.add(b2);
        Reservation s1 = new Reservation("James",113,10,2000);
        bk.add(s1);

        Scanner sc = new Scanner(System.in);
            System.out.println("1: New Reservations\n" +
                    "2: Check Reservations\n" +
                    "3: Update Reservations\n" +
                    "4: Delete Reservations\n" +
                    "5: Exit");
        System.out.println("Enter case");
        int num = sc.nextInt();
        switch (num){
            case 1:
                System.out.println("Enter name,room,date and amount");
                String name=sc.next();
                int room=sc.nextInt();
                int date=sc.nextInt();
                int amount=sc.nextInt();
                Reservation b3=new Reservation(name,room,date,amount);
                bk.add(b3);

            case 2:
                System.out.println("list of members");
                Hotel10 obj = new Hotel10(bk);
                obj.check();
                break;
            case 3:
                System.out.println("Enter name,room,date and amount");
                String name2=sc.next();
                int room2=sc.nextInt();
                int date2=sc.nextInt();
                int amount2=sc.nextInt();
                Reservation b4=new Reservation(name2,room2,date2,amount2);
                bk.add(b4);
                break;
            case 4:
                System.out.println("Enter name,room,date and amount");
                String name3=sc.next();
                int room3=sc.nextInt();
                int date3=sc.nextInt();
                int amount3=sc.nextInt();
                Reservation b5=new Reservation(name3,room3,date3,amount3);
                bk.remove(b5);
                break;
            case 5:
                System.out.println("Exiting.....");
            default:
                System.out.println("Wrong Input!");
        }

    }
}
