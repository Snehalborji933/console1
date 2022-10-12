# console1
multiplication of 4 no.
Q1. Create an application that obtains four int values from the user and displays the product.
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace AWP_A
{
class Program
{
static void Main(string[] args)
{
Console.WriteLine("Enter values");
int a = Convert.ToInt32(Console.ReadLine());
int b = Convert.ToInt32(Console.ReadLine());
int c = Convert.ToInt32(Console.ReadLine());
int d = Convert.ToInt32(Console.ReadLine());
int ans = a * b * c * d;
Console.WriteLine("Answer Is: {0}", ans);
Console.ReadLine();
}
}
}


Q2. Create an application to demonstrate string operations.
Solution C# Code:

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
namespace AWP_A
{
class strOps
{
static void Main(string[] args)
{
string firstname ="Web Programming";
string lastname = "Advanced";
Console.WriteLine("...Clone....");
Console.WriteLine(firstname.Clone());
// Make String Clone
Console.WriteLine("...Compare....");
Console.WriteLine(firstname.CompareTo(lastname));

////Compare two string value and returns 0 for true and 1 for false
Console.WriteLine("...Conatins....");
Console.WriteLine(firstname.Contains("Web"));
// //Check whether specified value exists or not in string
Console.WriteLine("...EndsWith....");
Console.WriteLine(firstname.EndsWith("g")); //Check whether specified value is the last character of string
Console.WriteLine("...Equals....");
Console.WriteLine(firstname.Equals(firstname));
////Compare two string and returns true and false
Console.WriteLine("...GetHashCode....");
Console.WriteLine(firstname.GetHashCode());
////Returns HashCode of String
Console.WriteLine("...GetType....");
Console.WriteLine(firstname.GetType());
////Returns type of string
Console.WriteLine("...GetTypeCode....");
Console.WriteLine(firstname.GetTypeCode());
////Returns type of string
Console.WriteLine("...IndexOf....");
Console.WriteLine(firstname.IndexOf("m"));
//Returns the first index position of specified value the first index position of specified value
Console.WriteLine(firstname.ToLower());
////Covert string into lower case

TYIT – Sem – V - Advanced Web Programming –Paper (III)

Compiled By Swarupa P. Gogate Page 3
Console.WriteLine(firstname.ToUpper());
////Convert string into Upper case
Console.WriteLine(firstname.Insert(12, "Hello"));
////Insert substring into string
// Console.WriteLine(firstname.IsNormalized());
////Check Whether string is in Unicode normalization from C

Console.WriteLine(firstname.LastIndexOf("m"));
////Returns the last index position of specified value
Console.WriteLine(firstname.Length);
////Returns the Length of String
Console.WriteLine(firstname.Remove(5));
////Deletes all the characters from begining to specified index.
Console.WriteLine(firstname.Replace('e','i')); // Replace the character
string[] split = firstname.Split(new char[] { 'e' });
//Split the string based on specified value

Console.WriteLine(split[0]);
Console.WriteLine(split[1]);
Console.WriteLine(split[2]);
Console.WriteLine(firstname.StartsWith("w"));
//Check wheter first character of string is same as specified value
Console.WriteLine(firstname.Substring(2,5));
////Returns substring
Console.WriteLine(firstname.ToCharArray());
////Converts an string into char array.

//Console.WriteLine(firstname.Trim());
string temp = " data ";
Console.WriteLine("Length before Trim {0}", temp.Length);
string op = temp.Trim();
Console.WriteLine("Length after Trim {0}", op.Length);
////It removes starting and ending white spaces from string.
Console.ReadLine();
}
}
}

TYIT – Sem – V - Advanced Web Programming –Paper (III)

Compiled By Swarupa P. Gogate Page 4
Q3. Write an application that receives the following information from a set of students:
Student Id:
Student Name:
Course Name:
Date of Birth:
The application should also display the information of all the students once the data is entered. Implement
this using an Array of Structs.
Solution C# Code:
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
namespace AWP_A
{
class structs
{
struct Student
{
public string studid, name, cname;
public int day, month, year;
}
static void Main(string[] args)
{
//Try the code for n students.
Student[] s = new Student[5];
int i;
for (i = 0; i < 5; i++)
{
Console.Write("Enter Student Id:");
s[i].studid = Console.ReadLine();
Console.Write("Enter Student name : ");
s[i].name = Console.ReadLine();
Console.Write("Enter Course name : ");
s[i].cname = Console.ReadLine();
Console.Write("Enter date of birth\n Enter day(1-31):");
s[i].day = Convert.ToInt32(Console.ReadLine());
Console.Write("Enter month(1-12):");
s[i].month = Convert.ToInt32(Console.ReadLine());
Console.Write("Enter year:");
s[i].year = Convert.ToInt32(Console.ReadLine());
}
Console.WriteLine("\n\nStudent's List\n");
for (i = 0; i < 5; i++)
{
Console.WriteLine("\nStudent ID : " + s[i].studid);
Console.WriteLine("\nStudent name : " + s[i].name);
Console.WriteLine("\nCourse name : " + s[i].cname);
Console.WriteLine("\nDate of birth(dd-mm-yy) : " + s[i].day + "-" + s[i].month +

TYIT – Sem – V - Advanced Web Programming –Paper (III)

Compiled By Swarupa P. Gogate Page 5
"-" + s[i].year);
Console.ReadLine();
}
}
}
}
Q1.Write a console application to perform the different operations using the concept of Delegates.
Solution C# Code:
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
namespace AWP_A
{
//STEP - 01 DECLARING A DELEGATE
delegate int Compute(int n);
//declaring delegate
class delegates
{
static int number = 100;
//STEP - 02 DELEGATE METHOD DECLARATION
public static int add(int n)
{
number = number + n;
return number;
}
public static int mul(int n)
{
number = number * n;
return number;
}
public static int getNumber()
{
return number;
}
static void Main(string[] args)
{
// STEP - 03 DELEGATE INSTATIATION
Compute c1 = new Compute(add);
//instantiating delegate
Compute c2 = new Compute(mul);
// STEP - 04 CALLING A DELEGATE

TYIT – Sem – V - Advanced Web Programming –Paper (III)

Compiled By Swarupa P. Gogate Page 6
c1(20);//calling method using delegate
Console.WriteLine("After c1 delegate, Number is: " + getNumber());
c2(20);
Console.WriteLine("After c2 delegate, Number is: " + getNumber());
Console.ReadKey();
}
}
}
Q2.Write a console application to perform Method Overloading for finding Area of Circle,Traingle and
Rectangle
Solution C# Code:
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
namespace AWP_A
{
public class Demo
{
public static double Area(int radius)
{
//area of circle
return 3.14 * radius * radius;
}
public static int Area(int b, int height)
{
//area of traingle
return b * height / 2;
}
public static double Area(double length, double breadth)
{
//area of rectangle
return length * breadth;
}
}
class methodOverload
{
static void Main(string[] args)
{
Console.WriteLine("area of circle: " + Demo.Area(10));
Console.WriteLine("area of traingle: " + Demo.Area(8,10));
Console.WriteLine("area of rectangle " + Demo.Area(3,7));
Console.ReadKey();
}
}
}

