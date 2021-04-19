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
# <a name="encrypting-data-with-cng"></a>Verschlüsseln von Daten mit CNG

Die primäre Verwendung einer beliebigen kryptografieapi besteht darin, Daten zu verschlüsseln und zu entschlüsseln. CNG ermöglicht das Verschlüsseln von Daten mithilfe einer minimalen Anzahl von Funktionsaufrufen und ermöglicht Ihnen die Durchführung der gesamten Speicherverwaltung. Während viele Details der Protokoll Implementierung dem Benutzer überlassen werden, stellt CNG die primitiven bereit, die die eigentlichen Daten Verschlüsselungs-und Entschlüsselungs Aufgaben ausführen.

-   [Verschlüsseln von Daten](#encrypting-data-with-cng)
-   [Beispiel für das Verschlüsseln von Daten](#encrypting-data-example)
-   [Entschlüsseln von Daten](#decrypting-data)

## <a name="encrypting-data"></a>Verschlüsseln von Daten

Führen Sie die folgenden Schritte aus, um Daten zu verschlüsseln:

1.  Öffnen Sie einen Algorithmusanbieter, der die Verschlüsselung unterstützt, z. **b. bcrypt \_ des- \_ Algorithmus**
2.  Erstellen Sie einen Schlüssel, mit dem die Daten verschlüsselt werden. Ein Schlüssel kann mit einer der folgenden Funktionen erstellt werden:
    -   [**BCryptGenerateKeyPair**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgeneratekeypair) oder [**BCryptImportKeyPair**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptimportkeypair) für asymmetrische Anbieter.
    -   [**BCryptGenerateSymmetricKey**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgeneratesymmetrickey) oder [**BCryptImportKey**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptimportkey) für symmetrische Anbieter.

    > [!Note]  
    > Die Verschlüsselung und Entschlüsselung von Daten mit einem asymmetrischen Schlüssel ist im Vergleich zur Verschlüsselung des symmetrischen Schlüssels Rechen intensiv. Wenn Sie Daten mit einem asymmetrischen Schlüssel verschlüsseln müssen, sollten Sie die Daten mit einem symmetrischen Schlüssel verschlüsseln, den symmetrischen Schlüssel mit einem asymmetrischen Schlüssel verschlüsseln und den verschlüsselten symmetrischen Schlüssel mit der Nachricht einschließen. Der Empfänger kann dann den symmetrischen Schlüssel entschlüsseln und den symmetrischen Schlüssel verwenden, um die Daten zu entschlüsseln.

     

3.  Abrufen der Größe der verschlüsselten Daten. Dies basiert auf dem Verschlüsselungsalgorithmus, dem Auffüll Schema (sofern vorhanden) und der Größe der zu verschlüsselnden Daten. Sie können die verschlüsselte Datengröße mit der [**BCryptEncrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptencrypt) -Funktion abrufen und dabei **null** für den *pboutput* -Parameter übergeben. Alle anderen Parameter müssen mit Ausnahme des Parameters *pbinput* , der in diesem Fall nicht verwendet wird, identisch sein, wenn die Daten tatsächlich verschlüsselt werden.
4.  Sie können entweder die Daten direkt mit dem gleichen Puffer verschlüsseln oder die Daten in einem separaten Puffer verschlüsseln.

    Wenn Sie die Daten direkt verschlüsseln möchten, übergeben Sie den Klartext-Puffer Zeiger sowohl für den Parameter *pbinput* als auch für den Parameter *pboutput* in der Funktion [**BCryptEncrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptencrypt) . Es ist möglich, dass die verschlüsselte Datengröße größer als die unverschlüsselte Datengröße ist, sodass der Klartext-Puffer groß genug sein muss, um die verschlüsselten Daten zu speichern, nicht nur den Klartext. Sie können die in Schritt 3 erhaltene Größe verwenden, um den Klartext-Puffer zuzuordnen.

    Wenn Sie die Daten in einem separaten Puffer verschlüsseln möchten, weisen Sie einen Speicherpuffer für die verschlüsselten Daten zu, indem Sie die in Schritt 3 abzurufende Größe verwenden.

5.  Aufrufen der [**BCryptEncrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptencrypt) -Funktion, um die Daten zu verschlüsseln. Diese Funktion schreibt die verschlüsselten Daten an den Speicherort, der im *pboutput* -Parameter bereitgestellt wird.
6.  Speichern Sie die verschlüsselten Daten bei Bedarf.
7.  Wiederholen Sie die Schritte 5 und 6, bis alle Daten verschlüsselt wurden.

## <a name="encrypting-data-example"></a>Beispiel für das Verschlüsseln von Daten

Im folgenden Beispiel wird gezeigt, wie Daten mit CNG mithilfe des symmetrischen Verschlüsselungsalgorithmus Advanced Encryption Standard verschlüsselt werden.


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

1.  Öffnen Sie einen Algorithmusanbieter, der die Verschlüsselung unterstützt, z. **b. bcrypt \_ des- \_ Algorithmus**
2.  Rufen Sie den Schlüssel ab, mit dem die Daten verschlüsselt wurden, und verwenden Sie diesen Schlüssel zum Abrufen eines Handles für den Schlüssel.
3.  Abrufen der Größe der entschlüsselten Daten. Dies basiert auf dem Verschlüsselungsalgorithmus, dem Auffüll Schema (sofern vorhanden) und der Größe der zu entschlüsselnden Daten. Sie können die verschlüsselte Datengröße mit der Funktion " [**bcryptentschlüsseln**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdecrypt) " abrufen und dabei **null** für den *pboutput* -Parameter übergeben. Die Parameter, mit denen das Auffüll Schema und der [*Initialisierungs Vektor*](/windows/desktop/SecGloss/i-gly) (IV) angegeben werden, müssen mit Ausnahme des *pbinput* -Parameters identisch sein, der in diesem Fall nicht verwendet wird.
4.  Zuordnen eines Speicherpuffers für die entschlüsselten Daten.
5.  Sie können die Daten entweder mit dem gleichen Puffer entschlüsseln oder die Daten in einem separaten Puffer entschlüsseln.

    Wenn Sie die Daten direkt entschlüsseln möchten, übergeben Sie den Chiffre Text Puffer Zeiger sowohl für den *pbinput* -Parameter als auch für den *pboutput* -Parameter in der Funktion " [**bcryptentschlpt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdecrypt) ".

    Wenn Sie die Daten in einem separaten Puffer entschlüsseln möchten, weisen Sie einen Arbeitsspeicher Puffer für die entschlüsselten Daten zu, indem Sie die in Schritt 3 abzurufende Größe verwenden.

6.  Aufrufen der Funktion " [**bcryptentschlpt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdecrypt) " zum Entschlüsseln der Daten. Die Parameter, die das Paddingschema und der IV angeben, müssen identisch mit dem Zeitpunkt sein, an dem die Daten verschlüsselt wurden. Diese Funktion schreibt die entschlüsselten Daten in den Speicherort, der im *pboutput* -Parameter bereitgestellt wird.
7.  Speichern Sie die entschlüsselten Daten bei Bedarf.
8.  Wiederholen Sie die Schritte 5 und 6, bis alle Daten entschlüsselt wurden.

 

 
