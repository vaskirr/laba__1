fun quicksort(arr: IntArray, start: Int, end: Int) {
    if(start < end) {
        //Находим пивот
        val piv: Int = part(arr, start, end)
        //рекурсивно сортируем левую часть массива отн пивота
        quicksort(arr, start, piv)
        //рекурсивно сортируем правую часть массива отн пивота
        quicksort(arr, piv + 1, end)
    }
}

fun part(arr: IntArray, start: Int, end: Int): Int {
    // берем в качестве пивота первый элемент
    val piv = arr[start]
    var i: Int = start
    var j: Int = end
    while(i < j) {
        // увеличиваем i пока элемент с индексом i меньше либо равны пивота
        while(arr[i] <= piv && i < end) {
            i++
        }
        // уменьшаем j, пока элемент с индексом j больше либо равен пивоту
        while(arr[j] >= piv && j > start) {
            j--
        }
        // меняем значение эл. с индексами i и j если i<j
        if(i < j) {
            val vrem: Int = arr[i]
            arr[i] = arr[j]
            arr[j] = vrem
        }

    }
    // помещаем значение эл. с индексом j в начальный элемент, а эл-у с индексом j присваем значение пивота
    arr[start] = arr[j]
    arr[j] = piv
    return j
}

fun printArray(arr: IntArray) {
    val lastIndex: Int = arr.size - 1
    // вывод массива через цикл <питон с выводом массива в одну строчку =(>
    for (i in 0..lastIndex) {
        val el = arr[i]
        print("$el ")
    }
    println("")
}

fun main(args: Array<String>) {
    val arr: IntArray = intArrayOf(10, 20, 50, 30, 90, 40, 1, 1, 1, 0, 45699, 2)//вводим значения массива
    print("Изначальный массив: ")
    printArray(arr)
    quicksort(arr, 0, arr.size - 1)
    print("Массив после сортировки: ")
    printArray(arr)
}