Q1.Create a simple web page with various server controls to demonstrate setting and use of their
properties. (Example : AutoPostBack)
Mathematical Operations
GUI:

using System;
using System.Collections.Generic;
using System.Linq;
using System.Web;
using System.Web.UI;
using System.Web.UI.WebControls;
namespace Web_AWP_A
{
public partial class Calculator : System.Web.UI.Page
{
protected void Page_Load(object sender, EventArgs e)
{
txtno1.Focus();
}

TYIT – Sem – V - Advanced Web Programming –Paper (III)

Compiled By Swarupa P. Gogate Page 8
protected void Button1_Click(object sender, EventArgs e)
{
//Response.Redirect("About.aspx");
}
protected void btnCompute_Click(object sender, EventArgs e)
{
//read the values from textboxes
int a = Convert.ToInt32(txtno1.Text);
int b = Convert.ToInt32(txtno2.Text);
//perform computations
int result = a * b;
//display on the form
lblDisplay.Text = Convert.ToString(result);
}
protected void btnCancel_Click(object sender, EventArgs e)
{
txtno1.Text = "";
txtno2.Text = "";
lblDisplay.Text = "";
txtno1.Focus();
}
}
}

Q2. Demonstrate the use of Calendar control to perform following operations.
a) Display messages in a calendar control b) Display vacation in a calendar control
c) Selected day in a calendar control using style d) Difference between two calendar dates
GUI:

TYIT – Sem – V - Advanced Web Programming –Paper (III)

Compiled By Swarupa P. Gogate Page 9
See the below properties set for the calendar control.
<%@ Page Language="C#" AutoEventWireup="true" CodeBehind="CalendarControl.aspx.cs"
Inherits="Web_AWP_A.CalendarControl" %>
<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">
<head runat="server">
<title></title>
</head>
<body>
<form id="form1" runat="server">
<div>
<asp:Calendar ID="Calendar1" runat="server" BackColor="#FFFFCC" BorderColor="#FFCC66"
BorderWidth="1px" DayNameFormat="Shortest" Font-Names="Verdana" Font-Size="8pt"
ForeColor="#663399" Height="200px" NextPrevFormat="ShortMonth" OnDayRender="Calendar1_DayRender"
OnSelectionChanged="Calendar1_SelectionChanged" ShowGridLines="True" Width="220px">
<DayHeaderStyle BackColor="#FFCC66" Font-Bold="True" Height="1px" />
<NextPrevStyle Font-Size="9pt" ForeColor="#FFFFCC" />
<OtherMonthDayStyle ForeColor="#CC9966" />
<SelectedDayStyle BackColor="#CCCCFF" Font-Bold="True" />
<SelectorStyle BackColor="#FFCC66" />
<TitleStyle BackColor="#990000" Font-Bold="True" Font-Size="9pt" ForeColor="#FFFFCC" />
<TodayDayStyle BackColor="#FFCC66" ForeColor="White" />
</asp:Calendar>
<br />

TYIT – Sem – V - Advanced Web Programming –Paper (III)

Compiled By Swarupa P. Gogate Page 10
<br />
<asp:Button ID="btnResult" runat="server" OnClick="btnResult_Click" Text="Result" />
&nbsp;&nbsp;&nbsp;
<asp:Button ID="btnReset" runat="server" OnClick="btnReset_Click" Text="Reset" />
<br />
<br />
<asp:Label ID="Label1" runat="server" Text="Label"></asp:Label>
<br />
<br />
<asp:Label ID="Label2" runat="server" Text="Label"></asp:Label>
<br />
<br />
<asp:Label ID="Label3" runat="server" Text="Label"></asp:Label>
<br />
<br />
<asp:Label ID="Label4" runat="server" Text="Label"></asp:Label>
<br />
<br />
<asp:Label ID="Label5" runat="server" Text="Label"></asp:Label>
</div>
</form>
</body>
</html>

