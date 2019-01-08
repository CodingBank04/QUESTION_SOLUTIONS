# QUESTION_SOLUTIONS
public class Solution {
    public int UniqueMorseRepresentations(string[] words) {
         HashSet<string> result=new HashSet<string>();
         Dictionary<char,string> match  = new Dictionary<char, string>()
            {
                {'a',".-"},
                {'b',"-..."},
                {'c',"-.-."},
                {'d',"-.."},
                {'e',"."},
                {'f',"..-."},
                {'g',"--."},
                {'h',"...."},
                {'i',".."},
                {'j',".---"},
                {'k',"-.-"},
                {'l',".-.."},
                {'m',"--"},
                {'n',"-."},
                {'o',"---"},
                {'p',".--."},
                {'q',"--.-"},
                {'r',".-."},
                {'s',"..."},
                {'t',"-"},
                {'u',"..-"},
                {'v',"...-"},
                {'w',".--"},
                {'x',"-..-"},
                {'y',"-.--"},
                {'z',"--.."},
            };
            
            string morse=string.Empty;
        
            for(int i =0 ; i<words.Length;i++)
            {
                morse="";
                foreach(char item in words[i])
                {
                    morse=morse+match[item];
                }
                result.Add(morse);
            }
        return result.Count;
    }
}
