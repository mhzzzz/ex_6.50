# ex_6.50
可行函数与匹配函数

    #include<iostream>

    using std::cout;
    using std::endl;

    void f()
    {
	    #ifndef NDEBUG
		    cout<<"should have no parameter"<<endl;
	    #endif
    }
    void f(int v)
     {
	    #ifndef NDEBUG
		    cout<<"one parameter of int type"<<endl;
	    #endif
		    cout<<v<<endl;
    }

    void f(int v1, int v2)
    {
	    #ifndef NDEBUG
		    cout<<"two parameters of int type"<<endl;
	    #endif
		    cout<<v1<<" "<<v2<<endl;
    }

    void f(double v1, double v2 = 3.14)
    {
	    #ifndef NDEBUG
		    cout<<"two parameters of double type"<<endl;
	    #endif
		    cout<<v1<<" "<<v2<<endl;
    }

    int main()
    {
    //	f(2.56, 42);  //ambiguous.
	    f(42);
	    f(42, 0);
	    f(2.56, 3.14);
	    return 0;
    }