using System;
using System.Collections.Generic;
using System.Linq;
using System.Web;
using System.Web.UI;
using System.Web.UI.WebControls;
namespace Web_AWP_A
{
public partial class CalendarControl : System.Web.UI.Page
{
protected void Page_Load(object sender, EventArgs e)
{
}
protected void Calendar1_SelectionChanged(object sender, EventArgs e)
{
Label1.Text = "Your Selected Date:" + Calendar1.SelectedDate.Date.ToString();
}
protected void btnResult_Click(object sender, EventArgs e)
{
//Change the caption
Calendar1.Caption = "Happy Home";
Calendar1.FirstDayOfWeek = FirstDayOfWeek.Sunday;
Calendar1.TitleFormat = TitleFormat.MonthYear;
Label2.Text = "Todays Date : " + Calendar1.TodaysDate.ToShortDateString();
Label3.Text = "Ganpati Vacation Start: 9-10-2021";
TimeSpan d = new DateTime(2021, 9, 10) - DateTime.Now;

TYIT – Sem – V - Advanced Web Programming –Paper (III)

Compiled By Swarupa P. Gogate Page 11
Label4.Text = "Days Remaining For Ganpati Vacation:" + d.Days.ToString();
TimeSpan d1 = new DateTime(2021, 12, 31) - DateTime.Now;
Label5.Text = "Days Remaining for New Year:" + d1.Days.ToString();
if (Calendar1.SelectedDate.ToShortDateString() == "9-10-2021")
Label3.Text += "<b>Ganpati Festival Start</b>";
if (Calendar1.SelectedDate.ToShortDateString() == "9-15-2021")
Label3.Text += "<b>Ganpati Festival End</b>";
}
protected void Calendar1_DayRender(object sender, System.Web.UI.WebControls.DayRenderEventArgs e)
{
if (e.Day.Date.Day == 5 && e.Day.Date.Month == 9)
{
e.Cell.BackColor = System.Drawing.Color.Yellow;
Label lbl = new Label();
lbl.Text = "<br>Teachers Day!";

e.Cell.Controls.Add(lbl);
Image g1 = new Image();
g1.ImageUrl = "Tulips.jpg";
g1.Height = 20;
g1.Width = 20;
e.Cell.Controls.Add(g1);
}
if (e.Day.Date.Day == 13 && e.Day.Date.Month == 9)
{
Calendar1.SelectedDate = new DateTime(2021, 9, 10);
Calendar1.SelectedDates.SelectRange(Calendar1.SelectedDate,
Calendar1.SelectedDate.AddDays(10));
Label lbl1 = new Label();
lbl1.Text = "<br>Ganpati!";
e.Cell.Controls.Add(lbl1);
}
}
protected void btnReset_Click(object sender, EventArgs e)
{
Label1.Text = "";
Label2.Text = "";
Label3.Text = "";
Label4.Text = "";
Label5.Text = "";
Calendar1.SelectedDates.Clear();
}
}
}

Q3. Demonstrate the use of Treeview control performs following operations.
a) Treeview control and datalist b) Treeview operations

TYIT – Sem – V - Advanced Web Programming –Paper (III)

Compiled By Swarupa P. Gogate Page 12
Add XML File

Website -> Add -> XML File

<?xml version="1.0" encoding="utf-8" ?>
<studentdetail>
<student>
<sid>1</sid>
<sname>Swarupa</sname>
<sclass>TYIT</sclass>
</student>
<student>
<sid>2</sid>
<sname>Sonali</sname>
<sclass>TYCS</sclass>
</student>
<student>
<sid>3</sid>
<sname>Yashashree</sname>
<sclass>TYIT</sclass>
</student>
<student>
<sid>4</sid>
<sname>Vedshree</sname>
<sclass>TYCS</sclass>
</student>
</studentdetail>

Source Code:
Treeview control navigation:<asp:TreeView ID = "TreeView1" runat = "server" Width = "150px"
ImageSet="Arrows">
<HoverNodeStyle Font-Underline="True" ForeColor="#5555DD" />
<Nodes>
<asp:TreeNode Text = "ASP.NET Practs" Value = "New Node">
<asp:TreeNode Text = "Calendar Control" Value = "RED" NavigateUrl="~/calndrCtrl.aspx"> </asp:TreeNode>
<asp:TreeNode Text = "Constructor Overloading" Value = "GREEN" NavigateUrl="~/clsconstrc.aspx">
</asp:TreeNode>
<asp:TreeNode NavigateUrl="~/singleInh.aspx" Text="Inheritance" Value="BLUE"></asp:TreeNode>
<asp:TreeNode NavigateUrl="~/clsProp.aspx" Text="Class Properties" Value="Class
Properties"></asp:TreeNode>
</asp:TreeNode>
</Nodes>
<NodeStyle Font-Names="Tahoma" Font-Size="10pt" ForeColor="Black" HorizontalPadding="5px"
NodeSpacing="0px" VerticalPadding="0px" />
<ParentNodeStyle Font-Bold="False" />
<SelectedNodeStyle Font-Underline="True" ForeColor="#5555DD" HorizontalPadding="0px"
VerticalPadding="0px" />
</asp:TreeView>
<asp:XmlDataSource ID="XmlDataSource1" runat="server"
DataFile="~/studentDeatils.xml"></asp:XmlDataSource>
<br />
Fetch Datalist Using XML data : </div>

TYIT – Sem – V - Advanced Web Programming –Paper (III)

Compiled By Swarupa P. Gogate Page 13
<asp:DataList ID="DataList1" runat="server">
<ItemTemplate>
<table class = "table" border="1">
<tr>
<td>Roll Num : <%# Eval("sid") %><br />
Name : <%# Eval("sname") %><br />
Class : <%# Eval("sclass")%>
</td>
</tr>
</table>
</ItemTemplate>
</asp:DataList>

using System;
using System.Collections.Generic;
using System.Linq;
using System.Web;
using System.Web.UI;
using System.Web.UI.WebControls;
using System.Data;
namespace WebApp_AWP_D
{

TYIT – Sem – V - Advanced Web Programming –Paper (III)

Compiled By Swarupa P. Gogate Page 14
public partial class TreeView : System.Web.UI.Page
{
protected void Page_Load(object sender, EventArgs e)
{
if (!IsPostBack)
{
BindData();
}
}
protected void BindData()
{
DataSet ds = new DataSet();
ds.ReadXml(Server.MapPath("stdetail.xml"));
if (ds != null && ds.HasChanges())
{
DataList1.DataSource = ds;
DataList1.DataBind();
}
else
{
DataList1.DataBind();
}
}
}
}

Practical 04: Working with Form Controls

Q1. Create a Registration form to demonstrate use of various Validation controls.
Q2. Create Web Form to demonstrate use of Adrotator Control.

Q1. Create a Registration form to demonstrate use of various Validation controls.
GUI:

TYIT – Sem – V - Advanced Web Programming –Paper (III)

