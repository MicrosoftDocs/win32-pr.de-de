---
description: Veranschaulicht verschiedene Möglichkeiten, den CryptAcquireContext und verwandte kryptoapi-Funktionen für die Arbeit mit einem Kryptografiedienstanbieter (kryptografischen Service Provider, CSP) und einem Schlüssel Container zu verwenden.
ms.assetid: e8d2503c-a38f-44f6-a653-ae9c7bf903bd
title: 'Beispiel-C-Programm: Verwenden von CryptAcquireContext'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 074d1967d8a32001e620b089280c034887b90cd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749569"
---
# <a name="example-c-program-using-cryptacquirecontext"></a>Beispiel-C-Programm: Verwenden von CryptAcquireContext

Im folgenden Beispiel werden verschiedene Möglichkeiten veranschaulicht, den [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) und zugehörige CryptoAPI-Funktionen zum Arbeiten mit einem [*Kryptografiedienstanbieter (kryptografischen Service Provider*](../secgloss/c-gly.md) , CSP) und einem [*Schlüssel Container*](../secgloss/k-gly.md)zu verwenden.

In diesem Beispiel werden die folgenden Aufgaben und kryptoapi-Funktionen veranschaulicht:

-   Verwenden Sie die [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) -Funktion, um ein Handle für den Standard-CSP und den Standardschlüssel Container abzurufen. Wenn kein Standardschlüssel Container vorhanden ist, verwenden Sie die **CryptAcquireContext** -Funktion, um den Standardschlüssel Container zu erstellen.
-   Verwenden Sie die Funktion " [**CryptGetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) " zum Abrufen von Informationen zu einem CSP und einem Schlüssel Container.
-   Erhöhen Sie den [*Verweis Zähler*](../secgloss/r-gly.md) für den Anbieter mithilfe der [**cryptcontextadressf**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcontextaddref) -Funktion.
-   Geben Sie einen CSP mithilfe der [**cryptreleasecontext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptreleasecontext) -Funktion frei.
-   Erstellen Sie einen benannten Schlüssel Container mithilfe der [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) -Funktion.
-   Abrufen eines Handles für einen CSP mithilfe des neu erstellten Schlüssel Containers.
-   Löschen Sie einen Schlüssel Container mithilfe der [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) -Funktion.

In diesem Beispiel wird die Funktion " [**myhanderror**](myhandleerror.md)" verwendet. Der Code für diese Funktion ist im Beispiel enthalten. Der Code für dieses und andere Hilfsfunktionen ist auch unter [universell Funktionen](general-purpose-functions.md)aufgeführt.


