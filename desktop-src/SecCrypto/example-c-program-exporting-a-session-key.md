---
description: Im folgenden Beispiel wird ein zufälliger Sitzungsschlüssel erstellt und ein exportier barer Schlüsselblob erstellt. Das Beispiel veranschaulicht die Verwendung von "CryptGetUserKey", "CryptExportKey" und verwandter Funktionen.
ms.assetid: a7f2fdd1-9514-4cda-bae2-2f379dd9a27d
title: 'Beispiel-C-Programm: Exportieren eines Sitzungsschlüssels'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5252e5eced86dd4e671f5080cf6dab5e1ec96b9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755569"
---
# <a name="example-c-program-exporting-a-session-key"></a><span data-ttu-id="d8dfe-104">Beispiel-C-Programm: Exportieren eines Sitzungsschlüssels</span><span class="sxs-lookup"><span data-stu-id="d8dfe-104">Example C Program: Exporting a Session Key</span></span>

<span data-ttu-id="d8dfe-105">Im folgenden Beispiel wird ein zufälliger Sitzungsschlüssel erstellt und ein exportier barer [*Schlüsselblob*](../secgloss/k-gly.md)erstellt.</span><span class="sxs-lookup"><span data-stu-id="d8dfe-105">The following example creates a random session key and creates an exportable [*key BLOB*](../secgloss/k-gly.md).</span></span> <span data-ttu-id="d8dfe-106">Das Beispiel veranschaulicht die Verwendung von " [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey)", " [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey)" und verwandter Funktionen.</span><span class="sxs-lookup"><span data-stu-id="d8dfe-106">The example illustrates the use of [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey), [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey), and related functions.</span></span>

<span data-ttu-id="d8dfe-107">In diesem Beispiel werden die folgenden Aufgaben und kryptoapi-Funktionen veranschaulicht:</span><span class="sxs-lookup"><span data-stu-id="d8dfe-107">This example illustrates the following tasks and CryptoAPI functions:</span></span>

-   <span data-ttu-id="d8dfe-108">Abrufen eines CSP-Kontexts mithilfe von [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta).</span><span class="sxs-lookup"><span data-stu-id="d8dfe-108">Acquiring a CSP context using [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta).</span></span>
-   <span data-ttu-id="d8dfe-109">Zugriff auf zwei verschiedene Paare von öffentlichen/privaten Schlüsseln mithilfe von [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey).</span><span class="sxs-lookup"><span data-stu-id="d8dfe-109">Gaining access to two different pairs of public/private keys using [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey).</span></span>
-   <span data-ttu-id="d8dfe-110">Generieren eines exportierbaren Sitzungsschlüssels mithilfe von [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey).</span><span class="sxs-lookup"><span data-stu-id="d8dfe-110">Generating an exportable session key using [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey).</span></span>
-   <span data-ttu-id="d8dfe-111">Erstellen eines [*einfachen Schlüsselblobs*](../secgloss/s-gly.md) , das einen Sitzungsschlüssel mithilfe von [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey)enthält.</span><span class="sxs-lookup"><span data-stu-id="d8dfe-111">Creating a [*simple key BLOB*](../secgloss/s-gly.md) containing a session key using [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey).</span></span>
-   <span data-ttu-id="d8dfe-112">Zerstören eines Sitzungsschlüssels und Zugreifen auf die beiden Paare von öffentlichen/privaten Schlüsseln mithilfe von [**cryptdestroykey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey).</span><span class="sxs-lookup"><span data-stu-id="d8dfe-112">Destroying a session key and access to the two pairs of public/private keys using [**CryptDestroyKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey).</span></span>
-   <span data-ttu-id="d8dfe-113">Freigeben des CSP-Kontexts mithilfe von [**cryptreleasecontext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptreleasecontext).</span><span class="sxs-lookup"><span data-stu-id="d8dfe-113">Releasing the CSP context using [**CryptReleaseContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptreleasecontext).</span></span>

<span data-ttu-id="d8dfe-114">In diesem Beispiel wird die Funktion " [**myhanderror**](myhandleerror.md)" verwendet.</span><span class="sxs-lookup"><span data-stu-id="d8dfe-114">This example uses the function [**MyHandleError**](myhandleerror.md).</span></span> <span data-ttu-id="d8dfe-115">Der Code für diese Funktion ist im Beispiel enthalten.</span><span class="sxs-lookup"><span data-stu-id="d8dfe-115">The code for this function is included with the sample.</span></span> <span data-ttu-id="d8dfe-116">Der Code für dieses und andere Hilfsfunktionen ist auch unter [universell Funktionen](general-purpose-functions.md)aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="d8dfe-116">Code for this and other auxiliary functions is also listed under [General Purpose Functions](general-purpose-functions.md).</span></span>