Compiled By Swarupa P. Gogate Page 15
Source Code:
<%@ Page Language="C#" AutoEventWireup="true" CodeBehind="ValidationDemo.aspx.cs"
Inherits="WebApp_AWP_D.ValidationDemo" %>
<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">
<head runat="server">
<title></title>
</head>
<body>
<form id="form1" runat="server">
<div style="background-color: #008080; font-family: Calibri; font-size: large">
<asp:Label ID="Label1" runat="server" Text="Name:"></asp:Label>
<asp:TextBox ID="txtName" runat="server" style="margin-left: 26px" Width="286px"></asp:TextBox>
<asp:RequiredFieldValidator ID="RequiredFieldValidator1" runat="server" ControlToValidate="txtName"
ErrorMessage="Field can't be empty!!!"></asp:RequiredFieldValidator>
<br />
<br />
<asp:Label ID="Label2" runat="server" Text="Age:"></asp:Label>
<asp:TextBox ID="txtAge" runat="server" style="margin-left: 42px" Width="269px"></asp:TextBox>
<asp:RangeValidator ID="RangeValidator1" runat="server" ControlToValidate="txtAge"
ErrorMessage="The value is not in the range!!!" MaximumValue="30" MinimumValue="20"
Type="Integer"></asp:RangeValidator>

TYIT – Sem – V - Advanced Web Programming –Paper (III)

Compiled By Swarupa P. Gogate Page 16
<br />
<br />
<asp:Label ID="Label3" runat="server" Text="Email ID:"></asp:Label>
<asp:TextBox ID="txtEmail" runat="server"></asp:TextBox>
<asp:RegularExpressionValidator ID="RegularExpressionValidator1" runat="server"
ControlToValidate="txtEmail" ErrorMessage="Email ID not valid!!!" ValidationExpression="\w+([-
+.']\w+)*@\w+([-.]\w+)*\.\w+([-.]\w+)*"></asp:RegularExpressionValidator>
<br />
<br />
<asp:Label ID="Label4" runat="server" Text="Password"></asp:Label>
<asp:TextBox ID="txtPwd" runat="server"></asp:TextBox>
<asp:CompareValidator ID="CompareValidator1" runat="server" ControlToCompare="txtPwd"
ControlToValidate="txtRetype" ErrorMessage="Passsword's don't match!!!"></asp:CompareValidator>
<br />
<br />
<asp:Label ID="Label5" runat="server" Text="Retype:"></asp:Label>
<asp:TextBox ID="txtRetype" runat="server" style="margin-left: 22px"></asp:TextBox>
<br />
<br />
<asp:Label ID="Label6" runat="server" Text="Gender:"></asp:Label>
<br />
<asp:ValidationSummary ID="ValidationSummary1" runat="server" HeaderText="PLEASE CORRECT THE
FOLLOWING ERRORS!!!" ShowMessageBox="True" />
<br />
<asp:RadioButton ID="RadioButton1" runat="server" Text="Male" />
<asp:RadioButton ID="RadioButton2" runat="server" Text="Female" />
<br />
<br />
<asp:Button ID="btnSubmit" runat="server" Text="Submit" />
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&n
bsp;&nbsp;&nbsp;&nbsp;
<asp:Button ID="btnReset" runat="server" Text="Reset" />
<br />
<br />
<br />
<br />
<br />
</div>
</form>
</body>
</html>

Add the above Source Code and run the program.

Q2.Create Web Form to demonstrate use of Adrotator Control.

GUI:

TYIT – Sem – V - Advanced Web Programming –Paper (III)

Compiled By Swarupa P. Gogate Page 17
<%@ Page Language="C#" AutoEventWireup="true" CodeBehind="AdRotatorDemo.aspx.cs"
Inherits="WebApp_AWP_D.AdRotatorDemo" %>
<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">
<head runat="server">
<title></title>
</head>
<body>
<form id="form1" runat="server">
<div style="background-color: #FF00FF; height: 858px; width: 957px;">
<asp:AdRotator ID="AdRotator1" runat="server" DataSourceID="XmlDataSource1" />
<br />
<br />
<asp:XmlDataSource ID="XmlDataSource1" runat="server" DataFile="~/adv.xml"></asp:XmlDataSource>
<br />
<br />
<br />
WELCOME TO ADVERTISEMENTS!!!!</div>
</form>
</body>
</html>

XML File
<?xml version="1.0" encoding="utf-8" ?>
<Advertisements>
<Ad>
<ImageUrl>Images\p1.jpg</ImageUrl>
<NavigateUrl>https://www.plants.com/</NavigateUrl>
<AlternateText>Order Plants</AlternateText>
<Impressions>20</Impressions>
<Keyword>plants</Keyword>
<Height>500</Height>
<width>2000</width>
</Ad>
<Ad>

TYIT – Sem – V - Advanced Web Programming –Paper (III)

Compiled By Swarupa P. Gogate Page 18
<ImageUrl>Images\p2.jpg</ImageUrl>
<NavigateUrl>https://www.plants.com/</NavigateUrl>
<AlternateText>Order Plants</AlternateText>
<Impressions>20</Impressions>
<Keyword>plants</Keyword>
<Height>500</Height>
<width>2000</width>
</Ad>
<Ad>
<ImageUrl>Images\p3.jpg</ImageUrl>
<NavigateUrl>https://www.plants.com/</NavigateUrl>
<AlternateText>Order Plants</AlternateText>
<Impressions>10</Impressions>
<Keyword>plants</Keyword>
<Height>500</Height>
<width>2000</width>
</Ad>
<Ad>
<ImageUrl>Images\p4.jpg</ImageUrl>
<NavigateUrl>https://www.plants.com/</NavigateUrl>
<AlternateText>Order Plants</AlternateText>
<Impressions>30</Impressions>
<Keyword>plants</Keyword>
<Height>500</Height>
<width>2000</width>
</Ad>
</Advertisements>

TYIT – Sem – V - Advanced Web Programming –Paper (III)

Compiled By Swarupa P. Gogate Page 19