```C++
//-------------------------------------------------------------------
//  Copyright (C) Microsoft.  All rights reserved.
//  Example code using CryptAcquireContext.
#pragma comment(lib, "crypt32.lib")

#include <stdio.h>
#include <tchar.h>
#include <windows.h>
#include <Wincrypt.h>

//-------------------------------------------------------------------
// This example uses the function MyHandleError, a simple error
// handling function to print an error message and exit 
// the program. 
// For most applications, replace this function with one 
// that does more extensive error reporting.

void MyHandleError(LPTSTR psz)
{
    _ftprintf(stderr, TEXT("An error occurred in the program. \n"));
    _ftprintf(stderr, TEXT("%s\n"), psz);
    _ftprintf(stderr, TEXT("Error number %x.\n"), GetLastError());
    _ftprintf(stderr, TEXT("Program terminating. \n"));
    exit(1);
} // End of MyHandleError.

void main(void)
{
    //---------------------------------------------------------------
    // Declare and initialize variables.
    HCRYPTPROV hCryptProv;

    //---------------------------------------------------------------
    // Get a handle to the default PROV_RSA_FULL provider.
    if(CryptAcquireContext(
        &hCryptProv, 
        NULL, 
        NULL, 
        PROV_RSA_FULL, 
        0)) 
    {
        _tprintf(TEXT("CryptAcquireContext succeeded.\n"));
    }
    else
    {
        if (GetLastError() == NTE_BAD_KEYSET)
        {
            // No default container was found. Attempt to create it.
            if(CryptAcquireContext(
                &hCryptProv, 
                NULL, 
                NULL, 
                PROV_RSA_FULL, 
                CRYPT_NEWKEYSET)) 
            {
                _tprintf(TEXT("CryptAcquireContext succeeded.\n"));
            }
            else
            {
                MyHandleError(TEXT("Could not create the default ")
                    TEXT("key container.\n"));
            }
        }
        else
        {
            MyHandleError(TEXT("A general error running ")
                TEXT("CryptAcquireContext."));
        }
    }

    CHAR pszName[1000];
    DWORD cbName;

    //---------------------------------------------------------------
    // Read the name of the CSP.
    cbName = 1000;
    if(CryptGetProvParam(
        hCryptProv, 
        PP_NAME, 
        (BYTE*)pszName, 
        &cbName, 
        0))
    {
        _tprintf(TEXT("CryptGetProvParam succeeded.\n"));
        printf("Provider name: %s\n", pszName);
    }
    else
    {
        MyHandleError(TEXT("Error reading CSP name.\n"));
    }

    //---------------------------------------------------------------
    // Read the name of the key container.
    cbName = 1000;
    if(CryptGetProvParam(
        hCryptProv, 
        PP_CONTAINER, 
        (BYTE*)pszName, 
        &cbName, 
        0))
    {
        _tprintf(TEXT("CryptGetProvParam succeeded.\n"));
        printf("Key Container name: %s\n", pszName);
    }
    else
    {
        MyHandleError(TEXT("Error reading key container name.\n"));
    }
    //---------------------------------------------------------------
    // Perform cryptographic operations.
    //...

    //---------------------------------------------------------------
    //  Add to the reference count on the provider. When the 
    //  reference count on a provider is greater than one,  
    //  CryptReleaseContext reduces the reference count but does not 
    //  free the provider.

    if(CryptContextAddRef(
        hCryptProv, 
        NULL, 
        0)) 
    {
        _tprintf(TEXT("CryptcontextAddRef succeeded.\n"));
    }
    else
    {
        MyHandleError(TEXT("Error during CryptContextAddRef!\n"));
    }

    //---------------------------------------------------------------
    //  The reference count on hCryptProv is now greater than one. 
    //  The first call to CryptReleaseContext will not release the 
    //  provider handle. 

    //---------------------------------------------------------------
    //  Release the context once.
    if (CryptReleaseContext(hCryptProv, 0))
    {
        _tprintf(TEXT("The first call to CryptReleaseContext ")
            TEXT("succeeded.\n"));
    }
    else
    {
        MyHandleError(TEXT("Error during ")
            TEXT("CryptReleaseContext #1!\n"));
    }

    //---------------------------------------------------------------
    // Release the provider handle again.
    if (CryptReleaseContext(hCryptProv, 0)) 
    {
        _tprintf(TEXT("The second call to CryptReleaseContext ")
            TEXT("succeeded.\n"));
    }
    else
    {
        MyHandleError(TEXT("Error during ")
            TEXT("CryptReleaseContext #2!\n"));
    }

    //---------------------------------------------------------------
    // Get a handle to a PROV_RSA_FULL provider and
    // create a key container named "My Sample Key Container".
    LPCTSTR pszContainerName = TEXT("My Sample Key Container");

    hCryptProv = NULL;
    if(CryptAcquireContext(
        &hCryptProv, 
        pszContainerName,
        NULL, 
        PROV_RSA_FULL, 
        CRYPT_NEWKEYSET)) 
    {
        _tprintf(TEXT("CryptAcquireContext succeeded. \n"));
        _tprintf(TEXT("New key set created. \n")); 

        //-----------------------------------------------------------
        // Release the provider handle and the key container.
        if(hCryptProv)
        {
            if(CryptReleaseContext(hCryptProv, 0)) 
            {
                hCryptProv = NULL;
                _tprintf(TEXT("CryptReleaseContext succeeded. \n"));
            }
            else
            {
                MyHandleError(TEXT("Error during ")
                    TEXT("CryptReleaseContext!\n"));
            }
        }
    }
    else
    {
        if(GetLastError() == NTE_EXISTS)
        {
            _tprintf(TEXT("The named key container could not be ")
                TEXT("created because it already exists.\n"));
            
            // Just continue the program. The named container 
            // will be reopened below.
        }
        else
        {
            MyHandleError(TEXT("Error during CryptAcquireContext ")
                TEXT("for a new key container."));
        }
    }

    //---------------------------------------------------------------
    // Get a handle to the provider by using the new key container. 
    // Note: This key container will be empty until keys
    // are explicitly created by using the CryptGenKey function.
    if(CryptAcquireContext(
        &hCryptProv, 
        pszContainerName, 
        NULL, 
        PROV_RSA_FULL,
        0)) 
    {
        _tprintf(TEXT("Acquired the key set just created. \n"));
    }
    else
    {
        MyHandleError(TEXT("Error during CryptAcquireContext!\n"));
    }

    //---------------------------------------------------------------
    // Perform cryptographic operations.

    //---------------------------------------------------------------
    // Release the provider handle.
    if(CryptReleaseContext(
        hCryptProv, 
        0)) 
    {
        _tprintf(TEXT("CryptReleaseContext succeeded. \n"));
    }
    else
    {
        MyHandleError(TEXT("Error during CryptReleaseContext!\n"));
    }

    //---------------------------------------------------------------
    // Delete the new key container.
    if(CryptAcquireContext(
        &hCryptProv, 
        pszContainerName, 
        NULL, 
        PROV_RSA_FULL,
        CRYPT_DELETEKEYSET)) 
    {
        _tprintf(TEXT("Deleted the key container just created. \n"));
    }
    else
    {
        MyHandleError(TEXT("Error during CryptAcquireContext!\n"));
    }
} // End of main.
```



 

 
