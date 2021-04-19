---
description: Listet die auf einem Computer verfügbaren CSPs mithilfe von CryptoAPI auf.
ms.assetid: 10a5210d-7992-4832-9435-67ac2b851a97
title: 'Beispiel-C-Programm: Auflisten von CSP-Anbietern und-Anbieter Typen'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a109aab8bbf3788bd539d078f00f7a28926f98de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356662"
---
# <a name="example-c-program-enumerating-csp-providers-and-provider-types"></a><span data-ttu-id="e8d17-103">Beispiel-C-Programm: Auflisten von CSP-Anbietern und-Anbieter Typen</span><span class="sxs-lookup"><span data-stu-id="e8d17-103">Example C Program: Enumerating CSP Providers and Provider Types</span></span>

<span data-ttu-id="e8d17-104">Im folgenden Beispiel werden die auf einem Computer verfügbaren CSPs aufgelistet und die folgenden [*CryptoAPI*](../secgloss/c-gly.md) -Funktionen verwendet:</span><span class="sxs-lookup"><span data-stu-id="e8d17-104">The following example lists the CSPs available on a computer and uses the following [*CryptoAPI*](../secgloss/c-gly.md) functions:</span></span>

-   [<span data-ttu-id="e8d17-105">**Cryptenum providertypes**</span><span class="sxs-lookup"><span data-stu-id="e8d17-105">**CryptEnumProviderTypes**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptenumprovidertypesa)
-   [<span data-ttu-id="e8d17-106">**Cryptenum Providers**</span><span class="sxs-lookup"><span data-stu-id="e8d17-106">**CryptEnumProviders**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptenumprovidersa)
-   [<span data-ttu-id="e8d17-107">**Cryptgetdefaultprovider**</span><span class="sxs-lookup"><span data-stu-id="e8d17-107">**CryptGetDefaultProvider**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetdefaultprovidera)
-   [<span data-ttu-id="e8d17-108">**CryptGetProvParam**</span><span class="sxs-lookup"><span data-stu-id="e8d17-108">**CryptGetProvParam**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam)

<span data-ttu-id="e8d17-109">In diesem Beispiel wird die Funktion " [**myhanderror**](myhandleerror.md)" verwendet.</span><span class="sxs-lookup"><span data-stu-id="e8d17-109">This example uses the function [**MyHandleError**](myhandleerror.md).</span></span> <span data-ttu-id="e8d17-110">Der Code für diese Funktion ist in diesem Beispiel enthalten.</span><span class="sxs-lookup"><span data-stu-id="e8d17-110">The code for this function is included in this example.</span></span> <span data-ttu-id="e8d17-111">Der Code für dieses und andere Hilfsfunktionen ist auch unter [universell Funktionen](general-purpose-functions.md)aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="e8d17-111">Code for this and other auxiliary functions is also listed under [General Purpose Functions](general-purpose-functions.md).</span></span>

<span data-ttu-id="e8d17-112">Im folgenden Beispiel werden die Aufzählung von CSPs und Anbieter Typen veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="e8d17-112">The following example shows enumerating CSPs and provider types.</span></span>


