---
description: Durch das Signieren von Daten werden die Daten nicht geschützt. Es überprüft nur die Integrität der Daten.
ms.assetid: 8f0ace5a-c8f9-4a45-8500-041a9f22637d
title: Signieren von Daten mit CNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 658dd1c9a833cfb15b708a7f85013e3d9cacac9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131292"
---
# <a name="signing-data-with-cng"></a><span data-ttu-id="48cf3-104">Signieren von Daten mit CNG</span><span class="sxs-lookup"><span data-stu-id="48cf3-104">Signing Data with CNG</span></span>

<span data-ttu-id="48cf3-105">Durch das Signieren von Daten werden die Daten nicht geschützt.</span><span class="sxs-lookup"><span data-stu-id="48cf3-105">Data signing does not protect the data.</span></span> <span data-ttu-id="48cf3-106">Es überprüft nur die Integrität der Daten.</span><span class="sxs-lookup"><span data-stu-id="48cf3-106">It only to verifies the integrity of the data.</span></span> <span data-ttu-id="48cf3-107">Der Absender Hashes diese Daten und signiert den Hash mithilfe eines privaten Schlüssels (verschlüsselt).</span><span class="sxs-lookup"><span data-stu-id="48cf3-107">The sender hashes that data and signs (encrypts) the hash by using a private key.</span></span> <span data-ttu-id="48cf3-108">Der beabsichtigte Empfänger führt die Überprüfung durch, indem er einen Hash der empfangenen Daten erstellt, die Signatur entschlüsselt, um den ursprünglichen Hash abzurufen, und die beiden Hashes vergleicht.</span><span class="sxs-lookup"><span data-stu-id="48cf3-108">The intended recipient performs verification by creating a hash of the data received, decrypting the signature to obtain the original hash, and comparing the two hashes.</span></span>

<span data-ttu-id="48cf3-109">Beim Signieren von Daten erstellt der Absender einen [*Hashwert*](/windows/desktop/SecGloss/h-gly) und signiert den Hash mithilfe eines privaten Schlüssels (verschlüsselt).</span><span class="sxs-lookup"><span data-stu-id="48cf3-109">When data is signed, the sender creates a [*hash*](/windows/desktop/SecGloss/h-gly) value and signs (encrypts) the hash by using a private key.</span></span> <span data-ttu-id="48cf3-110">Diese Signatur wird dann an die Daten angefügt und in einer Nachricht an einen Empfänger gesendet.</span><span class="sxs-lookup"><span data-stu-id="48cf3-110">This signature is then attached to the data and sent in a message to a recipient.</span></span> <span data-ttu-id="48cf3-111">Der Hash Algorithmus, der zum Erstellen der Signatur verwendet wurde, muss vom Empfänger im Voraus bekannt sein oder in der Nachricht identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="48cf3-111">The hashing algorithm that was used to create the signature must be known in advance by the recipient or identified in the message.</span></span> <span data-ttu-id="48cf3-112">Wie dies geschieht, ist das Nachrichtenprotokoll.</span><span class="sxs-lookup"><span data-stu-id="48cf3-112">How this is done is up to the message protocol.</span></span>

<span data-ttu-id="48cf3-113">Zum Überprüfen der Signatur extrahiert der Empfänger die Daten und die Signatur aus der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="48cf3-113">To verify the signature, the recipient extracts the data and the signature from the message.</span></span> <span data-ttu-id="48cf3-114">Der Empfänger erstellt dann einen weiteren Hashwert aus den Daten, entschlüsselt den signierten Hash mithilfe des öffentlichen Schlüssels des Absenders und vergleicht die beiden Hashwerte.</span><span class="sxs-lookup"><span data-stu-id="48cf3-114">The recipient then creates another hash value from the data, decrypts the signed hash by using the sender's public key, and compares the two hash values.</span></span> <span data-ttu-id="48cf3-115">Wenn die Werte identisch sind, wurde die Signatur überprüft, und es wird davon ausgegangen, dass die Daten unverändert sind.</span><span class="sxs-lookup"><span data-stu-id="48cf3-115">If the values are identical, the signature has been verified and the data is assumed to be unaltered.</span></span>

<span data-ttu-id="48cf3-116">**So erstellen Sie eine Signatur mithilfe von CNG**</span><span class="sxs-lookup"><span data-stu-id="48cf3-116">**To create a signature by using CNG**</span></span>

