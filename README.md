# BGL COMP1






#include <stdio.h>
#include <stdio.h>
#include <math.h>
#define PI 3.14
int main()
{
    int escolha, escolha2, objeto;
    float num, sum, sub, mul, di, elevacao, i,j, raio, altura, base, lado, area, volume;
    double nums;
    char escolha3;
    printf("bem vindo a caluladora de matematica\n");
    printf("digite qual operacao deseja fazer\n");
    printf("1 - soma  2 - subtracao 3 - multiplicacao 4 - divisao 5 - formulas geometricas \n");
    scanf("%d", &escolha);
    
    switch(escolha)
    {
        case 1:
        
            printf("digite os numeros desejados\n");
            scanf("%f" "%f", &i, &j);
            sum= i+j;
            printf("a soma eh %f \n", sum);
        
        break;
        
        case 2:

            printf("digite os numeros desejados\n");
            scanf("%f" "%f", &i, &j );
            sub= i-j;
            printf("a subtracao eh %f \n", sub);
        
        break;
        
        case 3:
        
            printf("digite os numeros desejados\n");
            scanf("%f"  "%f", &i, &j);
            mul= i*j;
            printf("a multiplicacao eh %f \n", mul);
        
        break;
        
        case 4:
        
            printf("digite os numeros desejados\n ");
            scanf("%f"  "%f", &i, &j);
            di= i/j;
            printf("a divisao eh %f \n", di);
        
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
                    sum+=nums;
                }
                printf("perimetro eh %f \n", sum);
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
                printf(" eh um Circulo ou cIlindro?");
                scanf(" %c", &escolha3);
                if(escolha 3 == 'C')
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
            
            else{
                
            }
            
            default :
            printf("essa opcao nao existe\n");
            break;
        }
        break;
        
        default :
        printf("essa opcao nao eh possivel\n");
        break;
    }
    
    
    return 0;
}