```C++
//-------------------------------------------------------------------
// Copyright (C) Microsoft.  All rights reserved.
#pragma comment(lib, "crypt32.lib")

#include <stdio.h>
#include <tchar.h>
#include <windows.h>
#include <wincrypt.h>

void MyHandleError(TCHAR* s);
void Wait(TCHAR* s);

int _tmain(int argc, _TCHAR* argv[])
{
    // Declare and initialize variables.
    HCRYPTPROV hProv;
    LPTSTR pszName;
    DWORD dwType;
    DWORD cbName;
    DWORD dwIndex = 0;
    BYTE* ptr;
    ALG_ID aiAlgid;
    DWORD dwBits;
    DWORD dwNameLen;
    CHAR szName[100];
    BYTE pbData[1024];
    DWORD cbData = 1024;
    DWORD dwIncrement = sizeof(DWORD);
    DWORD dwFlags = CRYPT_FIRST;
    DWORD dwParam = PP_CLIENT_HWND;
    CHAR* pszAlgType = NULL;
    BOOL fMore = TRUE;
    LPTSTR pbProvName;
    DWORD cbProvName;

    //--------------------------------------------------------------
    // Print header lines for provider types.
    _tprintf(TEXT("Listing Available Provider Types.\n"));
    _tprintf(TEXT("Provider type    Provider Type Name\n"));
    _tprintf(TEXT("_____________    ")
        TEXT("_____________________________________\n"));

    // Loop through enumerating provider types.
    dwIndex = 0;
    while(CryptEnumProviderTypes(
        dwIndex,
        NULL,
        0,
        &dwType,
        NULL,
        &cbName))
    {
        //-----------------------------------------------------------
        // cbName is the length of the name of the next provider 
        // type.

        // Allocate memory in a buffer to retrieve that name.
        if (!(pszName = (LPTSTR)LocalAlloc(LMEM_ZEROINIT, cbName)))
        {
           MyHandleError(TEXT("ERROR - LocalAlloc failed!"));
        }

        //-----------------------------------------------------------
        // Get the provider type name.
        if (CryptEnumProviderTypes(
            dwIndex++,
            NULL,
            NULL,
            &dwType,   
            pszName,
            &cbName))     
        {
            _tprintf (TEXT("     %4.0d        %s\n"), 
                dwType, 
                pszName);
        }
        else
        {
            MyHandleError(TEXT("ERROR - CryptEnumProviders"));
        }

        LocalFree(pszName);
    }

    //--------------------------------------------------------------
    // Print header lines for providers.
    _tprintf(TEXT("\n\nListing Available Providers.\n"));
    _tprintf(TEXT("Provider type    Provider Name\n"));
    _tprintf(TEXT("_____________    ")
        TEXT("_____________________________________\n"));

    //---------------------------------------------------------------
    // Loop through enumerating providers.
    dwIndex = 0;
    while(CryptEnumProviders(
        dwIndex,
        NULL,
        0,
        &dwType,
        NULL,
        &cbName))
    {
        //-----------------------------------------------------------
        // cbName is the length of the name of the next provider.
        // Allocate memory in a buffer to retrieve that name.
        if (!(pszName = (LPTSTR)LocalAlloc(LMEM_ZEROINIT, cbName)))
        {
           MyHandleError(TEXT("ERROR - LocalAlloc failed!"));
        }

        //-----------------------------------------------------------
        // Get the provider name.
        if (CryptEnumProviders(
            dwIndex++,
            NULL,
            0,
            &dwType,
            pszName,
            &cbName))
        {
            _tprintf (TEXT("     %4.0d        %s\n"), 
                dwType, 
                pszName);
        }
        else
        {
            MyHandleError(TEXT("ERROR - CryptEnumProviders"));
        }

        LocalFree(pszName);
    } // End while loop.

    //---------------------------------------------------------------
    // Get the name of the default CSP specified for the 
    // PROV_RSA_FULL type for the computer.

    //---------------------------------------------------------------
    // Get the length of the RSA_FULL default provider name.
    if (!(CryptGetDefaultProvider(
        PROV_RSA_FULL, 
        NULL, 
        CRYPT_MACHINE_DEFAULT,
        NULL, 
        &cbProvName))) 
    { 
       MyHandleError(TEXT("Error getting the length of the ")
           TEXT("default provider name."));
    }

    //---------------------------------------------------------------
    // Allocate local memory for the name of the default provider.
    if (!(pbProvName = (LPTSTR)LocalAlloc(
        LMEM_ZEROINIT, 
        cbProvName)))
    {
        MyHandleError(TEXT("Error during memory allocation ")
            TEXT("for provider name."));
    }

    //---------------------------------------------------------------
    // Get the name of the default PROV_RSA_FULL provider.
    if (CryptGetDefaultProvider(
        PROV_RSA_FULL, 
        NULL, 
        CRYPT_MACHINE_DEFAULT,
        pbProvName,
        &cbProvName)) 
    {
        _tprintf(TEXT("\nThe default provider name is \"%s\"\n"), 
            pbProvName);
    }
    else
    {
        MyHandleError(TEXT("Getting the provider name failed."));
    }

    LocalFree(pbProvName);

    //-----------------------------------------------------
    //  Acquire a cryptographic context.
    if(!CryptAcquireContext(
        &hProv, 
        NULL,
        NULL,
        PROV_RSA_FULL, 
        NULL))  
    {
        MyHandleError(TEXT("Error during CryptAcquireContext!"));
    }

    //------------------------------------------------------
    // Enumerate the supported algorithms.

    //------------------------------------------------------
    // Print header for algorithm information table.
    _tprintf(TEXT("\nEnumerating the supported ")
        TEXT("algorithms\n\n"));
    _tprintf(TEXT("     Algid      Bits      Type        ")
        TEXT("Name         Algorithm\n"));
    _tprintf(TEXT("                                     Length")
        TEXT("          Name\n"));
    _tprintf(TEXT("    _______________________________________")
        TEXT("_________________\n"));
    while(fMore)
    {
        //------------------------------------------------------
        // Retrieve information about an algorithm.
        if(CryptGetProvParam(
            hProv, 
            PP_ENUMALGS, 
            pbData, 
            &cbData, 
            dwFlags))
        {       
            //-------------------------------------------------------
            // Extract algorithm information from the pbData buffer.
           dwFlags = 0;
           ptr = pbData;
           aiAlgid = *(ALG_ID *)ptr;
           ptr += sizeof(ALG_ID);
           dwBits = *(DWORD *)ptr;
           ptr += dwIncrement;
           dwNameLen = *(DWORD *)ptr;
           ptr += dwIncrement;
           strncpy_s(szName,(char *) ptr, sizeof(szName), dwNameLen);
           
            //-------------------------------------------------------
            // Determine the algorithm type.
           switch(GET_ALG_CLASS(aiAlgid)) 
           {
           case ALG_CLASS_DATA_ENCRYPT: 
               pszAlgType = "Encrypt  ";
               break;
            
            case ALG_CLASS_HASH:         
                pszAlgType = "Hash     ";
                break;

            case ALG_CLASS_KEY_EXCHANGE: 
                pszAlgType = "Exchange ";
                break;

            case ALG_CLASS_SIGNATURE:    
                pszAlgType = "Signature";
                break;

            default:
                pszAlgType = "Unknown  ";
                break;
           }

           //--------------------------------------------------------
            // Print information about the algorithm.
            printf("    %8.8xh    %-4d    %s     %-2d          %s\n",
                aiAlgid, 
                dwBits, 
                pszAlgType, 
                dwNameLen, 
                szName);
        }
        else
        {
            fMore = FALSE;
        }
    }

    Wait(TEXT("\nPress Enter to continue."));

    if(!(CryptReleaseContext(hProv, 0)))
    {
        MyHandleError(TEXT("Error during CryptReleaseContext.")); 
    }

    if(GetLastError() == ERROR_NO_MORE_ITEMS)
    { 
       _tprintf(TEXT("\nThe program completed without error.\n"));
    }
    else
    { 
       MyHandleError(TEXT("Error reading algorithm!"));
    }

} // End main.

//-------------------------------------------------------------------
//  This example uses the function MyHandleError, a simple error
//  handling function, to print an error message and exit 
//  the program. 
//  For most applications, replace this function with one 
//  that does more extensive error reporting.

void MyHandleError(TCHAR *s)
{
    _tprintf(TEXT("An error occurred in running the program.\n"));
    _tprintf(TEXT("%s\n"),s);
    _tprintf(TEXT("Error number %x\n."), GetLastError());
    _tprintf(TEXT("Program terminating.\n"));
    exit(1);
}

void Wait(TCHAR *s)
{
    char x;
    _tprintf(s);
    x = getchar();
}

```



 

 
