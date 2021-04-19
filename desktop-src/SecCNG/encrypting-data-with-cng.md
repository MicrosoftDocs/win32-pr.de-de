---
description: CNG ermöglicht das Verschlüsseln von Daten mithilfe einer minimalen Anzahl von Funktionsaufrufen und ermöglicht Ihnen die Durchführung der gesamten Speicherverwaltung.
ms.assetid: 40622282-e190-40d0-80d4-cab9eddc2091
title: Verschlüsseln von Daten mit CNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8f161cd23ec6863bee7f5ffd5b696fa99880e3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343028"
---
# <a name="encrypting-data-with-cng"></a><span data-ttu-id="d417d-103">Verschlüsseln von Daten mit CNG</span><span class="sxs-lookup"><span data-stu-id="d417d-103">Encrypting Data with CNG</span></span>

<span data-ttu-id="d417d-104">Die primäre Verwendung einer beliebigen kryptografieapi besteht darin, Daten zu verschlüsseln und zu entschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="d417d-104">The primary use of any cryptography API is to encrypt and decrypt data.</span></span> <span data-ttu-id="d417d-105">CNG ermöglicht das Verschlüsseln von Daten mithilfe einer minimalen Anzahl von Funktionsaufrufen und ermöglicht Ihnen die Durchführung der gesamten Speicherverwaltung.</span><span class="sxs-lookup"><span data-stu-id="d417d-105">CNG allows you to encrypt data by using a minimum number of function calls and allows you to perform all of the memory management.</span></span> <span data-ttu-id="d417d-106">Während viele Details der Protokoll Implementierung dem Benutzer überlassen werden, stellt CNG die primitiven bereit, die die eigentlichen Daten Verschlüsselungs-und Entschlüsselungs Aufgaben ausführen.</span><span class="sxs-lookup"><span data-stu-id="d417d-106">While many of the protocol implementation details are left up to the user, CNG provides the primitives that perform the actual data encryption and decryption tasks.</span></span>

