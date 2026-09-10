# BGL COMP1


#include <stdio.h>
#include <stdio.h>
#include <math.h>
#define PI 3.14
int main()
{
    int escolha, escolha2, objeto, D3, faces, qtd;
    float num,operacao, elevacao, i,j, raio, altura, alturaface, base, lado, area, volume, capital, montante, juros, indice, tempo, numero;
    double nums;
    char escolha3;
    printf("bem vindo a caluladora de matematica\n");
    printf("digite qual operacao deseja fazer\n");
    printf("1 - Soma.  2 - Subtracao. 3 - Multiplicacao. 4 - Divisao. 5 - Formulas Geometricas. 6 - Investimento. 7- Equações Complexas. 8 - Funcao \n");
    scanf("%d", &escolha);
    numero=0;
    switch(escolha)
    {
        case 1:
        
            printf("digite quantidade de numeros a somar\n");
            scanf("%d", &qtd);

            for(qtd;qtd >0;qtd--)
                {
                    printf("digite o valor %d\n", qtd);
                    scanf("%f", &numero);
                    operacao+=numero;
                }
           printf("a Soma eh %f \n", operacao);
        
        break;
        
        case 2:

            printf("digite quantidade de numeros a subtrair\n");
            scanf("%d", &qtd);

            for(qtd;qtd >0;qtd--)
                {
                    printf("digite o valor %d\n", qtd);
                    scanf("%f", &numero);
                    operacao-=numero;
                }
           printf("a Subtracao eh %f \n", operacao);
        
        break;
        
        case 3:
        
            printf("digite quantidade de numeros a multiplicar\n");
            scanf("%d", &qtd);

            for(qtd;qtd >0;qtd--)
                {
                    printf("digite o valor %d\n", qtd);
                    scanf("%f", &numero);
                    operacao*=numero;
                }
           printf("a Multiplicacao eh %f \n", operacao);
        
        break;
        
        case 4:
        
            printf("digite quantidade de numeros a dividir\n");
            scanf("%d", &qtd);

            for(qtd;qtd >0;qtd--)
                {
                    printf("digite o valor %d\n", qtd);
                    scanf("%f", &numero);
                    operacao/=numero;
                }
           printf("a Divisao eh %f \n", operacao);
        
        break;
        
        case 5:
        printf(" quantos lados a figura tem \n");
        scanf("%d", &objeto); 
        if(objeto ==1 || objeto ==2)
            {
                printf("apenas possivel em casos complexos, esse progama nao os suporta \n");
                return 0;
            }
        printf(" deseja calcular 1 - perimetro, 2 - area ou 3 - volume? \n");
        scanf("%d", &escolha2); 
        
        switch(escolha2)
        {
            case 1:
            if(objeto ==0)
            {
                printf("digite o raio do circulo \n");
                scanf("%f", &raio);
              double perimetro = 2 *PI *raio;
              printf("circulo tem perimetro de %lf \n", perimetro);
            }
            else
            {
                
                for(objeto; objeto>0;objeto--)
                {
                    printf("digite o valor do lado %d \n", objeto);
                    scanf("%lf", &nums);
                    operacao+=nums;
                }
                printf("perimetro eh %f \n", operacao);
            }
            break;
            
            case 2:
            if(objeto ==0)
            {
                printf("digite o raio do circulo \n");
                scanf("%f", &raio);
                area= (PI*powf(raio,2));
                printf("area eh %f \n", area);
            }
            else if(objeto ==4 )
            {
                printf("digite os lados \n");
                scanf("%f",&lado);
                area = powf(lado,2);
                
                printf("area eh %f \n", area);
            }
            else {
                 printf("digite a base e altura ");
                 scanf("%f %f", &altura, &base);
                 if(objeto!=3){
                 area= objeto*(base*altura)/2;
                 printf("area eh %f \n", area);
                 }
                 else {
                 area= (base*altura)/2;
                 printf("area eh %f \n", area);
                 }
                 }
            
            break;
            
            case 3:
            if(objeto ==0)
            {
                printf(" eh uma Esfera ou Cilindro?");
                scanf(" %c", &escolha3);
                if(escolha3 == 'E')
                {
                printf("digite o raio da esfera");
                scanf("%f", &raio);
                volume = (4.0f / 3.0f)*(PI*powf(raio,3));
                printf("o volume da esfera eh %f", volume);
                }
                else
                {
                    printf("digite o raio da base e a altura");
                    scanf("%f  %f", &raio, &altura);
                    volume = powf(raio,2)*altura*PI;
                }
            }
            
            else if (objeto >0){
                
                printf("digite 1 para piramide e 2 para outras formas");
                scanf("%d", &D3);
                
                if(D3 == 1)
                {
                    printf("digite os lado da base e a altura");
                    scanf("%f  %f", &lado, &altura);
                    volume = (lado*lado*altura)/3;
                    printf("o volume eh : %f", volume);
                }
                
                else
                {
                    printf("digite o numero de faces");
                    scanf("%d", &faces);
                    printf("digite a altura da face e a base");
                    scanf("%f %f ", &alturaface, &lado);
                    printf("digite a altura do poliedro");
                    scanf("%f", &altura);
                    area = (alturaface*lado)/2;
                    volume = (faces*area*altura)/3;
                    printf("volume eh : %f", volume);
                }
                
            }
            
            default :
            printf("essa opcao nao existe\n");
            break;
        }
        break;

        case 6:
        {
        
        }
        break;  

        case 7:
        {
        
        }
        break;  

        case 8:
        {
        
        }
        break;  
        
        
        default :
        printf("essa opcao nao eh possivel\n");
        break;
    }
    
    
    return 0;
}
