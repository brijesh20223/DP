## Approach:
![alt text](https://github.com/brijesh20223/DP/blob/main/stringDP/Longest%20Common%20Substring/img/lcssa1.jpeg)
```cpp
int
longestCommonSubstr (string S1, string S2, int n, int m)
{
  int k = min (m, n);
  for (k; k >= 1; k--)
    {
      for (int i = 0; i <= n - k; i++)
	{
	  string s = S1.substr (i, k);
	  for (int j = 0; j <= m - k; j++)
	    {
	      if (s == S2.substr (j, k))
		return k;
	    }
	}
    }
  return 0;
}

```
#### ***Time O(n\*m^2)***
#### ***Spaace O(1)***
