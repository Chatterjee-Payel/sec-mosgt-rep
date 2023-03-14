# sec-mosgt-rep
class Solution
{
  public:
    string secFrequent (string arr[], int n)
    {
        //code here.
        map<string,int>mp;
         string str="";
         int max1=INT_MIN;
         int max2=INT_MIN;
         for(int it=0;it<n;it++){
             mp[arr[it]]++;
         }
         for(auto it:mp)
         {
             if(it.second>max1)
             {
                 max1=it.second;
             }
         }
         for(auto it:mp)
    {
        if(it.second>max2 && it.second<max1)
        {
           max2=it.second;
            str=it.first;
        }
    }
    
     return str;

    }
};
