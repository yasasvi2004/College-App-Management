import java.io.FileInputStream;
import java.io.FileOutputStream;
import java.io.InputStream;
import java.io.ObjectInputStream;
import java.io.ObjectOutputStream;
import java.io.OutputStream;
import java.util.Scanner;
import java.io.Serializable;
import java.io.BufferedOutputStream;
import java.io.File;
import java.io.FileOutputStream;
import java.io.IOException;
import java.io.StringWriter;
import java.io.BufferedWriter;
class student{
    static int jeerollno;
    static float jeepercentile;
   static  int tenthpercentile;
   static  String address,email,schoolname,collegename,reqcou;
   static  String cse="cse",ece="ece";
   static  String cse1="cse_artificial_intelligence",cse2="cse_machine_learning",cse3="cse_graphics_game_design",cse4="cse_computer_networking";
   static  String ece1="ece_robotics",ece2="ece_iot";
   static  int stuphonenumber;static int parphonenumber;
    static String stuname;
    student(int jeerollno,float jeepercentile,int tenthpercentile,String address,int stuphonenumber,int parphonenumber,String email,String schoolname,String collegename,String stuname){
        this.jeerollno=jeerollno;
        this.jeepercentile=jeepercentile;
        this.tenthpercentile=tenthpercentile;
        this.address=address;
        this.stuphonenumber=stuphonenumber;
        this.parphonenumber=parphonenumber;
        this.email=email;
        this.collegename=collegename;
        this.schoolname=schoolname;
        this.stuname=stuname;
    }
   int eligible(String reqcou){
        this.reqcou=reqcou;
        if(reqcou.equals(cse)){
            if(jeepercentile>=90){
                return 1;
            }
            else{
                return 0;
            }
        }
        else if(reqcou.equals(ece)){
            if(jeepercentile>=88){
                return 1;
            }
            else{
                return 0;
            }
        }
        return 0;
    }
}
class student1 extends student{
    static String sub_course;
   static  String course;
   static String cse1="cse_artificial_intelligence",cse2="cse_machine_learning",cse3="cse_graphics_game_design",cse4="cse_computer_networking";
    static String ece1="ece_robotics",ece2="ece_iot";
    static String eligibility,eligibility_sub;
    static float jeepercentile1;
    student1(int jeerollno,float jeepercentile,int tenthpercentile,String address,int stuphonenumber,int parphonenumber,String email,String schoolname,String collegename,String course,String sub_course,String stuname){
        super(jeerollno,jeepercentile,tenthpercentile,address,stuphonenumber,parphonenumber,email,schoolname,collegename,stuname);
        this.course=course;
        this.sub_course=sub_course;
        jeepercentile1=jeepercentile;
    }
   // int subc=super.eligible(course);
   static void eligibility_checking(){
    if(course.equals("cse")){
        if(jeepercentile1>=90){
            if(sub_course.equals(cse1)){
                if(jeepercentile1>=97){
                    eligibility_sub="eligible";
                    eligibility="eligible";
                }
                else{
                    eligibility_sub="not eligible";
                    eligibility="eligible";
                }
            }
            else if(sub_course.equals(cse2)){
                if(jeepercentile1>=96){
                    eligibility_sub="eligible";
                    eligibility="eligible";
                }
                else{
                    eligibility_sub="not eligible";
                    eligibility="eligible";
                }
            }
            else if(sub_course.equals(cse3)){
                if(jeepercentile1>=95){
                    eligibility_sub="eligible";
                    eligibility="eligible";
                }
                else{
                    eligibility_sub="not eligible";
                    eligibility="eligible";
                }
            }
            else if(sub_course.equals(cse4)){
                if(jeepercentile1>=94){
                    eligibility_sub="eligible";
                    eligibility="eligible";
                }
                else{
                    eligibility_sub="not eligible";
                    eligibility="eligible";
                }
            }
        }
        else{
            eligibility="not eligible";
            eligibility_sub="not eligible";
        }
        }
        else{
            if(jeepercentile1>=88){
                if(sub_course.equals(ece1)){
                if(jeepercentile1>=94){
                    eligibility_sub="eligible";
                    eligibility="eligible";
                }
                else{
                    eligibility_sub="not eligible";
                    eligibility="eligible";
                }
            }
            else if(sub_course.equals(ece2)){
                if(jeepercentile1>=93){
                    eligibility_sub="eligible";
                    eligibility="eligible";
                }
                else{
                    eligibility_sub="not eligible";
                    eligibility="eligible";
                }
            }
            }
            else{
                eligibility="not eligible";
                eligibility_sub="not eligible";
            }
        }
    }
    }

