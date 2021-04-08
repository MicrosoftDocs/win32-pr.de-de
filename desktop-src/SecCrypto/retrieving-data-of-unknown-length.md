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
# <a name="retrieving-data-of-unknown-length"></a><span data-ttu-id="da278-103">Abrufen von Daten mit unbekannter Länge</span><span class="sxs-lookup"><span data-stu-id="da278-103">Retrieving Data of Unknown Length</span></span>

<span data-ttu-id="da278-104">Viele Funktionen geben eine potenziell große Datenmenge an eine Adresse zurück, die von der Anwendung als einer der Parameter bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="da278-104">Many functions return a potentially large amount of data to an address provided as one of the parameters by the application.</span></span> <span data-ttu-id="da278-105">In all diesen Fällen wird der Vorgang in einer ähnlichen, nicht identischen Weise ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="da278-105">In all these cases, the operation is performed in a similar, if not identical, fashion.</span></span> <span data-ttu-id="da278-106">Der-Parameter, der auf den Speicherort der zurückgegebenen Daten zeigt, verwendet die Notation-Konvention, bei der PB oder PV die ersten beiden Zeichen des Parameter namens sind.</span><span class="sxs-lookup"><span data-stu-id="da278-106">The parameter that points to the location of the returned data will use the notation convention where pb or pv are the first two characters of the parameter name.</span></span> <span data-ttu-id="da278-107">Ein anderer Parameter verfügt über eine Platine als die ersten drei Zeichen des Parameter namens.</span><span class="sxs-lookup"><span data-stu-id="da278-107">Another parameter will have pcb as the first three characters of the parameter name.</span></span> <span data-ttu-id="da278-108">Dieser Parameter stellt die Größe (in Bytes) der Daten dar, die an den PB-oder PV-Speicherort zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="da278-108">This parameter represents the size, in bytes, of the data that will be returned to the pb or pv location.</span></span> <span data-ttu-id="da278-109">Sehen Sie sich beispielsweise die folgende Funktionsspezifikation an:</span><span class="sxs-lookup"><span data-stu-id="da278-109">For example, consider the following function specification:</span></span>

``` syntax
#include <windows.h>

BOOL WINAPI SomeFunction(
  PCCRL_CONTEXT pCrlContext,  // in
  DWORD dwPropId,             // in
  BYTE *pbData,               // out
  DWORD *pcbData              // in/out
);
```

<span data-ttu-id="da278-110">In diesem Beispiel ist *pbData* ein Zeiger auf den Speicherort, an den die Daten zurückgegeben werden, und *pcbData* ist die Größe (in Bytes) der zurückgegebenen Daten.</span><span class="sxs-lookup"><span data-stu-id="da278-110">In this example, *pbData* is a pointer to the location where the data will be returned, and *pcbData* is the size, in bytes, of the returned data.</span></span>

> [!Note]  
> <span data-ttu-id="da278-111">Der Parameter "Companion" für den "PCB"-Parameter kann manchmal ein etwas anderes Präfix enthalten, z. b. p oder PV.</span><span class="sxs-lookup"><span data-stu-id="da278-111">The companion parameter to the pcb parameter may sometimes carry a slightly different prefix, such as p or pv.</span></span> <span data-ttu-id="da278-112">Für Begleit Parameter, die die Kombination von Präfixen Pwsz und pcch verwenden, entspricht der pcch-Parameter außerdem der Anzahl der zurückgegebenen Daten (in Zeichen ([*Unicode*](../secgloss/u-gly.md) oder [*ASCII*](../secgloss/a-gly.md), sofern zutreffend).</span><span class="sxs-lookup"><span data-stu-id="da278-112">Also, for companion parameters using the combination of prefixes pwsz and pcch, the pcch parameter is the count, in characters ([*Unicode*](../secgloss/u-gly.md) or [*ASCII*](../secgloss/a-gly.md), as applicable), of the returned data.</span></span>

 

<span data-ttu-id="da278-113">Wenn der durch den *pbData* -Parameter angegebene Puffer nicht groß genug ist, um die zurückgegebenen Daten aufzunehmen, legt die Funktion den Fehler \_ weiteren \_ Datencode fest (der durch Aufrufen der [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) -Funktion angezeigt werden kann) und speichert die erforderliche Puffergröße in Bytes in der Variablen, auf die von *pcbData* verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="da278-113">If the buffer specified by the *pbData* parameter is not large enough to hold the returned data, the function sets the ERROR\_MORE\_DATA code (which can be seen by calling the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function) and stores the required buffer size, in bytes, in the variable pointed to by *pcbData*.</span></span>

<span data-ttu-id="da278-114">Wenn **null** für *pbData* und *pcbData* nicht **null** ist, wird kein Fehler zurückgegeben, und die Funktion gibt die Größe (in Bytes) des benötigten Speicherpuffers in der Variablen zurück, auf die von *pcbData* verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="da278-114">If **NULL** is input for *pbData* and *pcbData* is not **NULL**, no error is returned, and the function returns the size, in bytes, of the needed memory buffer in the variable pointed to by *pcbData*.</span></span> <span data-ttu-id="da278-115">Dadurch kann eine Anwendung die Größe von und die beste Zuordnungs Methode zum Zuordnen eines Puffers für die zurückgegebenen Daten bestimmen.</span><span class="sxs-lookup"><span data-stu-id="da278-115">This lets an application determine the size of, and the best way to allocate, a buffer for the returned data.</span></span>

> [!Note]  
> <span data-ttu-id="da278-116">Wenn **null** für *pbData verwendet* wird, um die erforderliche Größe zu ermitteln, um sicherzustellen, dass die zurückgegebenen Daten in den angegebenen Puffer passen, kann der zweite aufrufungs Vorgang, der den Puffer mit den gewünschten Daten füllt, nicht den gesamten Puffer verwenden.</span><span class="sxs-lookup"><span data-stu-id="da278-116">When **NULL** is input for *pbData* to determine the size needed to ensure that the returned data fits in the specified buffer, the second call to the function which populates the buffer with the desired data may not use the whole buffer.</span></span> <span data-ttu-id="da278-117">Nach dem zweiten-Befehl ist die tatsächliche Größe der zurückgegebenen Daten in *pcbData* enthalten.</span><span class="sxs-lookup"><span data-stu-id="da278-117">After the second call, the actual size of the data returned is contained in *pcbData*.</span></span> <span data-ttu-id="da278-118">Verwenden Sie diese Größe, wenn Sie die Daten verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="da278-118">Use this size when processing the data.</span></span>

 

<span data-ttu-id="da278-119">Das folgende Beispiel zeigt, wie Eingabe-und Ausgabeparameter zu diesem Zweck implementiert werden können.</span><span class="sxs-lookup"><span data-stu-id="da278-119">The following example shows how input and output parameters might be implemented for this purpose.</span></span>


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



 

 
