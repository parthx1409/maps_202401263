

class Solution {
public:
    int longestConsecutive(vector<int>& nums) {
        
        unordered_map<int, int> map;
        int max_len = 0;
        
        for (int num : nums) {

            if (map.find(num) != map.end()) continue;
          
            int left = map.find(num - 1) != map.end() ? map[num - 1] : 0;
            int right = map.find(num + 1) != map.end() ? map[num + 1] : 0;
          
            int current_len = left + right + 1;
            max_len = max(max_len, current_len);
            
            map[num] = current_len;
            map[num - left] = current_len;
            map[num + right] = current_len;
        }
        
        return max_len;
    }
};
