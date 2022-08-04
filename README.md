# Pesquisa-de-caracteristicas-fisicas-em-vetor
Trabalho da faculdade onde fizemos em java  pesquisa de caracteristicas fisicas de uma certa regiao, aonde calculava a media das idades das pessoas e entre outros..

import java.util.Random;
import java.util.Scanner;
public class Q1 {
 
       
    Scanner sc = new Scanner(System.in);
    static int []age (){
        Scanner sc = new Scanner(System.in);
        int ages [] = new int [5];
   
            for (int i=0; i &lt; ages.length;i++){
            System.out.println(&quot;Digite sua idade: &quot;);
            ages [i] = sc.nextInt();
         
            }
            return ages;
        }
 
    static char []sexo (){
    Scanner sc = new Scanner(System.in);
    char genero[] = new char [5];
        for (int i=0; i &lt; genero.length;i++){
        System.out.println(&quot;Digite seu sexo: &quot;);
        genero [i] = sc.next().charAt(0);
   
    }
    return genero;
}
 
 
    static char []hair (){
    Scanner sc = new Scanner(System.in);
    char colorhair[] = new char [5];
        for (int i=0; i &lt; colorhair.length;i++){
        System.out.println(&quot;Digite qual é a cor do seu cabelo: &quot;);
        colorhair [i] = sc.next().charAt(0);
 
        }
        return colorhair;    
}

    static char []eyes (){
    Scanner sc = new Scanner(System.in);
    char coloreyes[] = new char [5];
        for (int i=0; i &lt; coloreyes.length;i++){
        System.out.println(&quot;Digite a cor do seu olho: &quot;);
        coloreyes [i] = sc.next().charAt(0);
 
        }
        return coloreyes;
    }
   
 
    static float Todos (int vetor[], char hair[], char eyes[], char sexo[]){
 
        float contador=0;
 
        for (int i=0; i&lt;vetor.length;i++){
           
            if(hair[i] ==&#39;L&#39; &amp;&amp; eyes[i] == &#39;A&#39; &amp;&amp; sexo[i] == &#39;M&#39; &amp;&amp; (vetor[i]&gt;= 18 ||
vetor[i]&lt;= 35)){
                contador++;
            } 
           
        }
        return  contador;
    }
 
    static float Big (int vetor[]){
 
        int maiorage=0;
 
        for (int i=0; i&lt;vetor.length;i++){
           
            if(vetor[i]&gt; maiorage){
               maiorage = vetor[i];
            }    
        }
 
        return (maiorage);
 
    }
   
    static float habitantes(int vetor[], char hair[], char eyes[]){
 
        float media=0;
        float quantidade=0;
 
        for(int i=0;i&lt;vetor.length;i++) {
           
            if(hair[i]==&#39;P&#39; || eyes[i]==&#39;C&#39;) {
               
                media+=vetor[i];
                quantidade++;
               
            }
           
           
        }
        return (media/quantidade);
 
    }
 
 
   
 
public static void main(String[] args) {
   
            int idade [] = age();
            char sexo []= sexo();
            char cabelos [] = hair();
            char olhos [] = eyes();
           
       
                System.out.println(&quot;A média da idade dos habitantes com olhos castanhos e
cabelos preto é de: &quot;+ habitantes(idade, cabelos, olhos));
               
                System.out.println(&quot;A maior idade entre os habitantes é: &quot;+ Big(idade));
               
                System.out.println(&quot;A quantidade de mulheres entre 18 a 35 anos de olho azul
e cabelo loiro é:  &quot;+Todos(idade, cabelos, olhos, sexo) );
               
                       
     }
}