1.  <span data-ttu-id="48cf3-117">Erstellen Sie einen Hashwert für die Daten mithilfe der CNG-Hash Funktionen.</span><span class="sxs-lookup"><span data-stu-id="48cf3-117">Create a hash value for the data by using the CNG hashing functions.</span></span> <span data-ttu-id="48cf3-118">Weitere Informationen zum Erstellen eines Hashs finden Sie unter [Erstellen eines Hash mit CNG](creating-a-hash-with-cng.md).</span><span class="sxs-lookup"><span data-stu-id="48cf3-118">For more information about creating a hash, see [Creating a Hash With CNG](creating-a-hash-with-cng.md).</span></span>
2.  <span data-ttu-id="48cf3-119">Erstellen Sie einen asymmetrischen Schlüssel zum Signieren des Hashs.</span><span class="sxs-lookup"><span data-stu-id="48cf3-119">Create an asymmetric key to sign the hash.</span></span> <span data-ttu-id="48cf3-120">Sie können entweder einen persistenten Schlüssel mit den [CNG-Schlüsselspeicher Funktionen](cng-key-storage-functions.md) oder einen kurzlebigen Schlüssel mit den [kryptografischen CNG-Funktionen](cng-cryptographic-primitive-functions.md)erstellen.</span><span class="sxs-lookup"><span data-stu-id="48cf3-120">You can either create a persistent key with the [CNG Key Storage Functions](cng-key-storage-functions.md) or an ephemeral key with the [CNG Cryptographic Primitive Functions](cng-cryptographic-primitive-functions.md).</span></span>
3.  <span data-ttu-id="48cf3-121">Verwenden Sie entweder die [**ncryptsignhash**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptsignhash) -Funktion oder die [**BCryptSignHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptsignhash) -Funktion, um den Hashwert zu signieren (zu verschlüsseln).</span><span class="sxs-lookup"><span data-stu-id="48cf3-121">Use either the [**NCryptSignHash**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptsignhash) or the [**BCryptSignHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptsignhash) function to sign (encrypt) the hash value.</span></span> <span data-ttu-id="48cf3-122">Diese Funktion signiert den Hashwert mithilfe des asymmetrischen Schlüssels.</span><span class="sxs-lookup"><span data-stu-id="48cf3-122">This function signs the hash value by using the asymmetric key.</span></span>
4.  <span data-ttu-id="48cf3-123">Kombinieren Sie die Daten und die Signatur in einer Nachricht, die an den beabsichtigten Empfänger gesendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="48cf3-123">Combine the data and signature into a message which can be sent sent to the intended recipient.</span></span>

<span data-ttu-id="48cf3-124">**So überprüfen Sie eine Signatur mithilfe von CNG**</span><span class="sxs-lookup"><span data-stu-id="48cf3-124">**To verify a signature by using CNG**</span></span>

