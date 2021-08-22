---
description: Hashes sind besonders nützlich, um die Integrität der Daten zu überprüfen, wenn sie mit einem asymmetrischen Signaturalgorithmus verwendet werden.
ms.assetid: f36b7e36-4377-4940-8951-6caba6e3ce8a
title: Erstellen eines Hashs mit CNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f57d56c4be7dc2f947dbb1869e63fb1789f57e9b4fe6b3a7a06e3cce15580ab8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118907819"
---
# <a name="creating-a-hash-with-cng"></a>Erstellen eines Hashs mit CNG

Ein [*Hash*](/windows/desktop/SecGloss/h-gly) ist ein unidirektionischer Vorgang, der für einen Datenblock ausgeführt wird, um einen eindeutigen Hashwert zu erstellen, der den Inhalt der Daten darstellt. Unabhängig davon, wann der Hash ausgeführt wird, erzeugt der gleiche [*Hashalgorithmus,*](/windows/desktop/SecGloss/h-gly) der für dieselben Daten ausgeführt wird, immer den gleichen Hashwert. Wenn sich eine der Daten ändert, ändert sich der Hashwert entsprechend.

Hashes sind für die Verschlüsselung von Daten nicht nützlich, da sie nicht zum Reproduzieren der ursprünglichen Daten aus dem Hashwert verwendet werden sollen. Hashes sind besonders nützlich, um die Integrität der Daten zu überprüfen, wenn sie mit einem asymmetrischen Signaturalgorithmus verwendet werden. Wenn Sie beispielsweise einen Hash für eine Textnachricht erstellt, den Hash signiert und den signierten Hashwert in die ursprüngliche Nachricht eingeschlossen haben, könnte der Empfänger den signierten Hash überprüfen, den Hashwert für die empfangene Nachricht erstellen und diesen Hashwert dann mit dem in der ursprünglichen Nachricht enthaltenen signierten Hashwert vergleichen. Wenn die beiden Hashwerte identisch sind, kann der Empfänger sicher sein, dass die ursprüngliche Nachricht nicht geändert wurde.

Die Größe des Hashwerts wird für einen bestimmten Hashalgorithmus festgelegt. Dies bedeutet, dass der Hashwert immer die gleiche Größe hat, unabhängig davon, wie groß oder klein der Datenblock ist. Als Beispiel hat der SHA256-Hashalgorithmus eine Hashwertgröße von 256 Bits.

