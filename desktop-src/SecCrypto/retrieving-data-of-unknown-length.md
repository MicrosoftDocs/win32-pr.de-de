---
description: Viele Funktionen geben eine potenziell große Datenmenge an eine Adresse zurück, die von der Anwendung als einer der Parameter bereitgestellt wird.
ms.assetid: ef99edef-39b2-4d78-9c01-13720215d47f
title: Abrufen von Daten unbekannter Länge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9a71a30e935dd20bee6cce8f6dbc00a3b61478a90f4ea2139d7daaddc6894da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117975014"
---
# <a name="retrieving-data-of-unknown-length"></a>Abrufen von Daten unbekannter Länge

Viele Funktionen geben eine potenziell große Datenmenge an eine Adresse zurück, die von der Anwendung als einer der Parameter bereitgestellt wird. In all diesen Fällen wird der Vorgang auf ähnliche, wenn nicht identische Weise ausgeführt. Der Parameter, der auf die Position der zurückgegebenen Daten zeigt, verwendet die Notationskonvention, wobei pb oder pv die ersten beiden Zeichen des Parameternamens sind. Ein anderer Parameter hat die ersten drei Zeichen des Parameternamens. Dieser Parameter stellt die Größe der Daten in Bytes dar, die an die PB- oder PV-Position zurückgegeben werden. Betrachten Sie beispielsweise die folgende Funktionsspezifikation:

``` syntax
#include <windows.h>

BOOL WINAPI SomeFunction(
  PCCRL_CONTEXT pCrlContext,  // in
  DWORD dwPropId,             // in
  BYTE *pbData,               // out
  DWORD *pcbData              // in/out
);
```

In diesem Beispiel ist *pbData* ein Zeiger auf den Speicherort, an dem die Daten zurückgegeben werden, und *"data"* ist die Größe der zurückgegebenen Daten in Bytes.

> [!Note]  
> Der Begleitparameter zum Parameter "parameters" kann manchmal ein etwas anderes Präfix aufweisen, z. B. p oder pv. Bei Begleitparametern, die die Kombination der Präfixe pwsz und pcch verwenden, ist der pcch-Parameter außerdem die Anzahl der zurückgegebenen Daten in Zeichen [*(Unicode*](../secgloss/u-gly.md) oder [*ASCII,*](../secgloss/a-gly.md)sofern zutreffend).

 

Wenn der durch den *pbData-Parameter* angegebene Puffer nicht groß genug ist, um die zurückgegebenen Daten zu speichern, legt die Funktion den ERROR \_ MORE \_ DATA-Code fest (der durch Aufrufen der [**GetLastError-Funktion**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) sichtbar ist) und speichert die erforderliche Puffergröße in Bytes in der Variablen, auf die *von %%amp;gt;* verweist.

Wenn **NULL** eine Eingabe für *pbData* ist und *"inputsData"* nicht **NULL** ist, wird kein Fehler zurückgegeben, und die Funktion gibt die Größe des benötigten Speicherpuffers in Bytes in der Variablen zurück, auf die *von "data"* verwiesen wird. Dadurch kann eine Anwendung die Größe und die beste Möglichkeit zum Zuordnen eines Puffers für die zurückgegebenen Daten bestimmen.

> [!Note]  
> Wenn **NULL** für *pbData* eingegeben wird, um die Größe zu bestimmen, die erforderlich ist, um sicherzustellen, dass die zurückgegebenen Daten in den angegebenen Puffer passen, verwendet der zweite Aufruf der Funktion, die den Puffer mit den gewünschten Daten auffüllt, möglicherweise nicht den gesamten Puffer. Nach dem zweiten Aufruf ist die tatsächliche Größe der zurückgegebenen Daten in *"pwData"* enthalten. Verwenden Sie diese Größe bei der Verarbeitung der Daten.

 

Das folgende Beispiel zeigt, wie Eingabe- und Ausgabeparameter für diesen Zweck implementiert werden können.


```C++
//-------------------------------------------------------------------
// Copyright (C) Microsoft.  All rights reserved.
#include <stdio.h>
#include <windows.h>
#include <Wincrypt.h>
#define MY_ENCODING_TYPE  (PKCS_7_ASN_ENCODING | X509_ASN_ENCODING)

void MyHandleError(char *s);

void main()
{

// Set up SomeFunction variables.
PCCRL_CONTEXT pCrlContext; // Initialized elsewhere.
DWORD dwPropId;            // Initialized elsewhere.
DWORD cbData;
BYTE  *pbData;

// Call SomeFunction to set cbData, the size of 
// the buffer needed for pbData.
if(SomeFunction(
     pCrlContext, 
     dwPropId, 
     NULL, 
     &cbData))
{
       printf("The function succeeded.\n");
}
else
{

// The function call failed. Handle the error.
       MyHandleError("Function call failed.");
}

// The call succeeded; the size for the needed buffer, in bytes, 
// now resides in cbData.

// Malloc memory for the size of the message.
if(pbData = (BYTE*)malloc(cbData))
{
   printf("Memory has been allocated.\n");
}
else
{

   // The allocation failed. Write an error message and exit.
   MyHandleError("Malloc operation failed. ");
}

// The space for the buffer has been allocated.
// Call SomeFunction to fill the buffer with the data.
if(SomeFunction(
      pCrlContext, 
      dwPropId, 
      pbData, 
      &cbData))
{
       printf("The function succeeded.\n");
}
else
{

   // The second function call failed. Handle the error.
   MyHandleError("The second call to the function failed.");
}

// The function succeeded; the data is now in the buffer
// pointed to by pbData. Note that cbData is
// updated with the actual size of the data returned. Use this size 
// to process bytes of pbData.

// When you have finished using the allocated memory, free it.
free(pbData);

} // End of main

//  This example uses the function MyHandleError, a simple error
//  handling function, to print an error message to the 
//  standard error (stderr) file and exit the program. 
//  For most applications, replace this function with one 
//  that does more extensive error reporting.
void MyHandleError(char *s)
{
    fprintf(stderr,"An error occurred in running the program.\n");
    fprintf(stderr,"%s\n",s);
    fprintf(stderr,"Error number %x.\n",GetLastError());
    fprintf(stderr,"Program terminating.\n");
    exit(1);
}
```



 

 