TYIT – Sem – V - Advanced Web Programming –Paper (III)

Compiled By Swarupa P. Gogate Page 20
Run the web form.
Following images will be displayed randomly.
  
  
  
  
  
  
  Practical No: 06: Working with Database
6)-a) Create a web application bind data in a multiline textbox by querying in another textbox.
GUI:

Source Code:

Web.Config File Contents:
Add the following details to web.config file under <connectionStrings> tag.

T.Y.B.Sc. (I.T.) – Advanced Web Programming –Paper (III)

Compiled By Swarupa P. Gogate Page 2
Source Code:
using System;
using System.Collections.Generic;
using System.Linq;
using System.Web;
using System.Web.UI;
using System.Web.UI.WebControls;
using System.Data;
using System.Data.SqlClient;
using System.Configuration;
public partial class DataBinding : System.Web.UI.Page
{
protected void Page_Load(object sender, EventArgs e)
{
}
protected void Execute_Click(object sender, EventArgs e)
{
string constr =
ConfigurationManager.ConnectionStrings["constr "].ConnectionString;
SqlConnection con = new SqlConnection(constr);
con.Open();
SqlCommand cmd = new SqlCommand(TextBox1.Text, con);
SqlDataReader reader = cmd.ExecuteReader();
ListBox1.Items.Clear();
while (reader.Read())
{
//To add new blank line in the text area
for (int i = 0; i < reader.FieldCount - 1; i++)
{
ListBox1.Items.Add(reader[i].ToString());
}
}
reader.Close();
con.Close();
}
}
Output:

T.Y.B.Sc. (I.T.) – Advanced Web Programming –Paper (III)

Compiled By Swarupa P. Gogate Page 3
6)-b) Create a web application to display records by using database. (Display records in GridView by
configuring SQLDataSource Control)
This example uses following database named “AirLinesMaster” and a table named ”airLInesData”

GUI:

T.Y.B.Sc. (I.T.) – Advanced Web Programming –Paper (III)

Compiled By Swarupa P. Gogate Page 4
Source Code:

Steps To Configure:

T.Y.B.Sc. (I.T.) – Advanced Web Programming –Paper (III)

Compiled By Swarupa P. Gogate Page 5
Click on “New Connection” .
Add the folllwoing connection details.

T.Y.B.Sc. (I.T.) – Advanced Web Programming –Paper (III)

Compiled By Swarupa P. Gogate Page 6
Click on “Test Connection”. You should get the following message box.
Click “Ok” for the next step.

T.Y.B.Sc. (I.T.) – Advanced Web Programming –Paper (III)

Compiled By Swarupa P. Gogate Page 7
The database is added as follows.

Click on “Next”.

T.Y.B.Sc. (I.T.) – Advanced Web Programming –Paper (III)

Compiled By Swarupa P. Gogate Page 8
Click on “Next”.

T.Y.B.Sc. (I.T.) – Advanced Web Programming –Paper (III)

Compiled By Swarupa P. Gogate Page 9

T.Y.B.Sc. (I.T.) – Advanced Web Programming –Paper (III)

Compiled By Swarupa P. Gogate Page 10
Click on “Finish”.
Switch to GUI and Select an arrow next to GridView.
Set “SQLDataSource1” as data source.

T.Y.B.Sc. (I.T.) – Advanced Web Programming –Paper (III)

Compiled By Swarupa P. Gogate Page 11
Run the web form.
Output:

T.Y.B.Sc. (I.T.) – Advanced Web Programming –Paper (III)

Compiled By Swarupa P. Gogate Page 12
6)-c) Demonstrate the use of Datalist link control
Drag the Datalist control to web page from Toolbox->Data-> Datalist
Select “Choose Data Source” Option and select <New Data Source>

select SQL Database and click on OK.

T.Y.B.Sc. (I.T.) – Advanced Web Programming –Paper (III)

Compiled By Swarupa P. Gogate Page 13
Click on “New Connection”.
Enter the information according to following screenshot.

T.Y.B.Sc. (I.T.) – Advanced Web Programming –Paper (III)

Compiled By Swarupa P. Gogate Page 14

T.Y.B.Sc. (I.T.) – Advanced Web Programming –Paper (III)

Compiled By Swarupa P. Gogate Page 15

T.Y.B.Sc. (I.T.) – Advanced Web Programming –Paper (III)

Compiled By Swarupa P. Gogate Page 16

T.Y.B.Sc. (I.T.) – Advanced Web Programming –Paper (III)

Compiled By Swarupa P. Gogate Page 17
Output:

T.Y.B.Sc. (I.T.) – Advanced Web Programming –Paper (III)

Compiled By Swarupa P. Gogate Page 18
Practical No: 07: Working with Database
7)-a) Create a web application to display Databinding using dropdownlist control.
GUI:

Refer to the database used in 6(a) example.
Source Code:
using System;
using System.Collections.Generic;
using System.Linq;
using System.Web;
using System.Web.UI;
using System.Web.UI.WebControls;

T.Y.B.Sc. (I.T.) – Advanced Web Programming –Paper (III)

Compiled By Swarupa P. Gogate Page 19
using System.Data;
using System.Data.SqlClient;
using System.Configuration;
public partial class DBDropDown : System.Web.UI.Page
{
protected void Page_Load(object sender, EventArgs e)
{
if (IsPostBack == false)
{
string conStr = ConfigurationManager.ConnectionStrings["conStr"].ConnectionString;
SqlConnection con = new SqlConnection(conStr);
SqlCommand cmd = new SqlCommand("Select Flightno from airLinesData", con);
con.Open();
SqlDataReader reader = cmd.ExecuteReader();
DropDownList1.DataSource = reader;
DropDownList1.DataTextField = "Flightno";
DropDownList1.DataBind();
reader.Close();
con.Close();
}
}
protected void Button1_Click(object sender, EventArgs e)
{
Label1.Text = "The You Have Selected : " + DropDownList1.SelectedValue;
}
Output:

T.Y.B.Sc. (I.T.) – Advanced Web Programming –Paper (III)

Compiled By Swarupa P. Gogate Page 20

7)-c) Create a web application for inserting and deleting record from a database. (Using Execute-
Non Query).

