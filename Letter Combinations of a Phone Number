class Solution {    
public:
    void help(int i,string digits,string mapping[],string sol,vector<string>&ans){
        if(i==digits.length()){
            ans.push_back(sol);
            return;
        }

        int num=digits[i]-'0';
        string val=mapping[num];

        for(int j=0;j<val.length();j++){
            sol.push_back(val[j]);
            help(i+1,digits,mapping,sol,ans);
            sol.pop_back();
        }
    }
    vector<string> letterCombinations(string digits) {
        vector<string>ans;
        string sol;
        if(digits.length()==0){
            return ans;
        }
        string mapping[10]={"","","abc","def","ghi","jkl","mno","pqrs","tuv","wxyz"};
        help(0,digits,mapping,sol,ans);
        return ans;
    }
};
