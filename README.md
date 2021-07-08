# Lista_de_Probabilidade

## 7.1

```{r}
numeros<-rep(c("A","2" , "3", "4", "5", "6", "7", "8", "9", "D", "J", "Q", "K"),4)
```

## 7.2

```{r}
naipes<-c("♥", "♦", "♠", "♣")
```

## 7.3

```{r}
baralho<-paste0(naipes,numeros)
```

## 7.4

```{r}
sorteiaMao<-function(vetor){
  aux<-sample(vetor,5)
  sort(aux)
}
```

## 7.5

```{r}
MaoComAs<-function(vetor){
  str_contains(vetor,"A")
}
```
## 7.6
```{r funcao.mesmo.naipe}
MesmoNaipe <- function(vetor){
  naipes <- substring(vetor, 2, 2)
  resp <- all(naipes == naipes[1])
  return(resp)
}
```

## 7.7
```{r funcao.quatro.ases}
QuatroAses <- function(vetor){
  cartas <- substring(vetor, 1, 1)
  if(sum(cartas == "A") == 4){
    return(TRUE)
  }
  return(FALSE)
}
