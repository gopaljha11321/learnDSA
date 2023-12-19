#include <iostream>
using namespace std;

class Trie{
    public:
    bool isLeaf=false;
    int sizeOfArray=26;
    Trie * character[26];
    Trie() {
        for (int i = 0; i < sizeOfArray; i++) { //sizeOfArray(26)
        this -> character[i] = nullptr;
    }
  }
};

void insert(Trie * head, string key) {
  for (auto itr: key) {
    int index = itr - 'a';
    if (head -> character[index] == nullptr) {
      head -> character[index] = new Trie();
    }
    head = head -> character[index];
  }
  head -> isLeaf = true;
}

bool search(Trie * head, string key) {
  for (auto itr: key) {
    int index = itr - 'a';
    if (head -> character[index] == nullptr) {
      return false;
    }
    head = head -> character[index];
  }
  return head -> isLeaf;
}

int main()
{
   Trie* n1=new Trie();
   insert(n1,"gopal");
   insert(n1,"gopaljha11321");
   insert(n1,"gopaljha");
   insert(n1,"gopaljha11");
   int a=5;
   while(a--){
    string str;
    cin>>str;  
    search(n1, str)?cout<<"Username already in use"<<endl:cout<<"It is available"<<endl;
   }
    return 0;
}
