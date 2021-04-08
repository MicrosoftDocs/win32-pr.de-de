---
description: Im folgenden Beispiel wird ein zufälliger Sitzungsschlüssel erstellt, einige Standardparameter dieses Schlüssels abgerufen und ausgegeben, ein neuer Parameter für den ursprünglichen Schlüssel festgelegt, und anschließend wird der Wert dieses neuen Parameters abgerufen und ausgegeben.
ms.assetid: 00f93036-05c9-4585-842a-a42a7faea2a5
title: 'Beispiel-C-Programm: festlegen und erhalten von Sitzungsschlüssel Parametern'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6be59b8b47c5becd8576a409d659f99d97b7ee3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866655"
---
# <a name="example-c-program-setting-and-getting-session-key-parameters"></a><span data-ttu-id="35880-103">Beispiel-C-Programm: festlegen und erhalten von Sitzungsschlüssel Parametern</span><span class="sxs-lookup"><span data-stu-id="35880-103">Example C Program: Setting and Getting Session Key Parameters</span></span>

<span data-ttu-id="35880-104">Im folgenden Beispiel wird ein zufälliger Sitzungsschlüssel erstellt, einige Standardparameter dieses Schlüssels abgerufen und ausgegeben, ein neuer Parameter für den ursprünglichen Schlüssel festgelegt, und anschließend wird der Wert dieses neuen Parameters abgerufen und ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="35880-104">The following example creates a random session key, gets and prints some default parameters of that key, sets a new parameters on the original key, then gets and prints the value of that new parameter.</span></span> <span data-ttu-id="35880-105">Er wird bereinigt, indem der Sitzungsschlüssel zerstört und der Kryptografiekontext freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="35880-105">It cleans up by destroying the session key and releasing the cryptographic context.</span></span>

<span data-ttu-id="35880-106">In diesem Beispiel wird die Verwendung der folgenden Aufgaben und Funktionen veranschaulicht:</span><span class="sxs-lookup"><span data-stu-id="35880-106">This example illustrates the use of the following tasks and functions:</span></span>

-   <span data-ttu-id="35880-107">Zugreifen auf einen CSP mithilfe von [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta).</span><span class="sxs-lookup"><span data-stu-id="35880-107">Accessing a CSP using [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta).</span></span>
-   <span data-ttu-id="35880-108">Einreichen eines Puffers mit zufälligen Bytes mithilfe von [**cryptgenrandom**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenrandom).</span><span class="sxs-lookup"><span data-stu-id="35880-108">Filing a buffer with random bytes using [**CryptGenRandom**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenrandom).</span></span>
-   <span data-ttu-id="35880-109">Erstellen eines Sitzungsschlüssels mithilfe von [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey).</span><span class="sxs-lookup"><span data-stu-id="35880-109">Creating a session key using [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey).</span></span>
-   <span data-ttu-id="35880-110">Der Wert von Schlüsselparametern wird mithilfe von " [**cryptgetkeyparam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetkeyparam)" abgerufen.</span><span class="sxs-lookup"><span data-stu-id="35880-110">Getting the value of key parameters using [**CryptGetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetkeyparam).</span></span>
-   <span data-ttu-id="35880-111">Verwenden von [**cryptsetkeyparam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) , um den Schlüssel Generierungsprozess zu ändern.</span><span class="sxs-lookup"><span data-stu-id="35880-111">Using [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) to alter the key generation process.</span></span>
-   <span data-ttu-id="35880-112">Zerstören der Schlüssel mithilfe von [**cryptdestroykey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey).</span><span class="sxs-lookup"><span data-stu-id="35880-112">Destroying the keys using [**CryptDestroyKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey).</span></span>
-   <span data-ttu-id="35880-113">Freigeben des CSP mit [**cryptreleasecontext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptreleasecontext).</span><span class="sxs-lookup"><span data-stu-id="35880-113">Releasing the CSP with [**CryptReleaseContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptreleasecontext).</span></span>

<span data-ttu-id="35880-114">In diesem Beispiel wird die Funktion " [**myhanderror**](myhandleerror.md)" verwendet.</span><span class="sxs-lookup"><span data-stu-id="35880-114">This example uses the function [**MyHandleError**](myhandleerror.md).</span></span> <span data-ttu-id="35880-115">Der Code für diese Funktion ist im Beispiel enthalten.</span><span class="sxs-lookup"><span data-stu-id="35880-115">The code for this function is included with the sample.</span></span> <span data-ttu-id="35880-116">Der Code für dieses und andere Hilfsfunktionen ist auch unter [universell Funktionen](general-purpose-functions.md)aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="35880-116">Code for this and other auxiliary functions is also listed under [General Purpose Functions](general-purpose-functions.md).</span></span>