GUI:

Source Code: - web.config File Contents
<configuration>
<system.web>
<compilation debug="true" ></compilation>
</system.web>
<connectionStrings>
<add name="constr" connectionString="Data Source=VM;Initial Catalog=Customers;Integrated
Security=True"
providerName="System.Data.SqlClient" />
</connectionStrings>
</configuration>
Source Code: - CS Code
using System;
using System.Data;
using System.Data.SqlClient;
namespace WebApplication2
{
public partial class CRUD_Demo : System.Web.UI.Page
{
protected void Page_Load(object sender, EventArgs e)
{
//Databases
}
protected void btnInsert_Click(object sender, EventArgs e)
{
string constr = ConfigurationManager.ConnectionStrings["constr"].ConnectionString;
SqlConnection con = new SqlConnection(constr);
string InsertQuery = "insert into tblCustomer values(@Cust_Id, @Name, @Country)";
SqlCommand cmd = new SqlCommand(InsertQuery, con);
cmd.Parameters.AddWithValue("@Cust_Id", TextBox1.Text);
cmd.Parameters.AddWithValue("@Name", TextBox2.Text);
cmd.Parameters.AddWithValue("@Country", TextBox3.Text);
con.Open();
cmd.ExecuteNonQuery();
lblShow.Text = "Record Inserted Successfuly.";
con.Close();

T.Y.B.Sc. (I.T.) – Advanced Web Programming –Paper (III)

Compiled By Swarupa P. Gogate
  
  
  
  Practical No: 06: Working with Database
6)-a) Create a web application bind data in a multiline textbox by querying in another textbox.
GUI:

Source Code:

Web.Config File Contents:
Add the following details to web.config file under <connectionStrings> tag.

T.Y.B.Sc. (I.T.) – Advanced Web Programming –Paper (III)

Compiled By Swarupa P. Gogate Page 2
Source Code:
using System;
using System.Collections.Generic;
using System.Linq;
using System.Web;
using System.Web.UI;
using System.Web.UI.WebControls;
using System.Data;
using System.Data.SqlClient;
using System.Configuration;
public partial class DataBinding : System.Web.UI.Page
{
protected void Page_Load(object sender, EventArgs e)
{
}
protected void Execute_Click(object sender, EventArgs e)
{
string constr =
ConfigurationManager.ConnectionStrings["constr "].ConnectionString;
SqlConnection con = new SqlConnection(constr);
con.Open();
SqlCommand cmd = new SqlCommand(TextBox1.Text, con);
SqlDataReader reader = cmd.ExecuteReader();
ListBox1.Items.Clear();
while (reader.Read())
{
//To add new blank line in the text area
for (int i = 0; i < reader.FieldCount - 1; i++)
{
ListBox1.Items.Add(reader[i].ToString());
}
}
reader.Close();
con.Close();
}
}
Output:

T.Y.B.Sc. (I.T.) – Advanced Web Programming –Paper (III)

Compiled By Swarupa P. Gogate Page 3
6)-b) Create a web application to display records by using database. (Display records in GridView by
configuring SQLDataSource Control)
This example uses following database named “AirLinesMaster” and a table named ”airLInesData”

GUI:

T.Y.B.Sc. (I.T.) – Advanced Web Programming –Paper (III)

Compiled By Swarupa P. Gogate Page 4
Source Code:

Steps To Configure:

T.Y.B.Sc. (I.T.) – Advanced Web Programming –Paper (III)

Compiled By Swarupa P. Gogate Page 5
Click on “New Connection” .
Add the folllwoing connection details.

T.Y.B.Sc. (I.T.) – Advanced Web Programming –Paper (III)

Compiled By Swarupa P. Gogate Page 6
Click on “Test Connection”. You should get the following message box.
Click “Ok” for the next step.

T.Y.B.Sc. (I.T.) – Advanced Web Programming –Paper (III)

Compiled By Swarupa P. Gogate Page 7
The database is added as follows.

Click on “Next”.

T.Y.B.Sc. (I.T.) – Advanced Web Programming –Paper (III)

Compiled By Swarupa P. Gogate Page 8
Click on “Next”.

T.Y.B.Sc. (I.T.) – Advanced Web Programming –Paper (III)

Compiled By Swarupa P. Gogate Page 9

T.Y.B.Sc. (I.T.) – Advanced Web Programming –Paper (III)

Compiled By Swarupa P. Gogate Page 10
Click on “Finish”.
Switch to GUI and Select an arrow next to GridView.
Set “SQLDataSource1” as data source.

T.Y.B.Sc. (I.T.) – Advanced Web Programming –Paper (III)

Compiled By Swarupa P. Gogate Page 11
Run the web form.
Output:

T.Y.B.Sc. (I.T.) – Advanced Web Programming –Paper (III)

Compiled By Swarupa P. Gogate Page 12
6)-c) Demonstrate the use of Datalist link control
Drag the Datalist control to web page from Toolbox->Data-> Datalist
Select “Choose Data Source” Option and select <New Data Source>

select SQL Database and click on OK.

T.Y.B.Sc. (I.T.) – Advanced Web Programming –Paper (III)

Compiled By Swarupa P. Gogate Page 13
Click on “New Connection”.
Enter the information according to following screenshot.

T.Y.B.Sc. (I.T.) – Advanced Web Programming –Paper (III)

Compiled By Swarupa P. Gogate Page 14

T.Y.B.Sc. (I.T.) – Advanced Web Programming –Paper (III)

Compiled By Swarupa P. Gogate Page 15

T.Y.B.Sc. (I.T.) – Advanced Web Programming –Paper (III)

Compiled By Swarupa P. Gogate Page 16

T.Y.B.Sc. (I.T.) – Advanced Web Programming –Paper (III)

Compiled By Swarupa P. Gogate Page 17
Output:

T.Y.B.Sc. (I.T.) – Advanced Web Programming –Paper (III)

