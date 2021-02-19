class primeiroExercicioCalculadoraKotlin {
}
fun main(){
    println("Calculadora ")
    val a: Float
    val b : Float
    var opc: Int
    val r : Float
    println("Primeiro valor a ser calculado: ")
    a = readLine()!!.toFloat()
    println("Segundo valor a ser calculado: ")
    b = readLine()!!.toFloat()
    println("Qual operação deseja realizar? \n [1] soma \n [2] Subtração \n [3] Multiplicação \n [4] Divisão ")
    opc = readLine()!!.toInt()
    println("Sua opção foi: $opc")
    while(opc > 4)
    {println("Opção inválida, tente novamente ")
        println("Qual operação deseja realizar? \n [1] soma \n [2] Subtração \n [3] Multiplicação \n [4] Divisão ")
        opc = readLine()!!.toInt()}



        if (opc == 1) {
             r = cal(a,b,:: soma)
             println ("O resultado da operação é: $r")}
        else if (opc == 2){
            r = cal(a,b, :: sub)
            println ("O resultado da operação é: $r")}
        else if (opc ==3){
            r = cal(a,b, :: mul)
            println ("O resultado da operação é: $r")}
        else if (opc ==4){
            r = cal(a,b, :: div)
            println ("O resultado da operação é: $r")}
        else{
            println("Opção inválida, tente novamente ")}



}
fun cal (n: Float, n0:Float, operacao:(Float, Float)-> Float):Float{
    val resultado = operacao (n,n0)
    return resultado
}
fun soma(n1:Float, n2:Float)= n1.plus(n2)
fun sub(n1:Float, n2:Float)= n1.minus(n2)
fun mul(n1:Float, n2:Float)= n1.times(n2)
fun div(n1:Float, n2:Float)= n1.div(n2)


}