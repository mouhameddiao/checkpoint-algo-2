function triInsertion(arr) {
let n = arr.length;

    // Boucle à travers chaque élément du tableau
    for (let i = 1; i < n; i++) {
        // Choisir l'élément à insérer
        let key = arr[i];
        // Initialiser j pour pointer vers l'élément juste avant i
        let j = i - 1;

        // Déplacer les éléments de arr[0..i-1], qui sont plus grands que key,
        // d'une position vers la droite pour faire de la place pour key
        while (j >= 0 && arr[j] > key) {
            arr[j + 1] = arr[j];
            j = j - 1;
        }
        // Insérer key dans sa bonne position
        arr[j + 1] = key;
    }

    return arr;

}
