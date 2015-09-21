# Apollon4ik
#include <iostream>
#include <set>
#include <iterator>
#include <cstdlib>
#include <ctime>
#include <bitset>
using namespace std;
int main ()
{
srand(time(NULL));
int c,m,k,n,b,bul=1 ;
set<int> mySet;
multiset<int> mySzet;
cout << "Vvedite K " << endl ;
cin >> k ;
int K[k];
cout << "vvedite M " << endl;
cin >> m ;
cout << "Vvedite N" << endl;
cin >> n ;
c= rand() % n+m ;
for( int i = 0; i!=k; i++)
        {
        K[i]=rand()% m;
        mySet.insert( K[i] );
        mySzet.insert (K[i]);
        if(K[i]==c) cout << "Yes \n";
        else if (k-1==i) cout << "No \n";
        }
cout<< "Slu4ainoe 4islo " << c << endl ;
cout << "Mnoshestvo s povtoyaushimi  " << endl ;
copy( mySzet.begin(), mySzet.end(), ostream_iterator<int>(cout, " "));
cout << endl;
cout << "Mnoshestvo bez povtoyaushih elementov \n"<< endl ;
copy( mySet.begin(), mySet.end(), ostream_iterator<int>(cout, " \n"));
cout << "Moshnost mnoshestva " << mySet.size()<< endl;
b=mySet.size();
for ( int i = 0 ; i!=b;i++)
{
 bul=bul*2;
}
cout << bul << "Kardinalnoe 4islo buleana";
return 0 ;
}