class student2 extends student{
    static float jeepercentile1;
   static  String sub_course;
   static  String course;
    String cse1="cse_artificial_intelligence",cse2="cse_machine_learning",cse3="cse_graphics_game_design",cse4="cse_computer_networking";
    String ece1="ece_robotics",ece2="ece_iot";
    static String eligibility,eligibility_sub;
    student2(int jeerollno,float jeepercentile,int tenthpercentile,String address,int stuphonenumber,int parphonenumber,String email,String schoolname,String collegename,String course,String sub_course,String stuname){
        super(jeerollno,jeepercentile,tenthpercentile,address,stuphonenumber,parphonenumber,email,schoolname,collegename,stuname);
        this.course=course;
        this.sub_course=sub_course;
        jeepercentile1=jeepercentile;
    }
  static  void checking_hand(){
    if(jeepercentile1>=10){
        eligibility_sub="eligible";
        eligibility="eligible";
    }
    else{
        eligibility_sub="eligible";
        eligibility="eligible";
    } 
    }
}
abstract class staff{
     int employeid;
     String name;
     int salary;
     String place;
     String category1;
     String s1="nonteaching_staff";  
     String s2="teaching_staff";  
     String s3="worker";
   public  staff(int employeid,String place,String name,String category){
        this.employeid=employeid;
        this.salary=salary;
        this.place=place;
        this.name=name;
        category1=category;
    }
    abstract int Salarycal();
    void set_sal(){
        if(category1.equals(s1)){
        salary=100000;
    }
         else if(category1.equals(s2)){
        salary=200000;
    }
    else if(category1.equals(s3)){
        salary=50000;
    }
    }
    public int getsalary(){
        return salary;
    }
    public void displaysalary(){
        System.out.println(salary);
    }
    public String tostring(){
        return "name of the employee:"+name +" employee id: "+employeid+" he is from:"+place;
    }
}
class nonteaching_staff extends staff{
    int working_hours;
    int workingexp;
    public nonteaching_staff(int employeid,String place,String name,int working_hours,String category,int working_experience){
        super(employeid,place,name,category);
        this.working_hours=working_hours;
        this.workingexp=working_experience;
    }
    @Override public int Salarycal(){
        set_sal();
        int tempsal=getsalary();
        int totalsal=tempsal*workingexp*(working_hours/2);
        return totalsal;
        
    }
    public void display(){
        System.out.println(tostring() + "working experience: "+workingexp+"  working hours:"+working_hours);
    }
}
class teaching_staff extends staff{
    int working_hours;
    int workingexp;
    public teaching_staff(int employeid,String place,String name,int working_hours,String category,int working_experience){
        super(employeid,place,name,category);
        this.working_hours=working_hours;
        this.workingexp=working_experience;
    }
    @Override public int Salarycal(){
        set_sal();
        int tempsal=getsalary();
        int totalsal=tempsal*workingexp*(working_hours/2);
        return totalsal;
        
    }
    public void display(){
        System.out.println(tostring() + "working experience: "+workingexp+"  working hours:"+working_hours);
    }
}
class worker extends staff{
    int working_hours;
    int workingexp;
    public worker(int employeid,String place,String name,int working_hours,String category,int working_experience){
        super(employeid,place,name,category);
        this.working_hours=working_hours;
        this.workingexp=working_experience;
    }
    @Override public int Salarycal(){
        set_sal();
        int tempsal=getsalary();
        int totalsal=tempsal*workingexp*(working_hours/2);
        return totalsal;
        
    }
    public void display(){
        System.out.println(tostring() + "working experience: "+workingexp+"  working hours:"+working_hours);
    }
}
public class Main{
     public static void teacstoreObject(teaching_staff ts){        
        try(FileOutputStream fos = new FileOutputStream("teastaff.txt");
                BufferedOutputStream bos = new BufferedOutputStream(fos)) {
                    String data="\n";
                    String data1="Name of staff:"+ts.name;
                    String data2="    Place    :"+ts.place;
                    String data3="Employe ID   :"+ts.employeid;
                    String data4="Working hours:"+ts.working_hours;
                    String data5="workingExperi:"+ts.workingexp;
                    String data6="secret salary:"+ts.Salarycal();
            byte[] bytes1 = data1.getBytes();
            byte[] bytes=data.getBytes();
            byte[] bytes2 = data2.getBytes();
            byte[] bytes3 = data3.getBytes();
            byte[] bytes4 = data4.getBytes();
            byte[] bytes5 = data5.getBytes();
            byte[] bytes6 = data6.getBytes();
            bos.write(bytes1);
            bos.write(bytes);
            bos.write(bytes2);
            bos.write(bytes);
            bos.write(bytes3);
            bos.write(bytes);
            bos.write(bytes4);
            bos.write(bytes);
            bos.write(bytes5);
            bos.write(bytes);
            bos.write(bytes6);
            bos.write(bytes);
            bos.flush();
            bos.close();
            fos.close();
            System.out.print("Data written to file successfully.");
        } catch (IOException e) {
            e.printStackTrace();
        }        
    }
    public static void nonteastoreObject(nonteaching_staff nts){        
       try(FileOutputStream fos = new FileOutputStream("nonteachingstaff.txt");
                BufferedOutputStream bos = new BufferedOutputStream(fos)) {
                    String data="\n";
                    String data1="Name of staff:"+nts.name;
                    String data2="    Place    :"+nts.place;
                    String data3="Employe ID   :"+nts.employeid;
                    String data4="Working hours:"+nts.working_hours;
                    String data5="workingExperi:"+nts.workingexp;
                    String data6="secret salary:"+nts.Salarycal();
            byte[] bytes1 = data1.getBytes();
            byte[] bytes=data.getBytes();
            byte[] bytes2 = data2.getBytes();
            byte[] bytes3 = data3.getBytes();
            byte[] bytes4 = data4.getBytes();
            byte[] bytes5 = data5.getBytes();
            byte[] bytes6 = data6.getBytes();
            bos.write(bytes1);
            bos.write(bytes);
            bos.write(bytes2);
            bos.write(bytes);
            bos.write(bytes3);
            bos.write(bytes);
            bos.write(bytes4);
            bos.write(bytes);
            bos.write(bytes5);
            bos.write(bytes);
            bos.write(bytes6);
            bos.write(bytes);
            bos.flush();
            bos.close();
            fos.close();
            System.out.print("Data written to file successfully.");
        } catch (IOException e) {
            e.printStackTrace();
        }        
    }
     public static void worstoreObject(worker wor){        
       try(FileOutputStream fos = new FileOutputStream("worker.txt");
                BufferedOutputStream bos = new BufferedOutputStream(fos)) {
                    String data="\n";
                    String data1="Name of staff:"+wor.name;
                    String data2="    Place    :"+wor.place;
                    String data3="Employe ID   :"+wor.employeid;
                    String data4="Working hours:"+wor.working_hours;
                    String data5="workingExperi:"+wor.workingexp;
                    String data6="secret salary:"+wor.Salarycal();
            byte[] bytes1 = data1.getBytes();
            byte[] bytes=data.getBytes();
            byte[] bytes2 = data2.getBytes();
            byte[] bytes3 = data3.getBytes();
            byte[] bytes4 = data4.getBytes();
            byte[] bytes5 = data5.getBytes();
            byte[] bytes6 = data6.getBytes();
            bos.write(bytes1);
            bos.write(bytes);
            bos.write(bytes2);
            bos.write(bytes);
            bos.write(bytes3);
            bos.write(bytes);
            bos.write(bytes4);
            bos.write(bytes);
            bos.write(bytes5);
            bos.write(bytes);
            bos.write(bytes6);
            bos.write(bytes);
            bos.flush();
            bos.close();
            fos.close();
            System.out.print("Data written to file successfully.");
        } catch (IOException e) {
            e.printStackTrace();
        }         
    }
    public static void student1obj(student1 stu1obj){
        try(FileOutputStream fos = new FileOutputStream("student.txt");
                BufferedOutputStream bos = new BufferedOutputStream(fos)) {
                    String data="\n";
                    String data1="Name of student               :"+student1.stuname;
                    String data2=" jeerollno                    :"+student1.jeerollno;
                    String data3="jeepercentile                 :"+student1.jeepercentile;
                    String data4="tenth percentile              :"+student1.tenthpercentile;
                    String data5="  address                     :"+student1.address;
                    String data6="stuphonenumber                :"+student1.stuphonenumber;
                    String data7="parent mobilenumber           :"+student1.parphonenumber;
                    String data9="  email                       :"+student1.email;
                   String data10="  school name                 :"+student1.schoolname;
                   String data11="  college name                :"+student1.collegename;
                   String data12="selected course               :"+student1.course;
                   String data13="selected specialization       :"+student1.sub_course;
                   student1.eligibility_checking();
                   String data14="eligibilty for course         :"+student1.eligibility;
                   String data15="eligibility for specialization:"+student1.eligibility_sub;
            byte[] bytes1 = data1.getBytes();
            byte[] bytes=data.getBytes();
            byte[] bytes2 = data2.getBytes();
            byte[] bytes3 = data3.getBytes();
            byte[] bytes4 = data4.getBytes();
            byte[] bytes5 = data5.getBytes();
            byte[] bytes6 = data6.getBytes();
            byte[] bytes7 = data7.getBytes();
            byte[] bytes8 = data9.getBytes();
            byte[] bytes9 = data10.getBytes();
            byte[] bytes10 = data11.getBytes();
            byte[] bytes11 = data12.getBytes();
            byte[] bytes12 = data13.getBytes();
            byte[] bytes13 = data14.getBytes();
            byte[] bytes14 = data15.getBytes();
            bos.write(bytes1);
            bos.write(bytes);
            bos.write(bytes2);
            bos.write(bytes);
            bos.write(bytes3);
            bos.write(bytes);
            bos.write(bytes4);
            bos.write(bytes);
            bos.write(bytes5);
            bos.write(bytes);
            bos.write(bytes6);
            bos.write(bytes);
            bos.write(bytes7);
            bos.write(bytes);
            bos.write(bytes8);
            bos.write(bytes);
            bos.write(bytes9);
            bos.write(bytes);
            bos.write(bytes10);
            bos.write(bytes);
            bos.write(bytes11);
            bos.write(bytes);
            bos.write(bytes12);
            bos.write(bytes);
            bos.write(bytes13);
            bos.write(bytes);
            bos.write(bytes14);
            bos.write(bytes);
            bos.flush();
            bos.close();
            fos.close();
            System.out.print("Data written to file successfully.");
        } catch (IOException e) {
            e.printStackTrace();
        }   
    }
    public static void student2obj(student2 stu1obj){
        try(FileOutputStream fos = new FileOutputStream("handicapped_stu.txt");
                BufferedOutputStream bos = new BufferedOutputStream(fos)) {
                    String data="\n";
                    String data1="Name of student               :"+student2.stuname;
                    String data2=" jeerollno                    :"+student2.jeerollno;
                    String data3="jeepercentile                 :"+student2.jeepercentile;
                    String data4="tenth percentile              :"+student2.tenthpercentile;
                    String data5="  address                     :"+student2.address;
                    String data6="stuphonenumber                :"+student2.stuphonenumber;
                    String data7="parent mobilenumber           :"+student2.parphonenumber;
                    String data9="  email                       :"+student2.email;
                   String data10="  school name                 :"+student2.schoolname;
                   String data11="  college name                :"+student2.collegename;
                   String data12="selected course               :"+student2.course;
                   String data13="selected specialization       :"+student2.sub_course;
                   student2.checking_hand();
                   String data14="eligibilty for course         :"+student2.eligibility;
                   String data15="eligibility for specialization:"+student2.eligibility_sub;
            byte[] bytes1 = data1.getBytes();
            byte[] bytes=data.getBytes();
            byte[] bytes2 = data2.getBytes();
            byte[] bytes3 = data3.getBytes();
            byte[] bytes4 = data4.getBytes();
            byte[] bytes5 = data5.getBytes();
            byte[] bytes6 = data6.getBytes();
            byte[] bytes7 = data7.getBytes();
            byte[] bytes8 = data9.getBytes();
            byte[] bytes9 = data10.getBytes();
            byte[] bytes10 = data11.getBytes();
            byte[] bytes11 = data12.getBytes();
            byte[] bytes12 = data13.getBytes();
            byte[] bytes13 = data14.getBytes();
            byte[] bytes14 = data15.getBytes();
            bos.write(bytes1);
            bos.write(bytes);
            bos.write(bytes2);
            bos.write(bytes);
            bos.write(bytes3);
            bos.write(bytes);
            bos.write(bytes4);
            bos.write(bytes);
            bos.write(bytes5);
            bos.write(bytes);
            bos.write(bytes6);
            bos.write(bytes);
            bos.write(bytes7);
            bos.write(bytes);
            bos.write(bytes8);
            bos.write(bytes);
            bos.write(bytes9);
            bos.write(bytes);
            bos.write(bytes10);
            bos.write(bytes);
            bos.write(bytes11);
            bos.write(bytes);
            bos.write(bytes12);
            bos.write(bytes);
            bos.write(bytes13);
            bos.write(bytes);
            bos.write(bytes14);
            bos.write(bytes);
            bos.flush();
            bos.close();
            fos.close();
            System.out.print("Data written to file successfully.");
        } catch (IOException e) {
            e.printStackTrace();
        }   
    }
    public static void main(String[] args){
        Scanner input=new Scanner(System.in);
        for(int i=0;i<10;i++){ 
            System.out.println("enter which category application you want to appear\n1:student\n2:staff\n3:exit ");
        int categoryinteger=input.nextInt();
        switch(categoryinteger){
        case 2:
            System.out.println("please select to which category you belongs to\n1:teaching\n2:nonteachinstaff\n3:working\n");
            int subselection=input.nextInt();
            System.out.println("please enter the employeid,place,name,category,workinghours and working experience");
            System.out.println("enter employee id\n");
            int emid=input.nextInt();
            System.out.println("enter the place of the employee\n");
            String place=input.next();
            System.out.println("enter the name of the person\n");
            String name=input.next();
            System.out.println("enter the category in the following astease---->\n1:teaching_staff\n2:nonteaching_staff\n3:worker");
            String category=input.next();
            System.out.println("enter the working hours of employee\n");
            int workinghours=input.nextInt();
            System.out.println("enter the working experience\n");
            int workingexp=input.nextInt();
             if(subselection==1){
                teaching_staff stf=new teaching_staff(emid,place,name,workinghours,category,workingexp);
                teacstoreObject(stf);
            }
            else if(subselection==2){
                nonteaching_staff nstf=new nonteaching_staff(emid,place,name,workinghours,category,workingexp);
                nonteastoreObject(nstf);
            }
            else if(subselection==3){
                worker wor=new worker(emid,place,name,workinghours,category,workingexp);
                worstoreObject(wor);
            }
            break;
        case 1:
            System.out.println("enter the category of student \n1:physically handicapped\n2:others");
            int sel=input.nextInt();
            System.out.println("enter the name of the student");
            String namestu=input.next();
            System.out.println("enter the jee percentile");
            float jeeper=input.nextInt();
            System.out.println("enter the jee rollno");
            int jeeroll=input.nextInt();
            System.out.println("enter the tenth percentile");
            int tenper=input.nextInt();
            System.out.println("enter the home address");
            String add=input.next();
            System.out.println("enter student phone number");
            int stupho=input.nextInt();
            System.out.println("enter the parents phone number");
            int parpho=input.nextInt();
            System.out.println("enter the email of student");
            String ema=input.next();
            System.out.println("enter the school name");
            String school=input.next();
            System.out.println("enter the college name");
            String clg=input.next();
            System.out.println("enter the course you want to choose");
            String cou=input.next();
            System.out.println("enter the specialization you want to choose\n1:cse_artificial_intelligence\n2:cse_machine_learning\n3:cse_graphics_game_design\n4:cse_computer_networking\nif ece:\n1:ece_iot\n2:ece_robotics");
            String couspe=input.next();
            if(sel==1){
                student2 stu2=new student2(jeeroll,jeeper,tenper,add,stupho,parpho,ema,school,clg,cou,couspe,namestu);
                student2obj(stu2);
            }
            else{
                student1 stu1=new student1(jeeroll,jeeper,tenper,add,stupho,parpho,ema,school,clg,cou,couspe,namestu);
                student1obj(stu1);
            }break;
        default: i=10;
    }
}
}}