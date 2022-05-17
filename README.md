#include<iostream>
using namespace std;
int k=1;
class staff {
    public:
        staff(int num_s,char name_s,char sex_s,char address_s,float salary_s);
    private:
        int num;
        char name,sex,address;
        float salary,real_salary;
};
class regular:virtual public staff {
    public:
        regular(int num_s,char name_s,char sex_s,char address_s,float salary_s,float allowance,float pension,float housing,float medical,float individual);
    private:
        float allowance,pension,housing,medical,individual;
};
class temporary:virtual public staff {
    public:
    staff(int num_s,char name_s,char sex_s,char address_s,float salary_s,float bonus,float individual);
    private:
        float bonus,individual;
};
void menu(void)
{
    int n;
    cout<<"  ******************************************************"<<endl;
    cout<<"  *                职工信息管理系统                    *"<<endl;
    cout<<"  ******************************************************"<<endl;
    cout<<"*********************系统功能菜单*************************"<<endl;
    cout<<"     ----------------------   ----------------------"<<endl;
    cout<<"     * 0.系统帮助及说明  * *  1.查询职工信息    *"<<endl;
    cout<<"     * 2.浏览职工信息    * *  3.增加职工信息    *"<<endl;
    cout<<"     * 4.修改职工信息    * *  5.删除职工信息    *"<<endl;
    cout<<"     * 6.退出系统        *"<<endl;
    cout<<"     ----------------------   ----------------------"<<endl;
    cout<<"请选择功能编号（选好后输入回车转到相应功能模块）:"<<endl;
    cout<<n<<endl;
    switch(n)
    {
        case 0:introduce();break;
        case 1:search();break;
        case 2:skim();break;
        case 3:add();break;
        case 4:change();break;
        case 5:reduce();break;
        case 8:
            k=0;
            system("cls");
            cout<<"退出程序!"<<endl;
            break;
        default:
            cout<<"按照您的需求请输入0-6之间的数字"<<endl;
            system("pause");
            system("cls");
   }
}
int main()
{
    printf("欢迎进入职工管理系统\n");
    begin();
    readinform();
    while(k)
    {
        menu();
    }
   return 0;
}
