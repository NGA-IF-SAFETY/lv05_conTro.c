#I)CON TRỎ  

##1.Khái Niệm:  

-Là một loại biến dùng để lưu địa chỉ  

-Mỗi loại địa chỉ sẽ có một kiểu con trỏ tương ứng (phụ thuộc vào loại dữ liệu lưu trữ trong địa chỉ đó)        

*Kiểu con trỏ cho phép:   

   +Truyền tham số kiểu địa chỉ  
   +Biểu diễn các kiểu, cấu trúc dữ liệu động    
   +Lưu trữ dữ liệu trong vùng nhớ heap  
   
##2.Phân loại: 
 -Con trỏ kiểu int dùng để chứa địa chỉ các biến kiểu int. Tương tự cũng có con trỏ kiểu float, kiểu double, char ....

## 3.khai báo :  

 a)Con trỏ có kiểu: Chỉ chứa được những địa chỉ của loại dữ liệu phù hợp với kiểu dữ liệu mà ta đã khai báo cho con trỏ  
 
  cú pháp: kiểu dữ liệu *tên biến con trỏ;   
  
  ví dụ: int *p;    
  
 b)Con trỏ không kiểu:  Có thể chứa bất kỳ một địa chỉ nào     
 
 void *tên biến con trỏ ;     
 
 ví dụ: void *pa;   
 
 c) Kiểu con trỏ phải được định nghĩa trên một kiểu cơ sở đã được định nghĩa trước đó    
 
  cú pháp: typedef <kiểu_cơ_sở> *Tên_kiểu;  
  
  ví dụ: typedef  int  *PINT;   
  
  // PINT là kiểu con trỏ - địa chỉ vùng nhớ kiểu int   
##4. Các Phép Toán Trên Con Trỏ  

a)Phép gán: chỉ nên thực hiện trên các con trỏ có cùng kiểu, khi thực hiện trên con trỏ phải thực hiện phép ép kiểu:  

ví dụ : 
 int n, *pi,*qi;  
 pi=&n;    
 pi=qi;   
  
b) Phép tăng giảm địa chỉ   

ví dụ : int a[100],*qa;   

 qa=&a[50];// q là con trỏ thực trỏ tới phần tử a[50]  

qa+i trỏ tới phần tử a[50+i]   

qa–i trỏ tới phần tử a[10-i]    

c)Phép so sánh: dùng so sánh các con trỏ cùng kiểu   

ví dụ:
int *p,*q;  

p<q;  

#II) TOÁN TỬ "&" 
  
  - Địa chỉ :  +Khi khai báo biến, máy sẽ cấp phát cho biến một khoảng nhớ.   
   
          +Địa chỉ của biến là số thứ tự của byte đầu tiên trong một dãy các byte liên tiếp mà máy dành cho biến 
           (các byte được đánh số từ 0).   
  
 - Máy phân biệt các loại địa chỉ như các biến. Ví dụ như: địa chỉ kiểu int, kiểu float,…    
  
 - Vào thời điểm mà chúng ta khai báo một biến thì nó phải được lưu trữ trong một vị trí cụ thể trong bộ nhớ. Chúng ta không quyết định nơi nào biến đó được đặt, điều đó làm tự động bởi trình biên dịch và hệ điều hành. Nhưng khi hệ điều hành đã gán một địa chỉ cho biến thì chúng ta cần biết biến đó được lưu trữ ở đâu. Điều này được thực hiện bằng cách đặt trước tên biến một dấu và (&).   
 
  Ví dụ: x = &y;   
 
 #III)Toán tử tham chiếu (*)  
 
  - Bằng cách sử dụng con trỏ chúng ta có thể truy xuất trực tiếp đến giá trị được lưu trữ trong biến được trỏ bởi nó bằng cách đặt trước tên biến con trỏ một dấu (*).  
  
  # IV) Con Trỏ Và Mảng  
    -Biến kiểu mảng là địa chỉ tĩnh của một vùng nhớ, được xác định khi khai báo, không thay đổi trong suốt chu kỳ sống   
    
    -Biến con trỏ là địa chỉ động của một vùng nhớ, được xác định qua phép gán địa chỉ khi chương trình thực thi   
    
   1)con trỏ và mảng một chiều:  
   
   -Các phần tử của mảng có thể được xác định thông qua con trỏ. 

   -Ta có tên mảng chính là một hằng địa chỉ trỏ tới địa chỉ phần tử đầu tiên của mảng và

      + a tương đương với &a[0]  

      + a+i tương đương với &a[i]  

      + *(a+i) tương đương với a[i]   
      
  2)Con trỏ và mảng nhiều chiều:
   - Phép toán lấy địa chỉ nói chung không dùng được đối với các thành phần của mảng nhiều chiều 
   (trừ trường hợp mảng hai chiều các số nguyên).  
  
   - Ðể tính toán địa chỉ của thành phần a[i][j] chúng ta sử dụng công thức sau : (float *)a+i

   +a là một hằng con trỏ trỏ đến các dòng của một ma trân hai chiều, vì vậy            

            a trỏ đến dòng thứ nhất

            a+1 trỏ đến dòng thứ hai

            a+2 trỏ đến dòng thứ ba
   
   
      
  
   
     
  
  
  
  
  
  
  
  
  












 
 
   
 
  
  
  
  
 
