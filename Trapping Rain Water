class Solution {
public:
    int trap(vector<int>& v) {
        int n = v.size(),i;
        vector<int> l(n,-1),r(n,-1),s;
        for(i = 0; i < n; i++){
            while(!s.empty()&&s.back()<=v[i]){
                s.pop_back();
            }
            if(!s.empty()){
                l[i] = s.back();
                if(v[i]>s.back())
                s.push_back(v[i]);
            }else{
                s.push_back(v[i]);
            }
        }
        s.clear();
        for(i = n-1; i >= 0; i--){
            while(!s.empty()&&s.back()<=v[i]){
                s.pop_back();
            }
            if(!s.empty()){
                r[i] = s.back();
                if(v[i]>s.back())
                s.push_back(v[i]);
            }else{
                s.push_back(v[i]);
            }
        }
        int ans = 0;
        for(i = 0; i < n; i++){
            if(l[i] != -1 && r[i] != -1){
                ans += min(l[i],r[i])-v[i];
            }
        }
        return ans;
    }
};
