---
description: Beim Signieren von Daten werden die Daten nicht geschützt. Es wird nur die Integrität der Daten überprüft.
ms.assetid: 8f0ace5a-c8f9-4a45-8500-041a9f22637d
title: Signieren von Daten mit CNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64a05f6cf655421422945d375c9d54ec2b74ae24efe1640c0dc9f6efe9a3e45c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118907151"
---
# <a name="signing-data-with-cng"></a>Signieren von Daten mit CNG

Beim Signieren von Daten werden die Daten nicht geschützt. Es wird nur die Integrität der Daten überprüft. Der Absender hasht diese Daten und signiert (verschlüsselt) den Hash mithilfe eines privaten Schlüssels. Der vorgesehene Empfänger führt die Überprüfung durch, indem er einen Hash der empfangenen Daten erstellt, die Signatur entschlüsselt, um den ursprünglichen Hash zu erhalten, und die beiden Hashes vergleicht.

Wenn Daten signiert sind, erstellt der Absender einen [*Hashwert*](/windows/desktop/SecGloss/h-gly) und signiert (verschlüsselt) den Hash mithilfe eines privaten Schlüssels. Diese Signatur wird dann an die Daten angefügt und in einer Nachricht an einen Empfänger gesendet. Der Hashalgorithmus, der zum Erstellen der Signatur verwendet wurde, muss dem Empfänger im Voraus bekannt sein oder in der Nachricht identifiziert werden. Dies erfolgt über das Nachrichtenprotokoll.

Um die Signatur zu überprüfen, extrahiert der Empfänger die Daten und die Signatur aus der Nachricht. Der Empfänger erstellt dann einen weiteren Hashwert aus den Daten, entschlüsselt den signierten Hash mithilfe des öffentlichen Schlüssels des Absenders und vergleicht die beiden Hashwerte. Wenn die Werte identisch sind, wurde die Signatur überprüft, und es wird davon ausgegangen, dass die Daten unverändert sind.

**So erstellen Sie eine Signatur mit CNG**

1.  Erstellen Sie mithilfe der CNG-Hashfunktionen einen Hashwert für die Daten. Weitere Informationen zum Erstellen eines Hashs finden Sie unter Creating a Hash With CNG ( [Erstellen eines Hashs mit CNG](creating-a-hash-with-cng.md)).
2.  Erstellen Sie einen asymmetrischen Schlüssel zum Signieren des Hashs. Sie können entweder einen persistenten Schlüssel mit dem [CNG-Schlüssel Storage Functions](cng-key-storage-functions.md) oder einen kurzlebigen Schlüssel mit den kryptografischen primitiven [CNG-Funktionen erstellen.](cng-cryptographic-primitive-functions.md)
3.  Verwenden Sie entweder [**die NCryptSignHash-**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptsignhash) oder [**die BCryptSignHash-Funktion,**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptsignhash) um den Hashwert zu signieren (zu verschlüsseln). Diese Funktion signiert den Hashwert mithilfe des asymmetrischen Schlüssels.
4.  Kombinieren Sie die Daten und die Signatur in einer Nachricht, die an den vorgesehenen Empfänger gesendet werden kann.

**So überprüfen Sie eine Signatur mit CNG**

1.  Extrahieren Sie die Daten und die Signatur aus der Nachricht.
2.  Erstellen Sie mithilfe der CNG-Hashfunktionen einen Hashwert für die Daten. Der verwendete Hashalgorithmus muss derselbe Algorithmus sein, der zum Signieren des Hashs verwendet wurde.
3.  Abrufen des öffentlichen Teils des asymmetrischen Schlüsselpaars, das zum Signieren des Hashs verwendet wurde. Wie Sie diesen Schlüssel abrufen, hängt davon ab, wie der Schlüssel erstellt und beibehalten wurde. Wenn der Schlüssel mit dem [CNG-Schlüssel Storage Functions](cng-key-storage-functions.md)erstellt oder geladen wurde, verwenden Sie die [**NCryptOpenKey-Funktion,**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptopenkey) um den persistenten Schlüssel zu laden. Wenn der Schlüssel ein kurzlebiger Schlüssel ist, muss er in einem SchlüsselBLOB gespeichert worden sein. Sie müssen dieses Schlüssel-BLOB entweder an die [**BCryptImportKeyPair- oder**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptimportkeypair) [**die NCryptImportKey-Funktion**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptimportkey) übergeben.
4.  Übergeben Sie den neuen Hashwert, die Signatur und das Schlüsselhand handle entweder an [**die NCryptVerifySignature-**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptverifysignature) oder die [**BCryptVerifySignature-Funktion.**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptverifysignature) Diese Funktionen führen die Überprüfung durch, indem sie den öffentlichen Schlüssel verwenden, um die Signatur zu entschlüsseln und den entschlüsselten Hash mit dem in Schritt 2 berechneten Hash zu vergleichen. Die **BCryptVerifySignature-Funktion** gibt **STATUS \_ SUCCESS** zurück, wenn die Signatur dem Hash entspricht, oder **STATUS INVALID \_ \_ SIGNATURE,** wenn die Signatur nicht dem Hash entspricht. Die **NCryptVerifySignature-Funktion** gibt **STATUS \_ SUCCESS** zurück, wenn die Signatur dem Hash entspricht, oder **NTE \_ BAD \_ SIGNATURE,** wenn die Signatur nicht dem Hash entspricht.

## <a name="signing-and-verifying-data-example"></a>Beispiel für das Signieren und Überprüfen von Daten

Das folgende Beispiel zeigt, wie Sie die kryptografischen primitiven APIs verwenden, um Daten mit einem persistenten Schlüssel zu signieren und die Signatur mit einem kurzlebigen Schlüssel zu überprüfen.


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



 

 