1.  <span data-ttu-id="48cf3-125">Extrahieren Sie die Daten und die Signatur aus der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="48cf3-125">Extract the data and signature from the message.</span></span>
2.  <span data-ttu-id="48cf3-126">Erstellen Sie einen Hashwert für die Daten mithilfe der CNG-Hash Funktionen.</span><span class="sxs-lookup"><span data-stu-id="48cf3-126">Create a hash value for the data by using the CNG hashing functions.</span></span> <span data-ttu-id="48cf3-127">Der verwendete Hash Algorithmus muss derselbe Algorithmus sein, der zum Signieren des Hashwerts verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="48cf3-127">The hashing algorithm used must be the same algorithm that was used to sign he hash.</span></span>
3.  <span data-ttu-id="48cf3-128">Abrufen des öffentlichen Teils des asymmetrischen Schlüssel Paars, das zum Signieren des Hashs verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="48cf3-128">Obtain the public portion of the asymmetric key pair that was used to sign the hash.</span></span> <span data-ttu-id="48cf3-129">Wie Sie diesen Schlüssel erhalten, hängt davon ab, wie der Schlüssel erstellt und persistent gespeichert wurde.</span><span class="sxs-lookup"><span data-stu-id="48cf3-129">How you obtain this key depends on how the key was created and persisted.</span></span> <span data-ttu-id="48cf3-130">Wenn der Schlüssel mit den [CNG-Schlüsselspeicher Funktionen](cng-key-storage-functions.md)erstellt oder geladen wurde, verwenden Sie die [**ncryptopenkey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptopenkey) -Funktion, um den persistenten Schlüssel zu laden.</span><span class="sxs-lookup"><span data-stu-id="48cf3-130">If the key was created or loaded with the [CNG Key Storage Functions](cng-key-storage-functions.md), you will use the [**NCryptOpenKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptopenkey) function to load the persisted key.</span></span> <span data-ttu-id="48cf3-131">Wenn es sich bei dem Schlüssel um einen kurzlebigen Schlüssel handelt, muss er in einem Schlüsselblob gespeichert worden sein.</span><span class="sxs-lookup"><span data-stu-id="48cf3-131">If the key is an ephemeral key, then it would have to have been saved to a key BLOB.</span></span> <span data-ttu-id="48cf3-132">Sie müssen dieses Schlüsselblob entweder an die Funktion [**BCryptImportKeyPair**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptimportkeypair) oder an die [**ncryptimportkey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptimportkey) -Funktion übergeben.</span><span class="sxs-lookup"><span data-stu-id="48cf3-132">You need to pass this key BLOB to either the [**BCryptImportKeyPair**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptimportkeypair) or the [**NCryptImportKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptimportkey) function.</span></span>
4.  <span data-ttu-id="48cf3-133">Übergeben Sie den neuen Hashwert, die Signatur und das Schlüssel handle entweder an die [**ncryptverifysignature**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptverifysignature) -oder die [**BCryptVerifySignature**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptverifysignature) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="48cf3-133">Pass the new hash value, the signature, and the key handle to either the [**NCryptVerifySignature**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptverifysignature) or the [**BCryptVerifySignature**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptverifysignature) function.</span></span> <span data-ttu-id="48cf3-134">Diese Funktionen führen die Überprüfung durch, indem Sie den öffentlichen Schlüssel verwenden, um die Signatur zu entschlüsseln und den entschlüsselten Hash mit dem in Schritt 2 berechneten Hash zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="48cf3-134">These functions perform verification by using the public key to decrypt the signature and comparing the decrypted hash to the hash computed in step 2.</span></span> <span data-ttu-id="48cf3-135">Die Funktion " **BCryptVerifySignature** " gibt den **Status " \_ erfolgreich** " zurück, wenn die Signatur mit dem Hash oder der **\_ ungültigen \_ Signatur** übereinstimmt, wenn die Signatur nicht mit dem Hash übereinstimmt</span><span class="sxs-lookup"><span data-stu-id="48cf3-135">The **BCryptVerifySignature** function will return **STATUS\_SUCCESS** if the signature matches the hash or **STATUS\_INVALID\_SIGNATURE** if the signature does not match the hash.</span></span> <span data-ttu-id="48cf3-136">Die **ncryptverifysignature** -Funktion gibt den **Status " \_ erfolgreich** " zurück, wenn die Signatur mit dem Hash übereinstimmt oder eine ungültige **\_ \_ Signatur** ergibt, wenn die Signatur nicht mit dem Hash übereinstimmt</span><span class="sxs-lookup"><span data-stu-id="48cf3-136">The **NCryptVerifySignature** function will return **STATUS\_SUCCESS** if the signature matches the hash or **NTE\_BAD\_SIGNATURE** if the signature does not match the hash.</span></span>

## <a name="signing-and-verifying-data-example"></a><span data-ttu-id="48cf3-137">Beispiel für Signierung und Verifizierung</span><span class="sxs-lookup"><span data-stu-id="48cf3-137">Signing and Verifying Data Example</span></span>

<span data-ttu-id="48cf3-138">Im folgenden Beispiel wird gezeigt, wie die kryptografischen primitiven APIs verwendet werden, um Daten mit einem permanenten Schlüssel zu signieren und die Signatur mit einem kurzlebigen Schlüssel zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="48cf3-138">The following example shows how to use the cryptographic primitive APIs to sign data with a persisted key and verify the signature with an ephemeral key.</span></span>


