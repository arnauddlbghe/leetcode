# Intuition
On va chercher à tester toutes les combinaisons possibles entre deux nombres. On ignore si notre liste est ordonnée et on va donc devoir comparer chaque nombre avec chaque autre nombre.

# Approach
On va donc parcourir notre liste de nombre et pour chacun d'entre eux on va à nouveau parcourir notre liste et comparer si les critères sont respectés. Dès que les critères sont respectés, on peut renvoyer `true`. Pas besoin de continuer.

Une autre approche existe être en utilisant la structure `Set`.

# Complexity
- Time complexity: O(n^2), ou O(n)

- Space complexity: O(1), ou O(n)

# Code
```java []
class Solution {
    public boolean checkIfExist(int[] arr) {
        for (int i = 0; i < arr.length; i++) {
            for (int j = 0; j < arr.length; j++) {
                if (i != j && arr[i] == (2*arr[j])) {
                    return true;
                }
            }
        }
        return false;
    }
}
```

```java []
import java.util.HashSet;

public class Solution {
    public boolean checkIfExist(int[] arr) {
        Set<Integer> setOfNumbers = new HashSet<>();
        for (int n : arr) {
            if (setOfNumbers.contains(n * 2) || (n % 2 == 0 && setOfNumbers.contains(n / 2))) {
                return true;
            }
            setOfNumbers.add(n);
        }
        return false;
    }
}

```