Compiled By Swarupa P. Gogate Page 18
Practical No: 07: Working with Database
7)-a) Create a web application to display Databinding using dropdownlist control.
GUI:

Refer to the database used in 6(a) example.
Source Code:
using System;
using System.Collections.Generic;
using System.Linq;
using System.Web;
using System.Web.UI;
using System.Web.UI.WebControls;

T.Y.B.Sc. (I.T.) – Advanced Web Programming –Paper (III)

Compiled By Swarupa P. Gogate Page 19
using System.Data;
using System.Data.SqlClient;
using System.Configuration;
public partial class DBDropDown : System.Web.UI.Page
{
protected void Page_Load(object sender, EventArgs e)
{
if (IsPostBack == false)
{
string conStr = ConfigurationManager.ConnectionStrings["conStr"].ConnectionString;
SqlConnection con = new SqlConnection(conStr);
SqlCommand cmd = new SqlCommand("Select Flightno from airLinesData", con);
con.Open();
SqlDataReader reader = cmd.ExecuteReader();
DropDownList1.DataSource = reader;
DropDownList1.DataTextField = "Flightno";
DropDownList1.DataBind();
reader.Close();
con.Close();
}
}
protected void Button1_Click(object sender, EventArgs e)
{
Label1.Text = "The You Have Selected : " + DropDownList1.SelectedValue;
}
Output:

T.Y.B.Sc. (I.T.) – Advanced Web Programming –Paper (III)

Compiled By Swarupa P. Gogate Page 20

7)-c) Create a web application for inserting and deleting record from a database. (Using Execute-
Non Query).

GUI:

