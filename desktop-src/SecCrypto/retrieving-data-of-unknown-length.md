---
description: Viele Funktionen geben eine potenziell große Datenmenge an eine Adresse zurück, die von der Anwendung als einer der Parameter bereitgestellt wird.
ms.assetid: ef99edef-39b2-4d78-9c01-13720215d47f
title: Abrufen von Daten mit unbekannter Länge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd30620018f3c4871bd27299c3dd21ae42936c51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863863"
---
# <a name="retrieving-data-of-unknown-length"></a>Abrufen von Daten mit unbekannter Länge

Viele Funktionen geben eine potenziell große Datenmenge an eine Adresse zurück, die von der Anwendung als einer der Parameter bereitgestellt wird. In all diesen Fällen wird der Vorgang in einer ähnlichen, nicht identischen Weise ausgeführt. Der-Parameter, der auf den Speicherort der zurückgegebenen Daten zeigt, verwendet die Notation-Konvention, bei der PB oder PV die ersten beiden Zeichen des Parameter namens sind. Ein anderer Parameter verfügt über eine Platine als die ersten drei Zeichen des Parameter namens. Dieser Parameter stellt die Größe (in Bytes) der Daten dar, die an den PB-oder PV-Speicherort zurückgegeben werden. Sehen Sie sich beispielsweise die folgende Funktionsspezifikation an:

``` syntax
#include <windows.h>

BOOL WINAPI SomeFunction(
  PCCRL_CONTEXT pCrlContext,  // in
  DWORD dwPropId,             // in
  BYTE *pbData,               // out
  DWORD *pcbData              // in/out
);
```

In diesem Beispiel ist *pbData* ein Zeiger auf den Speicherort, an den die Daten zurückgegeben werden, und *pcbData* ist die Größe (in Bytes) der zurückgegebenen Daten.

> [!Note]  
> Der Parameter "Companion" für den "PCB"-Parameter kann manchmal ein etwas anderes Präfix enthalten, z. b. p oder PV. Für Begleit Parameter, die die Kombination von Präfixen Pwsz und pcch verwenden, entspricht der pcch-Parameter außerdem der Anzahl der zurückgegebenen Daten (in Zeichen ([*Unicode*](../secgloss/u-gly.md) oder [*ASCII*](../secgloss/a-gly.md), sofern zutreffend).

 

Wenn der durch den *pbData* -Parameter angegebene Puffer nicht groß genug ist, um die zurückgegebenen Daten aufzunehmen, legt die Funktion den Fehler \_ weiteren \_ Datencode fest (der durch Aufrufen der [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) -Funktion angezeigt werden kann) und speichert die erforderliche Puffergröße in Bytes in der Variablen, auf die von *pcbData* verwiesen wird.

Wenn **null** für *pbData* und *pcbData* nicht **null** ist, wird kein Fehler zurückgegeben, und die Funktion gibt die Größe (in Bytes) des benötigten Speicherpuffers in der Variablen zurück, auf die von *pcbData* verwiesen wird. Dadurch kann eine Anwendung die Größe von und die beste Zuordnungs Methode zum Zuordnen eines Puffers für die zurückgegebenen Daten bestimmen.

> [!Note]  
> Wenn **null** für *pbData verwendet* wird, um die erforderliche Größe zu ermitteln, um sicherzustellen, dass die zurückgegebenen Daten in den angegebenen Puffer passen, kann der zweite aufrufungs Vorgang, der den Puffer mit den gewünschten Daten füllt, nicht den gesamten Puffer verwenden. Nach dem zweiten-Befehl ist die tatsächliche Größe der zurückgegebenen Daten in *pcbData* enthalten. Verwenden Sie diese Größe, wenn Sie die Daten verarbeiten.

 

Das folgende Beispiel zeigt, wie Eingabe-und Ausgabeparameter zu diesem Zweck implementiert werden können.


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



 

 