-   [Erstellen eines Hashobjekts](#creating-a-hashing-object)
-   [Erstellen eines wiederverwendbaren Hashobjekts](#creating-a-reusable-hashing-object)
-   [Duplizieren eines Hashobjekts](#duplicating-a-hash-object)

## <a name="creating-a-hashing-object"></a>Erstellen eines Hashobjekts

Führen Sie die folgenden Schritte aus, um einen Hash mit CNG zu erstellen:

1.  Öffnen Sie einen Algorithmusanbieter, der den gewünschten Algorithmus unterstützt. Typische Hashalgorithmen sind MD2, MD4, MD5, SHA-1 und SHA256. Rufen Sie die [**BCryptOpenAlgorithmProvider-Funktion**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) auf, und geben Sie den entsprechenden Algorithmusbezeichner im *parameter pszAlgId* an. Die Funktion gibt ein Handle an den Anbieter zurück.
2.  Führen Sie die folgenden Schritte aus, um das Hashobjekt zu erstellen:

    1.  Rufen Sie die Größe des Objekts ab, indem Sie die [**BCryptGetProperty-Funktion**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) aufrufen, um die **BCRYPT \_ OBJECT \_ LENGTH-Eigenschaft** abzurufen.
    2.  Zuordnen von Arbeitsspeicher zum Speichern des Hashobjekts.
    3.  Erstellen Sie das -Objekt, indem Sie die [**BCryptCreateHash-Funktion**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash) aufrufen.

3.  Hash der Daten. Dies umfasst das mehrmalige Aufrufen der [**BCryptHashData-Funktion.**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcrypthashdata) Jeder Aufruf fügt die angegebenen Daten an den Hash an.
4.  Führen Sie die folgenden Schritte aus, um den Hashwert abzurufen:

    1.  Rufen Sie die Größe des Werts ab, indem Sie die [**BCryptGetProperty-Funktion**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) aufrufen, um die **BCRYPT \_ HASH \_ LENGTH-Eigenschaft** abzurufen.
    2.  Zuordnen von Arbeitsspeicher zum Speichern des Werts.
    3.  Rufen Sie den Hashwert ab, indem Sie die [**BCryptFinishHash-Funktion**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptfinishhash) aufrufen. Nachdem diese Funktion aufgerufen wurde, ist das Hashobjekt nicht mehr gültig.

5.  Um dieses Verfahren abzuschließen, müssen Sie die folgenden Bereinigungsschritte ausführen:

    1.  Schließen Sie das Hashobjekt, indem Sie das Hashhandle an die [**BCryptDestroyHash-Funktion**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdestroyhash) übergeben.
    2.  Freigeben des Arbeitsspeichers, den Sie für das Hashobjekt belegt haben.
    3.  Wenn Sie keine weiteren Hashobjekte erstellen, schließen Sie den Algorithmusanbieter, indem Sie das Anbieterhandle an die [**BCryptCloseAlgorithmProvider-Funktion**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptclosealgorithmprovider) übergeben.

        Wenn Sie weitere Hashobjekte erstellen, empfiehlt es sich, den Algorithmusanbieter wiederzuverwenden, anstatt denselben Algorithmusanbietertyp mehrmals zu erstellen und zu zerstören.

    4.  Wenn Sie die Verwendung des Hashwertspeichers abgeschlossen haben, können Sie ihn freigeben.

Das folgende Beispiel zeigt, wie Sie einen Hashwert mithilfe von CNG erstellen.


```C++
// THIS CODE AND INFORMATION IS PROVIDED "AS IS" WITHOUT WARRANTY OF
// ANY KIND, EITHER EXPRESSED OR IMPLIED, INCLUDING BUT NOT LIMITED TO
// THE IMPLIED WARRANTIES OF MERCHANTABILITY AND/OR FITNESS FOR A
// PARTICULAR PURPOSE.
//
// Copyright (C) Microsoft. All rights reserved.
/*++

Abstract:

    Sample program for SHA 256 hashing using CNG

--*/


#include <windows.h>
#include <stdio.h>
#include <bcrypt.h>



#define NT_SUCCESS(Status)          (((NTSTATUS)(Status)) >= 0)

#define STATUS_UNSUCCESSFUL         ((NTSTATUS)0xC0000001L)


static const BYTE rgbMsg[] = 
{
    0x61, 0x62, 0x63
};


void __cdecl wmain(
                   int                      argc, 
                   __in_ecount(argc) LPWSTR *wargv)
{

    BCRYPT_ALG_HANDLE       hAlg            = NULL;
    BCRYPT_HASH_HANDLE      hHash           = NULL;
    NTSTATUS                status          = STATUS_UNSUCCESSFUL;
    DWORD                   cbData          = 0,
                            cbHash          = 0,
                            cbHashObject    = 0;
    PBYTE                   pbHashObject    = NULL;
    PBYTE                   pbHash          = NULL;

    UNREFERENCED_PARAMETER(argc);
    UNREFERENCED_PARAMETER(wargv);

    //open an algorithm handle
    if(!NT_SUCCESS(status = BCryptOpenAlgorithmProvider(
                                                &hAlg,
                                                BCRYPT_SHA256_ALGORITHM,
                                                NULL,
                                                0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptOpenAlgorithmProvider\n", status);
        goto Cleanup;
    }

    //calculate the size of the buffer to hold the hash object
    if(!NT_SUCCESS(status = BCryptGetProperty(
                                        hAlg, 
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
                                        hAlg, 
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
                                        hAlg, 
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

    wprintf(L"Success!\n");

Cleanup:

    if(hAlg)
    {
        BCryptCloseAlgorithmProvider(hAlg,0);
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

}

```



## <a name="creating-a-reusable-hashing-object"></a>Erstellen eines wiederverwendbaren Hashobjekts

Ab Windows 8 und Windows Server 2012 können Sie ein wiederverwendbares Hashobjekt für Szenarien erstellen, in denen Sie mehrere Hashes oder HMACs in schneller Folge berechnen müssen. Geben Sie hierzu das **BCRYPT \_ HASH \_ REUSABLE \_ FLAG** an, wenn Sie die [**BCryptOpenAlgorithmProvider-Funktion**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) aufrufen. Dieses Flag wird von allen Microsoft-Hashalgorithmusanbietern unterstützt. Ein hashing-Objekt, das mit diesem Flag erstellt wurde, kann sofort nach dem Aufruf von [**BCryptFinishHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptfinishhash) wiederverwendet werden, so als ob es durch Aufrufen von [**BCryptCreateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash)neu erstellt worden wäre. Führen Sie die folgenden Schritte aus, um ein wiederverwendbares Hashobjekt zu erstellen:

1.  Öffnen Sie einen Algorithmusanbieter, der den gewünschten Hashalgorithmus unterstützt. Rufen Sie die [**BCryptOpenAlgorithmProvider-Funktion**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) auf, und geben Sie den entsprechenden Algorithmusbezeichner im *parameter pszAlgId* und **das BCRYPT HASH \_ \_ REUSABLE \_ FLAG** im *dwFlags-Parameter* an. Die Funktion gibt ein Handle an den Anbieter zurück.
2.  Führen Sie die folgenden Schritte aus, um das Hashobjekt zu erstellen:

    1.  Rufen Sie die Größe des Objekts ab, indem Sie die [**BCryptGetProperty-Funktion**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) aufrufen, um die **BCRYPT \_ OBJECT \_ LENGTH-Eigenschaft** abzurufen.
    2.  Zuordnen von Arbeitsspeicher zum Speichern des Hashobjekts.
    3.  Erstellen Sie das -Objekt, indem Sie die [**BCryptCreateHash-Funktion**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash) aufrufen. Geben Sie **BCRYPT \_ HASH \_ REUSABLE \_ FLAG** im *dwFlags-Parameter* an.

3.  Hashen Sie die Daten, indem Sie die [**BCryptHashData-Funktion**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcrypthashdata) aufrufen.
4.  Führen Sie die folgenden Schritte aus, um den Hashwert abzurufen:

    1.  Rufen Sie die Größe des Hashwerts ab, indem Sie die [**BCryptGetProperty-Funktion**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) aufrufen, um die **BCRYPT \_ HASH \_ LENGTH-Eigenschaft** abzurufen.
    2.  Zuordnen von Arbeitsspeicher zum Speichern des Werts.
    3.  Rufen Sie den Hashwert ab, indem [**Sie BCryptFinishHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptfinishhash)aufrufen.

5.  Um das Hashobjekt mit neuen Daten wiederzuverwenden, fahren Sie mit Schritt 3 fort.
6.  Um dieses Verfahren abzuschließen, müssen Sie die folgenden Bereinigungsschritte ausführen:

    1.  Schließen Sie das Hashobjekt, indem Sie das Hashhandle an die [**BCryptDestroyHash-Funktion**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdestroyhash) übergeben.
    2.  Freigeben des Arbeitsspeichers, den Sie für das Hashobjekt belegt haben.
    3.  Wenn Sie keine weiteren Hashobjekte erstellen, schließen Sie den Algorithmusanbieter, indem Sie das Anbieterhandle an die [**BCryptCloseAlgorithmProvider-Funktion**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptclosealgorithmprovider) übergeben.
    4.  Wenn Sie die Verwendung des Hashwertspeichers abgeschlossen haben, können Sie ihn freigeben.

## <a name="duplicating-a-hash-object"></a>Duplizieren eines Hashobjekts

Unter bestimmten Umständen kann es hilfreich sein, eine bestimmte Menge allgemeiner Daten zu hashen und dann zwei separate Hashobjekte aus den gemeinsamen Daten zu erstellen. Sie müssen nicht zwei separate Hashobjekte erstellen und die gemeinsamen Daten zweimal hashen, um dies zu erreichen. Sie können ein einzelnes Hashobjekt erstellen und dem Hashobjekt alle allgemeinen Daten hinzufügen. Anschließend können Sie die [**BCryptDuplicateHash-Funktion**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptduplicatehash) verwenden, um ein Duplikat des ursprünglichen Hashobjekts zu erstellen. Das doppelte Hashobjekt enthält alle Zustandsinformationen und Hashdaten wie das originale, es handelt sich jedoch um ein vollständig unabhängiges Hashobjekt. Sie können nun die eindeutigen Daten zu jedem der Hashobjekte hinzufügen und den Hashwert abrufen, wie im Beispiel gezeigt. Diese Technik ist beim Hashing einer möglicherweise großen Menge allgemeiner Daten nützlich. Sie müssen dem ursprünglichen Hash nur einmal die allgemeinen Daten hinzufügen, und dann können Sie das Hashobjekt duplizieren, um ein eindeutiges Hashobjekt zu erhalten.

 

 
