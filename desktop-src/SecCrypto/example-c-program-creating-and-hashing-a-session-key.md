---
description: Erstellt und Hashes einen Sitzungsschlüssel, der zum Verschlüsseln einer Nachricht, eines Texts oder einer Datei verwendet werden kann.
ms.assetid: 15d4a05d-5888-4532-91fd-6cd94afe0b99
title: 'Beispiel-C-Programm: Erstellen und Hashwert eines Sitzungsschlüssels'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbfb1dae0f331a80a2b2c473f0446cf2a1623dda
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359508"
---
# <a name="example-c-program-creating-and-hashing-a-session-key"></a>Beispiel-C-Programm: Erstellen und Hashwert eines Sitzungsschlüssels

Im folgenden Beispiel wird ein [*Sitzungsschlüssel*](../secgloss/s-gly.md) erstellt und [*Hashes*](../secgloss/h-gly.md) erstellt, der zum Verschlüsseln von Nachrichten, Text oder Dateien verwendet werden kann.

Dieses Beispiel zeigt auch die Verwendung der folgenden CryptoAPI-Funktionen:

-   [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) zum Abrufen eines [*Kryptografiedienstanbieters*](../secgloss/c-gly.md).
-   [**Cryptkreatehash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) zum Erstellen eines leeren Hash Objekts.
-   [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) zum Erstellen eines zufälligen [*Sitzungsschlüssels*](../secgloss/s-gly.md).
-   [**Crypthashsessionkey**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashsessionkey) zum Hashen des erstellten Sitzungsschlüssels.
-   [**Cryptdestroyhash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroyhash) , um den Hash zu zerstören.
-   [**Cryptdestroykey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey) , um den erstellten Schlüssel zu zerstören.
-   [**Cryptreleasecontext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptreleasecontext) zum Freigeben des CSP.

In diesem Beispiel wird die Funktion " [**myhanderror**](myhandleerror.md)" verwendet. Der Code für diese Funktion ist im Beispiel enthalten. Der Code für dieses und andere Hilfsfunktionen ist auch unter [universell Funktionen](general-purpose-functions.md)aufgeführt.


```C++
//  Copyright (C) Microsoft. All rights reserved.
//  
//  CreateAndHashSessionKey.cpp : Defines the entry point for the 
//  application.
//

#include <stdafx.h>

#include <stdio.h>
#include <windows.h>
#include <Wincrypt.h>

// Link with the Crypt32.lib file.
#pragma comment (lib, "Crypt32")

#define MY_ENCODING_TYPE  (PKCS_7_ASN_ENCODING | X509_ASN_ENCODING)

void MyHandleError(LPTSTR psz);

void main()
{
    HCRYPTPROV hCryptProv;
    HCRYPTHASH hHash;
    HCRYPTKEY hKey;

    //---------------------------------------------------------------
    // Acquire a cryptographic provider context handle.
    if(CryptAcquireContext(
        &hCryptProv, 
        NULL, 
        NULL, 
        PROV_RSA_FULL, 
        0)) 
    {
        printf("CryptAcquireContext complete. \n");
    }
    else
    {
        MyHandleError("Acquisition of context failed.");
    }

    //---------------------------------------------------------------
    // Create a hash object.
    if(CryptCreateHash(
        hCryptProv, 
        CALG_MD5, 
        0, 
        0, 
        &hHash)) 
    {
        printf("An empty hash object has been created. \n");
    }
    else
    {
        MyHandleError("Error during CryptBeginHash!\n");
    }

    //---------------------------------------------------------------
    // Create a random session key.
    if(CryptGenKey(
        hCryptProv, 
        CALG_RC2, 
        CRYPT_EXPORTABLE, 
        &hKey)) 
    {
        printf("A random session key has been created. \n");
    }
    else
    {
        MyHandleError("Error during CryptGenKey!\n");
    }

    //---------------------------------------------------------------
    // Compute the cryptographic hash on the key object.
    if(CryptHashSessionKey(
        hHash, 
        hKey, 
        0))
    {
        printf("The session key has been hashed. \n");
    }
    else
    {
        MyHandleError("Error during CryptHashSessionKey!\n");
    }

    /*
    Use the hash of the key object. For instance, additional data 
    could be hashed and sent in a message to several recipients. The 
    recipients will be able to verify who the message originator is 
    if the key used is also exported to them.
    */

    //---------------------------------------------------------------
    // Clean up.

    // Destroy the hash object.

    if(hHash)
    {
        if(!(CryptDestroyHash(hHash)))
        {
            MyHandleError("Error during CryptDestroyHash");
        }
    }

    // Destroy the session key.
    if(hKey)
    {
        if(!(CryptDestroyKey(hKey)))
        {
            MyHandleError("Error during CryptDestroyKey");
        }
    }

    // Release the provider.
    if(hCryptProv)
    {
        if(!(CryptReleaseContext(hCryptProv,0)))
        {
            MyHandleError("Error during CryptReleaseContext");
        }
    }
} // End main.

//  Define function MyHandleError.
void MyHandleError(LPTSTR psz)
{
    _ftprintf(stderr, TEXT("An error occurred in the program. \n"));
    _ftprintf(stderr, TEXT("%s\n"), psz);
    _ftprintf(stderr, TEXT("Error number %x.\n"), GetLastError());
    _ftprintf(stderr, TEXT("Program terminating. \n"));
    exit(1);
} // End of MyHandleError.

```



 

 
