---
description: CNG ermöglicht es Ihnen, Daten mithilfe einer minimalen Anzahl von Funktionsaufrufen zu verschlüsseln, und ermöglicht Ihnen die Durchführung der speicherverwaltung.
ms.assetid: 40622282-e190-40d0-80d4-cab9eddc2091
title: Verschlüsseln von Daten mit CNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b264518c2a0ccfe0f626c869ba3062c0429941234ca0c286f9e7801961485b74
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118907738"
---
# <a name="encrypting-data-with-cng"></a>Verschlüsseln von Daten mit CNG

Die primäre Verwendung einer Kryptografie-API ist das Verschlüsseln und Entschlüsseln von Daten. CNG ermöglicht es Ihnen, Daten mithilfe einer minimalen Anzahl von Funktionsaufrufen zu verschlüsseln, und ermöglicht Ihnen die Durchführung der speicherverwaltung. Während viele details der Protokollimplementierung dem Benutzer bleiben, stellt CNG die Grundtypen zur Verfügung, die die eigentlichen Datenverschlüsselungs- und Entschlüsselungsaufgaben ausführen.

-   [Verschlüsseln von Daten](#encrypting-data-with-cng)
-   [Beispiel für die Verschlüsselung von Daten](#encrypting-data-example)
-   [Entschlüsseln von Daten](#decrypting-data)

## <a name="encrypting-data"></a>Verschlüsseln von Daten

Führen Sie zum Verschlüsseln von Daten die folgenden Schritte aus:

1.  Öffnen Sie einen Algorithmusanbieter, der Verschlüsselung unterstützt, z. **B. BCRYPT \_ DES \_ ALGORITHM**.
2.  Erstellen Sie einen Schlüssel zum Verschlüsseln der Daten. Ein Schlüssel kann mit einer der folgenden Funktionen erstellt werden:
    -   [**BCryptGenerateKeyPair oder**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgeneratekeypair) [**BCryptImportKeyPair**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptimportkeypair) für asymmetrische Anbieter.
    -   [**BCryptGenerateSymmetricKey**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgeneratesymmetrickey) oder [**BCryptImportKey für**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptimportkey) symmetrische Anbieter.

    > [!Note]  
    > Die Datenverschlüsselung und -entschlüsselung mit einem asymmetrischen Schlüssel ist im Vergleich zur Verschlüsselung symmetrischer Schlüssel rechenintensiv. Wenn Sie Daten mit einem asymmetrischen Schlüssel verschlüsseln müssen, sollten Sie die Daten mit einem symmetrischen Schlüssel verschlüsseln, den symmetrischen Schlüssel mit einem asymmetrischen Schlüssel verschlüsseln und den verschlüsselten symmetrischen Schlüssel mit der Nachricht enthalten. Der Empfänger kann dann den symmetrischen Schlüssel entschlüsseln und den symmetrischen Schlüssel verwenden, um die Daten zu entschlüsseln.

     

3.  Abrufen der Größe der verschlüsselten Daten. Dies basiert auf dem Verschlüsselungsalgorithmus, dem Auf padding-Schema (falls möglich) und der Größe der zu verschlüsselnden Daten. Sie können die verschlüsselte Datengröße abrufen, indem Sie die [**BCryptEncrypt-Funktion**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptencrypt) verwenden und **NULL** für den *pbOutput-Parameter* übergeben. Alle anderen Parameter müssen mit dem tatsächlichen Verschlüsseln der Daten identisch sein, mit Ausnahme des *pbInput-Parameters,* der in diesem Fall nicht verwendet wird.
4.  Sie können die Daten entweder direkt mit demselben Puffer oder in einem separaten Puffer verschlüsseln.

    Wenn Sie die Daten an Ort und Stelle verschlüsseln möchten, übergeben Sie den Klartextpufferzeiger für die Parameter *pbInput* und *pbOutput* in der [**BCryptEncrypt-Funktion.**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptencrypt) Es ist möglich, dass die verschlüsselte Datengröße größer als die unverschlüsselte Datengröße ist, sodass der Klartextpuffer groß genug sein muss, um die verschlüsselten Daten und nicht nur den Klartext zu halten. Sie können die in Schritt 3 erhaltene Größe verwenden, um den Klartextpuffer zu zuordnen.

    Wenn Sie die Daten in einem separaten Puffer verschlüsseln möchten, ordnen Sie einen Speicherpuffer für die verschlüsselten Daten zu, indem Sie die in Schritt 3 ermittelte Größe verwenden.

5.  Rufen Sie die [**BCryptEncrypt-Funktion**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptencrypt) auf, um die Daten zu verschlüsseln. Diese Funktion schreibt die verschlüsselten Daten an den Speicherort, der im *pbOutput-Parameter angegeben* ist.
6.  Die verschlüsselten Daten werden bei Bedarf beibehalten.
7.  Wiederholen Sie die Schritte 5 und 6, bis alle Daten verschlüsselt wurden.

## <a name="encrypting-data-example"></a>Beispiel für die Verschlüsselung von Daten

Das folgende Beispiel zeigt, wie Daten mit CNG mithilfe des erweiterten symmetrischen Verschlüsselungsalgorithmus für den Verschlüsselungsstandard verschlüsselt werden.


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



## <a name="decrypting-data"></a>Entschlüsseln von Daten

Führen Sie zum Entschlüsseln von Daten die folgenden Schritte aus:

1.  Öffnen Sie einen Algorithmusanbieter, der Verschlüsselung unterstützt, z. **B. BCRYPT \_ DES \_ ALGORITHM**.
2.  Beschaffen Sie den Schlüssel, mit dem die Daten verschlüsselt wurden, und verwenden Sie diesen Schlüssel, um ein Handle für den Schlüssel zu erhalten.
3.  Abrufen der Größe der entschlüsselten Daten. Dies basiert auf dem Verschlüsselungsalgorithmus, dem Auf padding-Schema (falls möglich) und der Größe der zu entschlüsselnden Daten. Sie können die verschlüsselte Datengröße abrufen, indem Sie die [**BCryptDecrypt-Funktion**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdecrypt) verwenden und **NULL** für den *pbOutput-Parameter* übergeben. Die Parameter, die das Auf [](/windows/desktop/SecGloss/i-gly) padding-Schema und den Initialisierungsvektor (IV) angeben, müssen mit denen identisch sein, als die Daten verschlüsselt wurden, mit Ausnahme des *pbInput-Parameters,* der in diesem Fall nicht verwendet wird.
4.  Ordnen Sie einen Speicherpuffer für die entschlüsselten Daten zu.
5.  Sie können die Daten entweder mithilfe desselben Puffers oder in einem separaten Puffer entschlüsseln.

    Wenn Sie die Daten an Ort und Stelle entschlüsseln möchten, übergeben Sie den Pufferzeiger für Chiffretext für die Parameter *pbInput* und *pbOutput* in der [**BCryptDecrypt-Funktion.**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdecrypt)

    Wenn Sie die Daten in einem separaten Puffer entschlüsseln möchten, ordnen Sie einen Speicherpuffer für die entschlüsselten Daten zu, indem Sie die in Schritt 3 ermittelte Größe verwenden.

6.  Rufen Sie die [**BCryptDecrypt-Funktion**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdecrypt) auf, um die Daten zu entschlüsseln. Die Parameter, die das Auf padding-Schema und IV angeben, müssen mit denen identisch sein, als die Daten verschlüsselt wurden. Diese Funktion schreibt die entschlüsselten Daten an den Speicherort, der im *pbOutput-Parameter angegeben* ist.
7.  Die entschlüsselten Daten werden bei Bedarf beibehalten.
8.  Wiederholen Sie die Schritte 5 und 6, bis alle Daten entschlüsselt wurden.

 

 
