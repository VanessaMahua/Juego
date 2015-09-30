#include <iostream>

using namespace std;
void tutorial();

/* run this program using the console pauser or add your own getch, system("pause") or input loop */

int main(int argc, char** argv) {
	cout <<  " " << endl;
	cout << " Welcome, Enter the option you wanna get in to: " << endl;
	cout <<  " " << endl;
	cout <<  " 1_Arriba" << endl;
	cout <<  " 2_Abajo"<< endl;
	cout <<  " 3_Izquierda"<< endl;
	cout <<  " 4_Derecha"<< endl;


	
	tutorial();

	return 0;
}




void tutorial() {
	int level=0;
	char charme = char(2);
	char charend = char(88);
	int me[] = {1, 7};
	int end[] = {13, 14};
//	char matriztuto[11][20]={{char(219),char(219),char(219),char(219),char(219),char(219),char(219),char(219),char(219),char(219)},
//				{char(219),' ',' ',' ',' ',' ',' ',' ',' ',char(176)},
//				{char(219),' ',' ',' ',' ',' ',' ',' ',' ',char(219)},
//				{char(219),char(219),char(219),char(219),char(219),' ',' ',char(254),' ',char(219)},
//				{char(219),' ',' ',' ',' ',' ',' ',' ',char(219),char(219)},
//				{char(219),' ',' ',' ',char(219),' ',' ',' ',' ',char(219)},
//				{char(219),' ',char(254),' ',char(219),' ',char(219),char(219),char(219),char(219)},
//				{char(219),' ',' ',' ',' ',' ',' ',' ',' ',char(219)},
//				{char(219),' ',' ',' ',' ',' ',' ',' ',' ',char(219)},
//				{char(219),' ',' ',' ',char(219),' ',' ',' ',' ',char(219)},
//				{char(219),char(219),char(219),char(219),char(219),char(219),char(219),char(219),char(219),char(219)}};
				
	char matriztuto[20][80]={{char(176),char(176),char(176),char(176),char(176),char(176),char(176),char(176),char(176),char(176),char(176),char(176),char(176),char(176),char(176),char(176),char(176),char(176),char(176),char(176)},
		{char(176),' ',' ',' ',char(219),' ',' ',char(2),' ',' ',char(219),' ',' ',' ',' ',' ',' ',' ',' ',char(176)},
		{char(219),' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',char(176)},
		{char(219),' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',char(176)},
		{char(219),' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',char(176)},
		{char(219),' ',' ',' ',' ',' ',' ',' ',' ',' ',char(219),' ',' ',' ',' ',' ',' ',' ',' ',char(176)},
		{char(219),' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',char(219),' ',' ',' ',char(176)},
		{char(176),' ',' ',' ',' ',' ',char(219),char(219),char(219),' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',char(219)},
		{char(176),' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',char(219)},
		{char(176),' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',char(219)},
		{char(176),' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',char(219)},
		{char(176),' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',char(176)},
		{char(176),' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',char(176)},
		{char(176),' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',char(88),char(219),' ',' ',' ',char(176)},
		{char(176),' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',char(219),' ',' ',char(219),char(219),' ',' ',' ',char(176)},
		{char(176),' ',' ',' ',char(219),' ',' ',' ',' ',' ',' ',char(219),' ',' ',' ',' ',' ',' ',' ',char(176)},
		{char(176),' ',' ',' ',char(219),char(219),' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',char(176)},
		{char(176),' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',char(176)},
		{char(176),' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',' ',char(176)},
{char(176),char(176),char(176),char(219),char(219),char(219),char(176),char(176),char(219),char(176),char(176),char(176),char(176),char(176),char(176),char(176),char(176),char(176),char(176),char(176)}};

				
				
	int a[]={1,7};
	int lon[]={20,20};
	
	//printScene(matriztuto, lon[0], lon[1]);
	
	matriztuto[me[0]][me[1]] = charme;
	matriztuto[end[0]][end[1]] = charend;
	
	
	for(int i = 0; i < lon[0]; i++){
		cout<<"\t\t";
        for(int j = 0; j < lon[1]; j++){
            cout<<matriztuto[i][j];
        }
        cout<<" "<<endl;
    }
		
	int op=0;
	while (op != -1) {
		
		cin >> op;
		
		bool b = true;
		while (b) {
			int tmp[] = {me[0], me[1]};
			
			if (op == 1)
				tmp[0]--;
			else if (op == 2)
				tmp[0]++;
			else if (op == 3)
				tmp[1]--;
			else if (op == 4)
				tmp[1]++;
			else {
			}
			
			if (matriztuto[tmp[0]][tmp[1]] == ' ' || matriztuto[tmp[0]][tmp[1]] == charend) {
				matriztuto[me[0]][me[1]] = ' ';
				me[0] = tmp[0];
				me[1] = tmp[1];
				matriztuto[me[0]][me[1]] = charme;
			}else {
				b = false;
			}
			
			
			system("cls");
			for(int i = 0; i < lon[0]; i++){
				cout<<"\t\t";
		        for(int j = 0; j < lon[1]; j++){
		            cout<<matriztuto[i][j];
		        }
		        cout<<" "<<endl;
		    }
		}
		if (me[0] == end[0] && me[1] == end[1])  {
			cout << "\n\n" << endl;
			cout<<"                         *                *                   *     "<<endl;
    cout<<"             *                                     *                "<<endl;
    cout<<"     *              |           *             *        *         *  "<<endl;
    cout<<"          *        -+-                 *                            "<<endl;
    cout<<"       __           |      *             *          *        *      "<<endl;
    cout<<"   ___|  |   *     _|_              *    ____    ____               "<<endl;
    cout<<"   [_]|°°|__      _| |_        *    |   |....|  |....|    *     *   "<<endl;     
    cout<<"      |     |   _|[] []|_    ___    |   |....|  | ___|__            "<<endl;
    cout<<"   [_]|  °° |__|_  ______|  |   |  |_|  |....|  || -- - |   *     * "<<endl;
    cout<<"      |________  |__     |  |# #|  |_|  |....|  || - -- |  _____    "<<endl;
    cout<<"   [_]| _____ |     |__[]|  |   |  |_|  |....|__|| -- - | |* * *|   "<<endl;
    cout<<"      | [___] |        |__  |# #|  |_|  |....|__|| -- -_|_|* * *|   "<<endl;
    cout<<"   [_]|       | °°        | |   |__| |__|....|  || ___|* *|* * *|   "<<endl;
    cout<<"      | _____ |           |__  #|_______|....|  | |* *|* *|* * *|   "<<endl;    
    cout<<"   [_]| [___] |       °°     |__|_______|__  |  | |* *|* *|* * *|   "<<endl;
    cout<<"      |       |            __|_____________|__    |* *|* *|* * *|   "<<endl;
    cout<<"   [_]| _____ |  °°      _|___________________|_  |* *|* *|* * *|   "<<endl;
    cout<<"      | [___] |         |_______________________|  ______________   "<<endl;
    cout<<"    __|_______|_________|_______________________| _________________ "<<endl;
    cout<<"   |_______________________________________________________________|"<<endl;
    cout<<"   |||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||"<<endl;
    cout<<"   |||||||||||||||||||||   G A N A S T E S      ||||||||||||||||||||"<<endl;
    cout<<"   |||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||"<<endl;
    cout << "\n\n" << endl;
			return;
		}
	}
	

	
}