-   [<span data-ttu-id="d417d-107">Verschlüsseln von Daten</span><span class="sxs-lookup"><span data-stu-id="d417d-107">Encrypting Data</span></span>](#encrypting-data-with-cng)
-   [<span data-ttu-id="d417d-108">Beispiel für das Verschlüsseln von Daten</span><span class="sxs-lookup"><span data-stu-id="d417d-108">Encrypting Data Example</span></span>](#encrypting-data-example)
-   [<span data-ttu-id="d417d-109">Entschlüsseln von Daten</span><span class="sxs-lookup"><span data-stu-id="d417d-109">Decrypting Data</span></span>](#decrypting-data)

## <a name="encrypting-data"></a><span data-ttu-id="d417d-110">Verschlüsseln von Daten</span><span class="sxs-lookup"><span data-stu-id="d417d-110">Encrypting Data</span></span>

<span data-ttu-id="d417d-111">Führen Sie die folgenden Schritte aus, um Daten zu verschlüsseln:</span><span class="sxs-lookup"><span data-stu-id="d417d-111">To encrypt data, perform the following steps:</span></span>

1.  <span data-ttu-id="d417d-112">Öffnen Sie einen Algorithmusanbieter, der die Verschlüsselung unterstützt, z. **b. bcrypt \_ des- \_ Algorithmus**</span><span class="sxs-lookup"><span data-stu-id="d417d-112">Open an algorithm provider that supports encryption, such as **BCRYPT\_DES\_ALGORITHM**.</span></span>
2.  <span data-ttu-id="d417d-113">Erstellen Sie einen Schlüssel, mit dem die Daten verschlüsselt werden.</span><span class="sxs-lookup"><span data-stu-id="d417d-113">Create a key to encrypt the data with.</span></span> <span data-ttu-id="d417d-114">Ein Schlüssel kann mit einer der folgenden Funktionen erstellt werden:</span><span class="sxs-lookup"><span data-stu-id="d417d-114">A key can be created by using any of the following functions:</span></span>
    -   <span data-ttu-id="d417d-115">[**BCryptGenerateKeyPair**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgeneratekeypair) oder [**BCryptImportKeyPair**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptimportkeypair) für asymmetrische Anbieter.</span><span class="sxs-lookup"><span data-stu-id="d417d-115">[**BCryptGenerateKeyPair**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgeneratekeypair) or [**BCryptImportKeyPair**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptimportkeypair) for asymmetric providers.</span></span>
    -   <span data-ttu-id="d417d-116">[**BCryptGenerateSymmetricKey**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgeneratesymmetrickey) oder [**BCryptImportKey**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptimportkey) für symmetrische Anbieter.</span><span class="sxs-lookup"><span data-stu-id="d417d-116">[**BCryptGenerateSymmetricKey**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgeneratesymmetrickey) or [**BCryptImportKey**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptimportkey) for symmetric providers.</span></span>

    > [!Note]  
    > <span data-ttu-id="d417d-117">Die Verschlüsselung und Entschlüsselung von Daten mit einem asymmetrischen Schlüssel ist im Vergleich zur Verschlüsselung des symmetrischen Schlüssels Rechen intensiv.</span><span class="sxs-lookup"><span data-stu-id="d417d-117">Data encryption and decryption with an asymmetric key is computationally intensive compared to symmetric key encryption.</span></span> <span data-ttu-id="d417d-118">Wenn Sie Daten mit einem asymmetrischen Schlüssel verschlüsseln müssen, sollten Sie die Daten mit einem symmetrischen Schlüssel verschlüsseln, den symmetrischen Schlüssel mit einem asymmetrischen Schlüssel verschlüsseln und den verschlüsselten symmetrischen Schlüssel mit der Nachricht einschließen.</span><span class="sxs-lookup"><span data-stu-id="d417d-118">If you need to encrypt data with an asymmetric key, you should encrypt the data with a symmetric key, encrypt the symmetric key with an asymmetric key, and include the encrypted symmetric key with the message.</span></span> <span data-ttu-id="d417d-119">Der Empfänger kann dann den symmetrischen Schlüssel entschlüsseln und den symmetrischen Schlüssel verwenden, um die Daten zu entschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="d417d-119">The recipient can then decrypt the symmetric key and use the symmetric key to decrypt the data.</span></span>

     

3.  <span data-ttu-id="d417d-120">Abrufen der Größe der verschlüsselten Daten.</span><span class="sxs-lookup"><span data-stu-id="d417d-120">Obtain the size of the encrypted data.</span></span> <span data-ttu-id="d417d-121">Dies basiert auf dem Verschlüsselungsalgorithmus, dem Auffüll Schema (sofern vorhanden) und der Größe der zu verschlüsselnden Daten.</span><span class="sxs-lookup"><span data-stu-id="d417d-121">This is based on the encryption algorithm, the padding scheme (if any), and the size of the data to be encrypted.</span></span> <span data-ttu-id="d417d-122">Sie können die verschlüsselte Datengröße mit der [**BCryptEncrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptencrypt) -Funktion abrufen und dabei **null** für den *pboutput* -Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="d417d-122">You can obtain the encrypted data size by using the [**BCryptEncrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptencrypt) function, passing **NULL** for the *pbOutput* parameter.</span></span> <span data-ttu-id="d417d-123">Alle anderen Parameter müssen mit Ausnahme des Parameters *pbinput* , der in diesem Fall nicht verwendet wird, identisch sein, wenn die Daten tatsächlich verschlüsselt werden.</span><span class="sxs-lookup"><span data-stu-id="d417d-123">All other parameters must be the same as when the data is actually encrypted except for the *pbInput* parameter, which is not used in this case.</span></span>
4.  <span data-ttu-id="d417d-124">Sie können entweder die Daten direkt mit dem gleichen Puffer verschlüsseln oder die Daten in einem separaten Puffer verschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="d417d-124">You can either encrypt the data in place with the same buffer or encrypt the data into a separate buffer.</span></span>

    <span data-ttu-id="d417d-125">Wenn Sie die Daten direkt verschlüsseln möchten, übergeben Sie den Klartext-Puffer Zeiger sowohl für den Parameter *pbinput* als auch für den Parameter *pboutput* in der Funktion [**BCryptEncrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptencrypt) .</span><span class="sxs-lookup"><span data-stu-id="d417d-125">If you want to encrypt the data in place, pass the plaintext buffer pointer for both the *pbInput* and *pbOutput* parameters in the [**BCryptEncrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptencrypt) function.</span></span> <span data-ttu-id="d417d-126">Es ist möglich, dass die verschlüsselte Datengröße größer als die unverschlüsselte Datengröße ist, sodass der Klartext-Puffer groß genug sein muss, um die verschlüsselten Daten zu speichern, nicht nur den Klartext.</span><span class="sxs-lookup"><span data-stu-id="d417d-126">It is possible that the encrypted data size will be larger than the unencrypted data size, so the plaintext buffer must be large enough to hold the encrypted data, not just the plaintext.</span></span> <span data-ttu-id="d417d-127">Sie können die in Schritt 3 erhaltene Größe verwenden, um den Klartext-Puffer zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="d417d-127">You can use the size obtained in step 3 to allocate the plaintext buffer.</span></span>

    <span data-ttu-id="d417d-128">Wenn Sie die Daten in einem separaten Puffer verschlüsseln möchten, weisen Sie einen Speicherpuffer für die verschlüsselten Daten zu, indem Sie die in Schritt 3 abzurufende Größe verwenden.</span><span class="sxs-lookup"><span data-stu-id="d417d-128">If you want to encrypt the data into a separate buffer, allocate a memory buffer for the encrypted data by using the size obtained in step 3.</span></span>

5.  <span data-ttu-id="d417d-129">Aufrufen der [**BCryptEncrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptencrypt) -Funktion, um die Daten zu verschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="d417d-129">Call the [**BCryptEncrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptencrypt) function to encrypt the data.</span></span> <span data-ttu-id="d417d-130">Diese Funktion schreibt die verschlüsselten Daten an den Speicherort, der im *pboutput* -Parameter bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="d417d-130">This function will write the encrypted data to the location provided in the *pbOutput* parameter.</span></span>
6.  <span data-ttu-id="d417d-131">Speichern Sie die verschlüsselten Daten bei Bedarf.</span><span class="sxs-lookup"><span data-stu-id="d417d-131">Persist the encrypted data as needed.</span></span>
7.  <span data-ttu-id="d417d-132">Wiederholen Sie die Schritte 5 und 6, bis alle Daten verschlüsselt wurden.</span><span class="sxs-lookup"><span data-stu-id="d417d-132">Repeat steps 5 and 6 until all of the data has been encrypted.</span></span>

## <a name="encrypting-data-example"></a><span data-ttu-id="d417d-133">Beispiel für das Verschlüsseln von Daten</span><span class="sxs-lookup"><span data-stu-id="d417d-133">Encrypting Data Example</span></span>

<span data-ttu-id="d417d-134">Im folgenden Beispiel wird gezeigt, wie Daten mit CNG mithilfe des symmetrischen Verschlüsselungsalgorithmus Advanced Encryption Standard verschlüsselt werden.</span><span class="sxs-lookup"><span data-stu-id="d417d-134">The following example shows how to encrypt data with CNG by using the advanced encryption standard symmetric encryption algorithm.</span></span>


```C++
// THIS CODE AND INFORMATION IS PROVIDED "AS IS" WITHOUT WARRANTY OF
// ANY KIND, EITHER EXPRESSED OR IMPLIED, INCLUDING BUT NOT LIMITED TO
// THE IMPLIED WARRANTIES OF MERCHANTABILITY AND/OR FITNESS FOR A
// PARTICULAR PURPOSE.
//
// Copyright (C) Microsoft. All rights reserved.
/*++

Abstract:
    Sample program for AES-CBC encryption using CNG

--*/

#include <windows.h>
#include <stdio.h>
#include <bcrypt.h>

#define NT_SUCCESS(Status)          (((NTSTATUS)(Status)) >= 0)

#define STATUS_UNSUCCESSFUL         ((NTSTATUS)0xC0000001L)


#define DATA_TO_ENCRYPT  "Test Data"


const BYTE rgbPlaintext[] = 
{
    0x00, 0x01, 0x02, 0x03, 0x04, 0x05, 0x06, 0x07, 
    0x08, 0x09, 0x0A, 0x0B, 0x0C, 0x0D, 0x0E, 0x0F
};

static const BYTE rgbIV[] =
{
    0x00, 0x01, 0x02, 0x03, 0x04, 0x05, 0x06, 0x07,
    0x08, 0x09, 0x0A, 0x0B, 0x0C, 0x0D, 0x0E, 0x0F
};

static const BYTE rgbAES128Key[] =
{
    0x00, 0x01, 0x02, 0x03, 0x04, 0x05, 0x06, 0x07, 
    0x08, 0x09, 0x0A, 0x0B, 0x0C, 0x0D, 0x0E, 0x0F
};

void PrintBytes(
                IN BYTE     *pbPrintData,
                IN DWORD    cbDataLen)
{
    DWORD dwCount = 0;

    for(dwCount=0; dwCount < cbDataLen;dwCount++)
    {
        printf("0x%02x, ",pbPrintData[dwCount]);

        if(0 == (dwCount + 1 )%10) putchar('\n');
    }

}

void __cdecl wmain(
                   int                      argc, 
                   __in_ecount(argc) LPWSTR *wargv)
{

    BCRYPT_ALG_HANDLE       hAesAlg                     = NULL;
    BCRYPT_KEY_HANDLE       hKey                        = NULL;
    NTSTATUS                status                      = STATUS_UNSUCCESSFUL;
    DWORD                   cbCipherText                = 0, 
                            cbPlainText                 = 0,
                            cbData                      = 0, 
                            cbKeyObject                 = 0,
                            cbBlockLen                  = 0,
                            cbBlob                      = 0;
    PBYTE                   pbCipherText                = NULL,
                            pbPlainText                 = NULL,
                            pbKeyObject                 = NULL,
                            pbIV                        = NULL,
                            pbBlob                      = NULL;

    UNREFERENCED_PARAMETER(argc);
    UNREFERENCED_PARAMETER(wargv);


    // Open an algorithm handle.
    if(!NT_SUCCESS(status = BCryptOpenAlgorithmProvider(
                                                &hAesAlg,
                                                BCRYPT_AES_ALGORITHM,
                                                NULL,
                                                0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptOpenAlgorithmProvider\n", status);
        goto Cleanup;
    }

    // Calculate the size of the buffer to hold the KeyObject.
    if(!NT_SUCCESS(status = BCryptGetProperty(
                                        hAesAlg, 
                                        BCRYPT_OBJECT_LENGTH, 
                                        (PBYTE)&cbKeyObject, 
                                        sizeof(DWORD), 
                                        &cbData, 
                                        0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptGetProperty\n", status);
        goto Cleanup;
    }

    // Allocate the key object on the heap.
    pbKeyObject = (PBYTE)HeapAlloc (GetProcessHeap (), 0, cbKeyObject);
    if(NULL == pbKeyObject)
    {
        wprintf(L"**** memory allocation failed\n");
        goto Cleanup;
    }

   // Calculate the block length for the IV.
    if(!NT_SUCCESS(status = BCryptGetProperty(
                                        hAesAlg, 
                                        BCRYPT_BLOCK_LENGTH, 
                                        (PBYTE)&cbBlockLen, 
                                        sizeof(DWORD), 
                                        &cbData, 
                                        0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptGetProperty\n", status);
        goto Cleanup;
    }

    // Determine whether the cbBlockLen is not longer than the IV length.
    if (cbBlockLen > sizeof (rgbIV))
    {
        wprintf (L"**** block length is longer than the provided IV length\n");
        goto Cleanup;
    }

    // Allocate a buffer for the IV. The buffer is consumed during the 
    // encrypt/decrypt process.
    pbIV= (PBYTE) HeapAlloc (GetProcessHeap (), 0, cbBlockLen);
    if(NULL == pbIV)
    {
        wprintf(L"**** memory allocation failed\n");
        goto Cleanup;
    }

    memcpy(pbIV, rgbIV, cbBlockLen);

    if(!NT_SUCCESS(status = BCryptSetProperty(
                                hAesAlg, 
                                BCRYPT_CHAINING_MODE, 
                                (PBYTE)BCRYPT_CHAIN_MODE_CBC, 
                                sizeof(BCRYPT_CHAIN_MODE_CBC), 
                                0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptSetProperty\n", status);
        goto Cleanup;
    }

                

     // Generate the key from supplied input key bytes.
    if(!NT_SUCCESS(status = BCryptGenerateSymmetricKey(
                                        hAesAlg, 
                                        &hKey, 
                                        pbKeyObject, 
                                        cbKeyObject, 
                                        (PBYTE)rgbAES128Key, 
                                        sizeof(rgbAES128Key), 
                                        0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptGenerateSymmetricKey\n", status);
        goto Cleanup;
    }

  
    // Save another copy of the key for later.
    if(!NT_SUCCESS(status = BCryptExportKey(
                                        hKey,
                                        NULL,
                                        BCRYPT_OPAQUE_KEY_BLOB,
                                        NULL,
                                        0,
                                        &cbBlob,
                                        0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptExportKey\n", status);
        goto Cleanup;
    }


    // Allocate the buffer to hold the BLOB.
    pbBlob = (PBYTE)HeapAlloc (GetProcessHeap (), 0, cbBlob);
    if(NULL == pbBlob)
    {
        wprintf(L"**** memory allocation failed\n");
        goto Cleanup;
    }

    if(!NT_SUCCESS(status = BCryptExportKey(
                                        hKey, 
                                        NULL, 
                                        BCRYPT_OPAQUE_KEY_BLOB,
                                        pbBlob, 
                                        cbBlob, 
                                        &cbBlob, 
                                        0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptExportKey\n", status);
        goto Cleanup;
    }
 
    cbPlainText = sizeof(rgbPlaintext);
    pbPlainText = (PBYTE)HeapAlloc (GetProcessHeap (), 0, cbPlainText);
    if(NULL == pbPlainText)
    {
        wprintf(L"**** memory allocation failed\n");
        goto Cleanup;
    }

    memcpy(pbPlainText, rgbPlaintext, sizeof(rgbPlaintext));
    
    //
    // Get the output buffer size.
    //
    if(!NT_SUCCESS(status = BCryptEncrypt(
                                        hKey, 
                                        pbPlainText, 
                                        cbPlainText,
                                        NULL,
                                        pbIV,
                                        cbBlockLen,
                                        NULL, 
                                        0, 
                                        &cbCipherText, 
                                        BCRYPT_BLOCK_PADDING)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptEncrypt\n", status);
        goto Cleanup;
    }

    pbCipherText = (PBYTE)HeapAlloc (GetProcessHeap (), 0, cbCipherText);
    if(NULL == pbCipherText)
    {
        wprintf(L"**** memory allocation failed\n");
        goto Cleanup;
    }

    // Use the key to encrypt the plaintext buffer.
    // For block sized messages, block padding will add an extra block.
    if(!NT_SUCCESS(status = BCryptEncrypt(
                                        hKey, 
                                        pbPlainText, 
                                        cbPlainText,
                                        NULL,
                                        pbIV,
                                        cbBlockLen, 
                                        pbCipherText, 
                                        cbCipherText, 
                                        &cbData, 
                                        BCRYPT_BLOCK_PADDING)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptEncrypt\n", status);
        goto Cleanup;
    }

    // Destroy the key and reimport from saved BLOB.
    if(!NT_SUCCESS(status = BCryptDestroyKey(hKey)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptDestroyKey\n", status);
        goto Cleanup;
    }    
    hKey = 0;

    if(pbPlainText)
    {
        HeapFree(GetProcessHeap(), 0, pbPlainText);
    }

    pbPlainText = NULL;

    // We can reuse the key object.
    memset(pbKeyObject, 0 , cbKeyObject);

    
    // Reinitialize the IV because encryption would have modified it.
    memcpy(pbIV, rgbIV, cbBlockLen);


    if(!NT_SUCCESS(status = BCryptImportKey(
                                        hAesAlg,
                                        NULL,
                                        BCRYPT_OPAQUE_KEY_BLOB,
                                        &hKey,
                                        pbKeyObject,
                                        cbKeyObject,
                                        pbBlob,
                                        cbBlob,
                                        0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptGenerateSymmetricKey\n", status);
        goto Cleanup;
    }
       

    //
    // Get the output buffer size.
    //
    if(!NT_SUCCESS(status = BCryptDecrypt(
                                    hKey, 
                                    pbCipherText, 
                                    cbCipherText, 
                                    NULL,
                                    pbIV,
                                    cbBlockLen,
                                    NULL, 
                                    0, 
                                    &cbPlainText, 
                                    BCRYPT_BLOCK_PADDING)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptDecrypt\n", status);
        goto Cleanup;
    }

    pbPlainText = (PBYTE)HeapAlloc (GetProcessHeap (), 0, cbPlainText);
    if(NULL == pbPlainText)
    {
        wprintf(L"**** memory allocation failed\n");
        goto Cleanup;
    }

    if(!NT_SUCCESS(status = BCryptDecrypt(
                                    hKey, 
                                    pbCipherText, 
                                    cbCipherText, 
                                    NULL,
                                    pbIV, 
                                    cbBlockLen,
                                    pbPlainText, 
                                    cbPlainText, 
                                    &cbPlainText, 
                                    BCRYPT_BLOCK_PADDING)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptDecrypt\n", status);
        goto Cleanup;
    }


    if (0 != memcmp(pbPlainText, (PBYTE)rgbPlaintext, sizeof(rgbPlaintext))) 
    {
        wprintf(L"Expected decrypted text comparison failed.\n");
        goto Cleanup;
    } 

    wprintf(L"Success!\n");


Cleanup:

    if(hAesAlg)
    {
        BCryptCloseAlgorithmProvider(hAesAlg,0);
    }

    if (hKey)    
    {
        BCryptDestroyKey(hKey);
    }

    if(pbCipherText)
    {
        HeapFree(GetProcessHeap(), 0, pbCipherText);
    }

    if(pbPlainText)
    {
        HeapFree(GetProcessHeap(), 0, pbPlainText);
    }

    if(pbKeyObject)
    {
        HeapFree(GetProcessHeap(), 0, pbKeyObject);
    }

    if(pbIV)
    {
        HeapFree(GetProcessHeap(), 0, pbIV);
    }

}
```



## <a name="decrypting-data"></a><span data-ttu-id="d417d-135">Entschlüsseln von Daten</span><span class="sxs-lookup"><span data-stu-id="d417d-135">Decrypting Data</span></span>

<span data-ttu-id="d417d-136">Führen Sie zum Entschlüsseln von Daten die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="d417d-136">To decrypt data, perform the following steps:</span></span>

1.  <span data-ttu-id="d417d-137">Öffnen Sie einen Algorithmusanbieter, der die Verschlüsselung unterstützt, z. **b. bcrypt \_ des- \_ Algorithmus**</span><span class="sxs-lookup"><span data-stu-id="d417d-137">Open an algorithm provider that supports encryption, such as **BCRYPT\_DES\_ALGORITHM**.</span></span>
2.  <span data-ttu-id="d417d-138">Rufen Sie den Schlüssel ab, mit dem die Daten verschlüsselt wurden, und verwenden Sie diesen Schlüssel zum Abrufen eines Handles für den Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="d417d-138">Obtain the key that the data was encrypted with, and use that key to obtain a handle for the key.</span></span>
3.  <span data-ttu-id="d417d-139">Abrufen der Größe der entschlüsselten Daten.</span><span class="sxs-lookup"><span data-stu-id="d417d-139">Obtain the size of the decrypted data.</span></span> <span data-ttu-id="d417d-140">Dies basiert auf dem Verschlüsselungsalgorithmus, dem Auffüll Schema (sofern vorhanden) und der Größe der zu entschlüsselnden Daten.</span><span class="sxs-lookup"><span data-stu-id="d417d-140">This is based on the encryption algorithm, the padding scheme (if any), and the size of the data to be decrypted.</span></span> <span data-ttu-id="d417d-141">Sie können die verschlüsselte Datengröße mit der Funktion " [**bcryptentschlüsseln**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdecrypt) " abrufen und dabei **null** für den *pboutput* -Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="d417d-141">You can obtain the encrypted data size by using the [**BCryptDecrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdecrypt) function, passing **NULL** for the *pbOutput* parameter.</span></span> <span data-ttu-id="d417d-142">Die Parameter, mit denen das Auffüll Schema und der [*Initialisierungs Vektor*](/windows/desktop/SecGloss/i-gly) (IV) angegeben werden, müssen mit Ausnahme des *pbinput* -Parameters identisch sein, der in diesem Fall nicht verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d417d-142">The parameters that specify the padding scheme and [*initialization vector*](/windows/desktop/SecGloss/i-gly) (IV) must be the same as when the data was encrypted except for the *pbInput* parameter, which is not used in this case.</span></span>
4.  <span data-ttu-id="d417d-143">Zuordnen eines Speicherpuffers für die entschlüsselten Daten.</span><span class="sxs-lookup"><span data-stu-id="d417d-143">Allocate a memory buffer for the decrypted data.</span></span>
5.  <span data-ttu-id="d417d-144">Sie können die Daten entweder mit dem gleichen Puffer entschlüsseln oder die Daten in einem separaten Puffer entschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="d417d-144">You can either decrypt the data in place by using the same buffer, or decrypt the data into a separate buffer.</span></span>

    <span data-ttu-id="d417d-145">Wenn Sie die Daten direkt entschlüsseln möchten, übergeben Sie den Chiffre Text Puffer Zeiger sowohl für den *pbinput* -Parameter als auch für den *pboutput* -Parameter in der Funktion " [**bcryptentschlpt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdecrypt) ".</span><span class="sxs-lookup"><span data-stu-id="d417d-145">If you want to decrypt the data in place, pass the ciphertext buffer pointer for both the *pbInput* and *pbOutput* parameters in the [**BCryptDecrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdecrypt) function.</span></span>

    <span data-ttu-id="d417d-146">Wenn Sie die Daten in einem separaten Puffer entschlüsseln möchten, weisen Sie einen Arbeitsspeicher Puffer für die entschlüsselten Daten zu, indem Sie die in Schritt 3 abzurufende Größe verwenden.</span><span class="sxs-lookup"><span data-stu-id="d417d-146">If you want to decrypt the data into a separate buffer, allocate a memory buffer for the decrypted data by using the size obtained in step 3.</span></span>

6.  <span data-ttu-id="d417d-147">Aufrufen der Funktion " [**bcryptentschlpt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdecrypt) " zum Entschlüsseln der Daten.</span><span class="sxs-lookup"><span data-stu-id="d417d-147">Call the [**BCryptDecrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdecrypt) function to decrypt the data.</span></span> <span data-ttu-id="d417d-148">Die Parameter, die das Paddingschema und der IV angeben, müssen identisch mit dem Zeitpunkt sein, an dem die Daten verschlüsselt wurden.</span><span class="sxs-lookup"><span data-stu-id="d417d-148">The parameters that specify the padding scheme and IV must be the same as when the data was encrypted.</span></span> <span data-ttu-id="d417d-149">Diese Funktion schreibt die entschlüsselten Daten in den Speicherort, der im *pboutput* -Parameter bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="d417d-149">This function will write the decrypted data to the location provided in the *pbOutput* parameter.</span></span>
7.  <span data-ttu-id="d417d-150">Speichern Sie die entschlüsselten Daten bei Bedarf.</span><span class="sxs-lookup"><span data-stu-id="d417d-150">Persist the decrypted data as needed.</span></span>
8.  <span data-ttu-id="d417d-151">Wiederholen Sie die Schritte 5 und 6, bis alle Daten entschlüsselt wurden.</span><span class="sxs-lookup"><span data-stu-id="d417d-151">Repeat steps 5 and 6 until all of the data has been decrypted.</span></span>

 

 