```C++
// THIS CODE AND INFORMATION IS PROVIDED "AS IS" WITHOUT WARRANTY OF
// ANY KIND, EITHER EXPRESSED OR IMPLIED, INCLUDING BUT NOT LIMITED TO
// THE IMPLIED WARRANTIES OF MERCHANTABILITY AND/OR FITNESS FOR A
// PARTICULAR PURPOSE.
//
// Copyright (C) Microsoft. All rights reserved.
/*++

Abstract:

    Sample program for ECDSA 256 signing using CNG
    
    Example for use of BCrypt/NCrypt API
    
    Persisted key for signing and ephemeral key for verification

--*/

#include <windows.h>
#include <stdio.h>
#include <bcrypt.h>
#include <ncrypt.h>


#define NT_SUCCESS(Status)          (((NTSTATUS)(Status)) >= 0)

#define STATUS_UNSUCCESSFUL         ((NTSTATUS)0xC0000001L)


static const  BYTE rgbMsg[] =
{
    0x04, 0x87, 0xec, 0x66, 0xa8, 0xbf, 0x17, 0xa6,
    0xe3, 0x62, 0x6f, 0x1a, 0x55, 0xe2, 0xaf, 0x5e,
    0xbc, 0x54, 0xa4, 0xdc, 0x68, 0x19, 0x3e, 0x94,
};

void __cdecl wmain(
                   int                      argc, 
                   __in_ecount(argc) LPWSTR *wargv)
{
    NCRYPT_PROV_HANDLE      hProv           = NULL;
    NCRYPT_KEY_HANDLE       hKey            = NULL;
    BCRYPT_KEY_HANDLE       hTmpKey         = NULL;
    SECURITY_STATUS         secStatus       = ERROR_SUCCESS;
    BCRYPT_ALG_HANDLE       hHashAlg        = NULL,
                            hSignAlg        = NULL;
    BCRYPT_HASH_HANDLE      hHash           = NULL;
    NTSTATUS                status          = STATUS_UNSUCCESSFUL;
    DWORD                   cbData          = 0,
                            cbHash          = 0,
                            cbBlob          = 0,
                            cbSignature     = 0,
                            cbHashObject    = 0;
    PBYTE                   pbHashObject    = NULL;
    PBYTE                   pbHash          = NULL,
                            pbBlob          = NULL,
                            pbSignature     = NULL;

    UNREFERENCED_PARAMETER(argc);
    UNREFERENCED_PARAMETER(wargv);

    //open an algorithm handle
    if(!NT_SUCCESS(status = BCryptOpenAlgorithmProvider(
                                                &hHashAlg,
                                                BCRYPT_SHA1_ALGORITHM,
                                                NULL,
                                                0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptOpenAlgorithmProvider\n", status);
        goto Cleanup;
    }

    if(!NT_SUCCESS(status = BCryptOpenAlgorithmProvider(
                                                &hSignAlg,
                                                BCRYPT_ECDSA_P256_ALGORITHM,
                                                NULL,
                                                0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptOpenAlgorithmProvider\n", status);
        goto Cleanup;
    }

    //calculate the size of the buffer to hold the hash object
    if(!NT_SUCCESS(status = BCryptGetProperty(
                                        hHashAlg, 
                                        BCRYPT_OBJECT_LENGTH, 
                                        (PBYTE)&cbHashObject, 
                                        sizeof(DWORD), 
                                        &cbData, 
                                        0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptGetProperty\n", status);
        goto Cleanup;
    }

    //allocate the hash object on the heap
    pbHashObject = (PBYTE)HeapAlloc (GetProcessHeap (), 0, cbHashObject);
    if(NULL == pbHashObject)
    {
        wprintf(L"**** memory allocation failed\n");
        goto Cleanup;
    }

   //calculate the length of the hash
    if(!NT_SUCCESS(status = BCryptGetProperty(
                                        hHashAlg, 
                                        BCRYPT_HASH_LENGTH, 
                                        (PBYTE)&cbHash, 
                                        sizeof(DWORD), 
                                        &cbData, 
                                        0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptGetProperty\n", status);
        goto Cleanup;
    }

    //allocate the hash buffer on the heap
    pbHash = (PBYTE)HeapAlloc (GetProcessHeap (), 0, cbHash);
    if(NULL == pbHash)
    {
        wprintf(L"**** memory allocation failed\n");
        goto Cleanup;
    }

    //create a hash
    if(!NT_SUCCESS(status = BCryptCreateHash(
                                        hHashAlg, 
                                        &hHash, 
                                        pbHashObject, 
                                        cbHashObject, 
                                        NULL, 
                                        0, 
                                        0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptCreateHash\n", status);
        goto Cleanup;
    }
    

    //hash some data
    if(!NT_SUCCESS(status = BCryptHashData(
                                        hHash,
                                        (PBYTE)rgbMsg,
                                        sizeof(rgbMsg),
                                        0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptHashData\n", status);
        goto Cleanup;
    }
    
    //close the hash
    if(!NT_SUCCESS(status = BCryptFinishHash(
                                        hHash, 
                                        pbHash, 
                                        cbHash, 
                                        0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptFinishHash\n", status);
        goto Cleanup;
    }

    //open handle to KSP
    if(FAILED(secStatus = NCryptOpenStorageProvider(
                                                &hProv, 
                                                MS_KEY_STORAGE_PROVIDER, 
                                                0)))
    {
        wprintf(L"**** Error 0x%x returned by NCryptOpenStorageProvider\n", secStatus);
        goto Cleanup;
    }

    //create a persisted key
    if(FAILED(secStatus = NCryptCreatePersistedKey(
                                                hProv,
                                                &hKey,
                                                NCRYPT_ECDSA_P256_ALGORITHM,
                                                L"my ecc key",
                                                0,
                                                0)))
    {
        wprintf(L"**** Error 0x%x returned by NCryptCreatePersistedKey\n", secStatus);
        goto Cleanup;
    }

    //create key on disk
    if(FAILED(secStatus = NCryptFinalizeKey(hKey, 0)))
    {
        wprintf(L"**** Error 0x%x returned by NCryptFinalizeKey\n", secStatus);
        goto Cleanup;
    }

    //sign the hash
    if(FAILED(secStatus = NCryptSignHash(
                                    hKey,
                                    NULL,
                                    pbHash,
                                    cbHash,
                                    NULL,
                                    0,
                                    &cbSignature,
                                    0)))
    {
        wprintf(L"**** Error 0x%x returned by NCryptSignHash\n", secStatus);
        goto Cleanup;
    }


    //allocate the signature buffer
    pbSignature = (PBYTE)HeapAlloc (GetProcessHeap (), 0, cbSignature);
    if(NULL == pbSignature)
    {
        wprintf(L"**** memory allocation failed\n");
        goto Cleanup;
    }

    if(FAILED(secStatus = NCryptSignHash(
                                    hKey,
                                    NULL,
                                    pbHash,
                                    cbHash,
                                    pbSignature,
                                    cbSignature,
                                    &cbSignature,
                                    0)))
    {
        wprintf(L"**** Error 0x%x returned by NCryptSignHash\n", secStatus);
        goto Cleanup;
    }

    if(FAILED(secStatus = NCryptExportKey(
                                        hKey,
                                        NULL,
                                        BCRYPT_ECCPUBLIC_BLOB,
                                        NULL,
                                        NULL,
                                        0,
                                        &cbBlob,
                                        0)))
    {
        wprintf(L"**** Error 0x%x returned by NCryptExportKey\n", secStatus);
        goto Cleanup;
    }

    pbBlob = (PBYTE)HeapAlloc (GetProcessHeap (), 0, cbBlob);
    if(NULL == pbBlob)
    {
        wprintf(L"**** memory allocation failed\n");
        goto Cleanup;
    }

    if(FAILED(secStatus = NCryptExportKey(
                                        hKey,
                                        NULL,
                                        BCRYPT_ECCPUBLIC_BLOB,
                                        NULL,
                                        pbBlob,
                                        cbBlob,
                                        &cbBlob,
                                        0)))
    {
        wprintf(L"**** Error 0x%x returned by NCryptExportKey\n", secStatus);
        goto Cleanup;
    }

    if(!NT_SUCCESS(status = BCryptImportKeyPair(
                                            hSignAlg,
                                            NULL,
                                            BCRYPT_ECCPUBLIC_BLOB,
                                            &hTmpKey,
                                            pbBlob,
                                            cbBlob,
                                            0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptImportKeyPair\n", status);
        goto Cleanup;
    }

    if(!NT_SUCCESS(status = BCryptVerifySignature(
                                            hTmpKey,
                                            NULL,
                                            pbHash,
                                            cbHash,
                                            pbSignature,
                                            cbSignature,
                                            0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptVerifySignature\n", status);
        goto Cleanup;
    }

    wprintf(L"Success!\n");

Cleanup:

    if(hHashAlg)
    {
        BCryptCloseAlgorithmProvider(hHashAlg,0);
    }

    if(hSignAlg)
    {
        BCryptCloseAlgorithmProvider(hSignAlg,0);
    }

    if (hHash)    
    {
        BCryptDestroyHash(hHash);
    }

    if(pbHashObject)
    {
        HeapFree(GetProcessHeap(), 0, pbHashObject);
    }

    if(pbHash)
    {
        HeapFree(GetProcessHeap(), 0, pbHash);
    }

    if(pbSignature)
    {
        HeapFree(GetProcessHeap(), 0, pbSignature);
    }

    if(pbBlob)
    {
        HeapFree(GetProcessHeap(), 0, pbBlob);
    }

    if (hTmpKey)    
    {
        BCryptDestroyKey(hTmpKey);
    }

    if (hKey)    
    {
        NCryptDeleteKey(hKey, 0);
    }

    if (hProv)    
    {
        NCryptFreeObject(hProv);
    }    
}


```



 

 