Source Code: - web.config File Contents
<configuration>
<system.web>
<compilation debug="true" ></compilation>
</system.web>
<connectionStrings>
<add name="constr" connectionString="Data Source=VM;Initial Catalog=Customers;Integrated
Security=True"
providerName="System.Data.SqlClient" />
</connectionStrings>
</configuration>
Source Code: - CS Code
using System;
using System.Data;
using System.Data.SqlClient;
namespace WebApplication2
{
public partial class CRUD_Demo : System.Web.UI.Page
{
protected void Page_Load(object sender, EventArgs e)
{
//Databases
}
protected void btnInsert_Click(object sender, EventArgs e)
{
string constr = ConfigurationManager.ConnectionStrings["constr"].ConnectionString;
SqlConnection con = new SqlConnection(constr);
string InsertQuery = "insert into tblCustomer values(@Cust_Id, @Name, @Country)";
SqlCommand cmd = new SqlCommand(InsertQuery, con);
cmd.Parameters.AddWithValue("@Cust_Id", TextBox1.Text);
cmd.Parameters.AddWithValue("@Name", TextBox2.Text);
cmd.Parameters.AddWithValue("@Country", TextBox3.Text);
con.Open();
cmd.ExecuteNonQuery();
lblShow.Text = "Record Inserted Successfuly.";
con.Close();

T.Y.B.Sc. (I.T.) – Advanced Web Programming –Paper (III)

Compiled By Swarupa P. Gogate
  
  
  XML Text Writer Code
GUI: -

Source Code:-
using System;
using System.Collections.Generic;
using System.Linq;
using System.Web;
using System.Web.UI;
using System.Web.UI.WebControls;
using System.IO;
using System.Xml;
namespace WebApplication1
{
public partial class WebForm1 : System.Web.UI.Page
{
protected void Page_Load(object sender, EventArgs e)
{
//Program To Create an XML file
}
protected void btnCreate_Click(object sender, EventArgs e)
{
//Set the path for the file Creation
string file =
Path.Combine(Request.PhysicalApplicationPath,@"App_Data\SuperProProductList.xml");
//Create a new File; If it already exists then overwrite
FileStream fs = new FileStream(file, FileMode.Create);
XmlTextWriter w = new XmlTextWriter(fs, null);
w.WriteStartDocument();
w.WriteStartElement("SuperProProductList");
w.WriteComment("This file generated by the XmlTextWriter class.");
// Write the first product.
w.WriteStartElement("Product");
w.WriteAttributeString("ID", "1");
w.WriteAttributeString("Name", "Chair");
w.WriteStartElement("Price");
w.WriteString("49.33");
w.WriteEndElement();
w.WriteEndElement();
// Write the second product.
w.WriteStartElement("Product");
w.WriteAttributeString("ID", "2");
w.WriteAttributeString("Name", "Car");
w.WriteStartElement("Price");
w.WriteString("43399.55");
w.WriteEndElement();

T.Y.B.Sc. (I.T.) – Advanced Web Programming –Paper (III) 2018-2019

Compiled By Swarupa P. Gogate Page 2
w.WriteEndElement();
// Write the third product.
w.WriteStartElement("Product");
w.WriteAttributeString("ID", "3");
w.WriteAttributeString("Name", "Fresh Fruit Basket");
w.WriteStartElement("Price");
w.WriteString("49.99");
w.WriteEndElement();
w.WriteEndElement();
// Close the root element.
w.WriteEndElement();
w.WriteEndDocument();
w.Close();
Response.Write("XML File Created Successfully...Check the contents in
App_Data folder");
}
}
}
Output:-

XML File Contents:-

T.Y.B.Sc. (I.T.) – Advanced Web Programming –Paper (III) 2018-2019

Compiled By Swarupa P. Gogate Page 3
XML Text Reader Code
GUI:-

Create the following file named “Books.xml” and place it under App_Data folder

Source Code:-
using System;
using System.Collections.Generic;
using System.Linq;
using System.Web;
using System.Web.UI;
using System.Web.UI.WebControls;
using System.IO;
using System.Xml;
namespace WebApplication1
{
public partial class WebForm1 : System.Web.UI.Page
{
protected void Page_Load(object sender, EventArgs e)
{
//XMLTextReader
}
protected void btnRead_Click(object sender, EventArgs e)
{
string file =
Path.Combine(Request.PhysicalApplicationPath,@"App_Data\Books.xml");
FileStream fs = new FileStream(file, FileMode.Open);
XmlTextReader r = new XmlTextReader(fs);
StringWriter writer = new StringWriter();
// Parse the file, and read each node.
while (r.Read())
{
// Skip whitespace.
if (r.NodeType == XmlNodeType.Whitespace) continue;
writer.Write("<b>Type:</b> ");
writer.Write(r.NodeType.ToString());
writer.Write("<br>");
// The name is available when reading the opening and closing tags
// for an element. It’s not available when reading the inner content.

T.Y.B.Sc. (I.T.) – Advanced Web Programming –Paper (III) 2018-2019

Compiled By Swarupa P. Gogate Page 4
if (r.Name != "")
{
writer.Write("<b>Name:</b> ");
writer.Write(r.Name);
writer.Write("<br>");
}
// The value is when reading the inner content.
if (r.Value != "")
{
writer.Write("<b>Value:</b> ");
writer.Write(r.Value);
writer.Write("<br>");
}
if (r.AttributeCount > 0)
{
writer.Write("<b>Attributes:</b> ");
for (int i = 0; i < r.AttributeCount; i++)
{
writer.Write(" ");
writer.Write(r.GetAttribute(i));
writer.Write(" ");
}
writer.Write("<br>");
}
writer.Write("<br>");
}
fs.Close();
// Copy the string content into a label to display it.
lblXml.Text = writer.ToString();
}
}
}
Output:-

T.Y.B.Sc. (I.T.) – Advanced Web Programming –Paper (III) 2018-2019

Compiled By Swarupa P. Gogate
                                     
                                     
PRACTICAL 10 c) - Implementing AJAX for displaying Random Images.
Steps in RandomImageSlideShow.aspx
 Add a folder named Images to the root of the project and paste4 images into it which are having
1.jpg, 2.jpg... up to 4.jpg.
 Add another WebForm called RandomImageSlideShow.
 Add ScriptManager control into the div tag of the form. Remember to add this inside the form tag
always.
 Add UpdatePanel control under ScriptManager control inside the div
 Add ContentTemplate tag inside the UpdatePanel.
 Add a Timer control within that ContentTemplate tag and set the interval as 1000ms.
 Add Image control under Timer control inside the ContentTemplate tag and set attribute Height
and Width as 200.
 Add text ImageDisplaying: followed by Label control under Image control inside the
ContentTemplateWe renamed that label as lblImageDisplaying.
GUI:

<%@PageLanguage="C#"AutoEventWireup="true"CodeBehind="WebForm6.aspx.cs"Inherits="WebAppli
cationDiv1.WebForm6"%>
<!DOCTYPEhtml>
<htmlxmlns="http://www.w3.org/1999/xhtml">
<headrunat="server">
<title></title>
</head>

T.Y.B.Sc. (I.T.) – Advanced Web Programming –Paper (III)

Compiled By Swarupa P. Gogate Page 2
<body>
<formid="form1"runat="server">
<div>
<asp:ScriptManagerID="ScriptManager1"runat="server"></asp:ScriptManager>
<asp:UpdatePanelID="UpdatePanel1"runat="server">
<ContentTemplate>
<asp:TimerID="Timer1"runat="server"Interval="1000"OnTick="Timer1_Tick"></asp:Timer>
<asp:ImageID="Image1"runat="server"Height="200"Width="200"ImageUrl="~/Images/p1.jpg"/
>
ImageDisplaying: <asp:LabelID="lblImageDisplaying"runat="server"Text="Label"></asp:Label>
</ContentTemplate>
</asp:UpdatePanel>
</div>
</form>
</body>
</html>
 Steps in RandomImageSlideShow.aspx.cs
 Create a private named SetImageUrl.
 Within that method create an object of Random
 Generate a random number from 1 to 8 using Next method of the Random object and get that
random number into an integer variable called i.
 Set the ImageUrl property in Image control using the above random number for the image file
name.
 Set the Text property of the Label control using that random number as the image file name.
 Call SetImageUrl method from Page_Load event if it is not a postback.
 Add the Tick event handler and call SetImageUrl method from it.
using System;
usingSystem.Collections.Generic;
usingSystem.Linq;
usingSystem.Web;
usingSystem.Web.UI;
usingSystem.Web.UI.WebControls;
namespace WebApplicationDiv1
{
publicpartialclassWebForm6 : System.Web.UI.Page
{
protectedvoidPage_Load(object sender, EventArgs e)
{
if (!IsPostBack)
{
SetImageUrl();
}
}
protectedvoid Timer1_Tick(object sender, EventArgs e)
{
SetImageUrl();
}
privatevoidSetImageUrl()
{
Random ran = newRandom();

T.Y.B.Sc. (I.T.) – Advanced Web Programming –Paper (III)

Compiled By Swarupa P. Gogate
  
  Implementing Forms Authentication in asp.net
GUI: - Login.aspx

GUI: - Welcome.aspx

Source Code:-
Set web.config file to implement the authentication of web application as follows

T.Y.B.Sc. (I.T.) – Advanced Web Programming –Paper (III) 2018-2019

Compiled By Swarupa P. Gogate Page 2
using System;
using System.Collections.Generic;
using System.Linq;
using System.Web;
using System.Web.UI;
using System.Web.UI.WebControls;
using System.Web.Security;
namespace FormAuth
{
public partial class Login : System.Web.UI.Page
{
protected void Page_Load(object sender, EventArgs e)
{
//This is the code for LoginPage
}
protected void Login_Click(object sender, EventArgs e)
{
if
(FormsAuthentication.Authenticate(txtUserName.Text,txtUserPassword.Text))
{
FormsAuthentication.RedirectFromLoginPage(txtUserName.Text,
chkPersist.Checked);
}
else
{
lblMessage.Text = "Invalid User Name and/or Password";
}
}
}
}
Output:-
On entering incorrect Login Name or Password

On entering correct Login Name or Password

T.Y.B.Sc. (I.T.) – Advanced Web Programming –Paper (III) 2018-2019

Compiled By Swarupa P. Gogate
