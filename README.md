# conversor-de-decimal-para-binario
#include <stdio.h>
#include <math.h>

int
main ()
{
  int decimal, binario = 0, exponencial = 0, n = 0;

  printf ("Digite o numero que vc deseja converter para binario:\n");
  scanf ("%d", &decimal);
  while (decimal >= exponencial)
    {
      n++;
      exponencial = pow (2, n);
    }
  n--;
  while (decimal > 0)
    {
      if ((decimal - pow (2, n) >= 0))
	{
	  binario = binario + pow (10, n);
	  decimal = decimal - pow (2, n);
	  n--;
	}
      else
	{
	  n--;
	}

    }
  printf ("%d", binario);
  return 0;
}