```C++
//--------------------------------------------------------------------
// Copyright (C) Microsoft.  All rights reserved.
// This example program creates a session key and a simple key 
// BLOB holding that session key. The key BLOB can be written to disk 
// and later read from a disk file.
#pragma comment(lib, "crypt32.lib")

#include <stdio.h>
#include <windows.h>
#include <Wincrypt.h>
#define MY_ENCODING_TYPE  (PKCS_7_ASN_ENCODING | X509_ASN_ENCODING)
void MyHandleError(char *s);

void main(void)
{
//--------------------------------------------------------------------
// Declare and initialize variables.

HCRYPTPROV hProv;       // CSP handle
HCRYPTKEY hSignKey;     // Signature key pair handle
HCRYPTKEY hXchgKey;     // Exchange key pair handle
HCRYPTKEY hKey;         // Session key handle
BYTE *pbKeyBlob;        // Pointer to a simple key BLOB
DWORD dwBlobLen;        // The length of the key BLOB

//--------------------------------------------------------------------
// Acquire a cryptographic provider context handle.

if(CryptAcquireContext(
   &hProv, 
   NULL, 
   NULL, 
   PROV_RSA_FULL, 
   0)) 
{
    printf("The CSP has been acquired. \n");
}
else
{
    MyHandleError("Error during CryptAcquireContext.");
}
//--------------------------------------------------------------------
// Get a handle to the signature key.
// The signature key must exist before it can be retrieved. For more
// information, see the CryptGetUserKey documentation.

if(CryptGetUserKey(
   hProv, 
   AT_SIGNATURE, 
   &hSignKey)) 
{
    printf("The signature key has been acquired. \n");
}
else
{
    MyHandleError("Error during CryptGetUserKey for signkey.");
}
//--------------------------------------------------------------------
// Get a handle to the key exchange key.
// The key must exist before it can be retrieved. For more
// information, see the CryptGetUserKey documentation.

if(CryptGetUserKey(
   hProv, 
   AT_KEYEXCHANGE, 
   &hXchgKey)) 
{
    printf("The key exchange key has been acquired. \n");
}
else
{
    printf("Error during CryptGetUserKey exchange key.");
}
// hSignKey may be used to verify a signature. hXchgKey will be used
// to export a session key.

//--------------------------------------------------------------------
// Generate a session key.

if (CryptGenKey(     
    hProv,      
    CALG_RC4,      
    CRYPT_EXPORTABLE, 
    &hKey))
{   
    printf("Original session key is created. \n");
}
else
{
   MyHandleError("ERROR -- CryptGenKey.");
}
// Determine the size of the key BLOB and allocate memory.

if(CryptExportKey(
   hKey, 
   hXchgKey, 
   SIMPLEBLOB, 
   0, 
   NULL, 
   &dwBlobLen)) 
{
     printf("Size of the BLOB for the session key determined. \n");
}
else
{
     MyHandleError("Error computing BLOB length.");
}

if(pbKeyBlob = (BYTE*)malloc(dwBlobLen)) 
{
    printf("Memory has been allocated for the BLOB. \n");
}
else
{
    MyHandleError("Out of memory. \n");
}
//--------------------------------------------------------------------
// Export the key into a simple key BLOB.

if(CryptExportKey(
   hKey, 
   hXchgKey, 
   SIMPLEBLOB, 
   0, 
   pbKeyBlob, 
   &dwBlobLen))
{
     printf("Contents have been written to the BLOB. \n");
}
else
{
    MyHandleError("Error during CryptExportKey.");
}
//--------------------------------------------------------------------
//   At this point, other processing such as writing the key BLOB to
//   a file could be done.

//--------------------------------------------------------------------
// After all processing, clean up.

//--------------------------------------------------------------------
//  Free the memory used by the key BLOB.

free(pbKeyBlob);

// Destroy the session key.
if(hKey)
    CryptDestroyKey(hKey);

// Destroy the signature key handle.
if(hSignKey)
    CryptDestroyKey(hSignKey);

// Destroy the key exchange key handle.
if(hXchgKey)
     CryptDestroyKey(hXchgKey);

// Release the provider handle.
if(hProv) 
   CryptReleaseContext(hProv, 0);
printf("The program ran to completion without error. \n");

}// End of main                                                    

//--------------------------------------------------------------------
//  This example uses the function MyHandleError, a simple error
//  handling function, to print an error message and exit 
//  the program. 
//  For most applications, replace this function with one 
//  that does more extensive error reporting.

void MyHandleError(char *s)
{
    printf("An error occurred in running the program.\n");
    printf("%s\n",s);
    printf("Error number %x\n.",GetLastError());
    printf("Program terminating.\n");
    exit(1);
}
```



 

 