```C++
//-------------------------------------------------------------------
// Copyright (C) Microsoft.  All rights reserved.

#include <windows.h>
#include <wincrypt.h>
#include <stdio.h>
#include <tchar.h>

// Link with the Crypt32.lib file.
#pragma comment (lib, "Crypt32")

void MyHandleError(PCTSTR psz);

void main()
{
    HCRYPTPROV hProv;
    HCRYPTKEY hKey;
    DWORD dwMode;
    BYTE pbData[16];
    BYTE pbRandomData[8];
    DWORD dwCount;
    DWORD i;

    // Acquire a cryptographic provider context handle.
    if(!CryptAcquireContext(
        &hProv, 
        NULL, 
        NULL, 
        PROV_RSA_FULL, 
        0)) 
    {
        MyHandleError(TEXT("Error during CryptAcquireContext."));
    }

    //  Generate eight bytes of random data into pbRandomData.
    if( CryptGenRandom(
            hProv,
            8,
            pbRandomData))
    {
        _tprintf(TEXT("Eight bytes of random data have been generated.\n"));
    }
    else
    {
        MyHandleError(TEXT("Random bytes were not correctly generated."));
    }

    // Create a random block cipher session key.
    if(!CryptGenKey(
            hProv, 
            CALG_RC4, 
            CRYPT_EXPORTABLE, 
            &hKey)) 
    {
        MyHandleError(TEXT("Error during CryptGenKey."));
    }

    // Read the cipher mode.
    dwCount = sizeof(DWORD);
    if(CryptGetKeyParam(
        hKey, 
        KP_MODE, 
        (PBYTE)&dwMode, 
        &dwCount, 
        0))
    {
        // Print the cipher mode.
        _tprintf(TEXT("Default cipher mode: %d\n"), dwMode);
    }
    else
    {
        MyHandleError(TEXT("Error during CryptGetKeyParam."));
    }

    // Read the initialization vector.

    //  Get the length of the initialization vector.
    if(!CryptGetKeyParam(
        hKey, 
        KP_IV, 
        NULL,     
        &dwCount, 
        0)) 
    {
        MyHandleError(TEXT("Error getting the IV length"));
    }

    // Get the initialization vector, itself.
    if(CryptGetKeyParam(
        hKey, 
        KP_IV, 
        pbData, 
        &dwCount, 
        0))
    {
        // Print the initialization vector.
        _tprintf(TEXT("Default IV:"));
        for(i = 0; i < dwCount; i++) 
        {
            _tprintf(TEXT("%2.2x "),pbData[i]);
        }

        _tprintf(TEXT("\n"));
    }
    else
    {
        MyHandleError(TEXT("Error getting the IV."));
    }

    //  Reset the initialization vector.
    if(CryptSetKeyParam(
        hKey,
        KP_IV,
        pbRandomData,
        0))
    {
        _tprintf(TEXT("New initialization vector is set.\n"));
    }
    else
    {
        MyHandleError(TEXT("The new IV was not set."));
    }

    // Read the new initialization vector.

    //  Get the length of the new initialization vector.
    if(!CryptGetKeyParam(
        hKey, 
        KP_IV, 
        NULL,     
        &dwCount, 
        0)) 
    {
        MyHandleError(TEXT("Error getting the IV length"));
    }

    // Get the initialization vector, itself.
    if(CryptGetKeyParam(
        hKey, 
        KP_IV, 
        pbData, 
        &dwCount, 
        0))
    {
        // Print the initialization vector.
        _tprintf(TEXT("RE-set IV:"));
        for(i = 0; i < dwCount; i++) 
        {
            _tprintf(TEXT("%2.2x "),pbData[i]);
        }
        
        _tprintf(TEXT("\n"));
    }
    else
    {
        MyHandleError(TEXT("Error getting the IV."));
    }

    //  Clean up.

    //  Destroy the session key.
    if(hKey)
    { 
        CryptDestroyKey(hKey);
    }

    // Release the provider handle.
    if(hProv)
    { 
        CryptReleaseContext(hProv, 0);
    }
} // End of main.

//-------------------------------------------------------------------
//    This example uses the function MyHandleError, a simple error
//    handling function, to print an error message to the standard  
//    error (stderr) file and exit the program. 
//    For most applications, replace this function with one 
//    that does more extensive error reporting.

void MyHandleError(PTSTR psz)
{
    _ftprintf(stderr, TEXT("An error occurred in the program. \n"));
    _ftprintf(stderr, TEXT("%s\n"), psz);
    _ftprintf(stderr, TEXT("Error number %x.\n"), GetLastError());
    _ftprintf(stderr, TEXT("Program terminating. \n"));
    exit(1);
} // End of MyHandleError.
```



 

 



