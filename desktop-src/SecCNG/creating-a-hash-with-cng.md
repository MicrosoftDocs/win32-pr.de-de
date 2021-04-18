---
description: Hashes sind besonders nützlich, um die Integrität der Daten zu überprüfen, wenn Sie mit einem asymmetrischen Signatur Algorithmus verwendet werden.
ms.assetid: f36b7e36-4377-4940-8951-6caba6e3ce8a
title: Erstellen eines Hash mit CNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 735f95182b63facee687f408ea4a07e09399e562
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106338949"
---
# <a name="creating-a-hash-with-cng"></a>Erstellen eines Hash mit CNG

Bei einem [*Hash*](/windows/desktop/SecGloss/h-gly) handelt es sich um einen unidirektionalen Vorgang, der für einen Datenblock ausgeführt wird, um einen eindeutigen Hashwert zu erstellen, der den Inhalt der Daten darstellt. Unabhängig von der Durchführung des Hashwerts erzeugt derselbe Hash Algorithmus, der für die gleichen Daten ausgeführt wird, immer denselben [*Hashwert*](/windows/desktop/SecGloss/h-gly) . Wenn eine der Daten geändert wird, ändert sich der Hashwert entsprechend.

Hashes sind nicht für die Verschlüsselung von Daten nützlich, da Sie nicht zum Reproduzieren der ursprünglichen Daten aus dem Hashwert verwendet werden sollen. Hashes sind besonders nützlich, um die Integrität der Daten zu überprüfen, wenn Sie mit einem asymmetrischen Signatur Algorithmus verwendet werden. Wenn Sie z. b. einen Hashwert für eine Textnachricht, den Hash signiert und den Hashwert mit Vorzeichen mit der ursprünglichen Nachricht eingefügt haben, könnte der Empfänger den signierten Hash überprüfen, den Hashwert für die empfangene Nachricht erstellen und diesen Hashwert mit dem mit Vorzeichen signierten Hashwert vergleichen, der in der ursprünglichen Nachricht enthalten ist. Wenn die beiden Hashwerte identisch sind, kann der Empfänger sicher sein, dass die ursprüngliche Nachricht nicht geändert wurde.

Die Größe des Hashwerts ist für einen bestimmten Hash Algorithmus korrigiert. Dies bedeutet, dass unabhängig davon, wie groß oder klein der Datenblock ist, der Hashwert immer dieselbe Größe hat. Der SHA256-Hash Algorithmus hat z. b. eine Hashwert-Größe von 256 Bits.

-   [Erstellen eines Hash Objekts](#creating-a-hashing-object)
-   [Erstellen eines wiederverwendbaren Hash Objekts](#creating-a-reusable-hashing-object)
-   [Duplizieren eines Hash Objekts](#duplicating-a-hash-object)

## <a name="creating-a-hashing-object"></a>Erstellen eines Hash Objekts

Führen Sie die folgenden Schritte aus, um einen Hash mithilfe von CNG zu erstellen:

1.  Öffnen Sie einen Algorithmusanbieter, der den gewünschten Algorithmus unterstützt. Typische Hash Algorithmen sind MD2, MD4, MD5, SHA-1 und SHA256. Aufrufen der Funktion " [**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) " und angeben des entsprechenden Algorithmus-Bezeichners im *pszalgid* -Parameter. Die-Funktion gibt ein Handle für den Anbieter zurück.
2.  Führen Sie die folgenden Schritte aus, um das Hash Objekt zu erstellen:

    1.  Rufen Sie die Größe des Objekts ab, indem Sie die Funktion [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) aufrufen, um die Eigenschaft **bcrypt- \_ Objekt \_ Länge** abzurufen.
    2.  Speicherplatz zum Speichern des Hash Objekts zuweisen.
    3.  Erstellen Sie das-Objekt, indem Sie die Funktion " [**BCryptCreateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash) " aufrufen.

3.  Hash der Daten. Dies bedeutet, dass die Funktion " [**BCryptHashData**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcrypthashdata) " einmal oder mehrmals aufgerufen wird. Jeder-Befehl fügt die angegebenen Daten an den Hash an.
4.  Führen Sie die folgenden Schritte aus, um den Hashwert abzurufen:

    1.  Rufen Sie die Größe des Werts ab, indem Sie die Funktion [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) aufrufen, um die Eigenschaft **bcrypt- \_ \_ Hashlänge** abzurufen.
    2.  Speicherplatz zum Speichern des Werts zuweisen.
    3.  Rufen Sie den Hashwert durch Aufrufen der [**BCryptFinishHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptfinishhash) -Funktion ab. Nachdem diese Funktion aufgerufen wurde, ist das Hash Objekt nicht mehr gültig.

5.  Um dieses Verfahren abzuschließen, müssen Sie die folgenden Bereinigungs Schritte ausführen:

    1.  Schließen Sie das Hash Objekt, indem Sie das Hashhandle an die Funktion " [**BCryptDestroyHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdestroyhash) " übergeben.
    2.  Freigeben des Speichers, den Sie für das Hash Objekt zugewiesen haben.
    3.  Wenn Sie keine weiteren Hash Objekte erstellen, schließen Sie den Algorithmusanbieter, indem Sie das Anbieter Handle an die Funktion " [**bcryptclosealgorithmprovider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptclosealgorithmprovider) " übergeben.

        Wenn Sie weitere Hash Objekte erstellen möchten, wird empfohlen, den Algorithmusanbieter wiederzuverwenden, anstatt denselben Algorithmusanbieter mehrmals zu erstellen und zu zerstören.

    4.  Wenn Sie die Verwendung des Hash Wert Speichers abgeschlossen haben, können Sie ihn freigeben.

Im folgenden Beispiel wird gezeigt, wie ein Hashwert mithilfe von CNG erstellt wird.


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



## <a name="creating-a-reusable-hashing-object"></a>Erstellen eines wiederverwendbaren Hash Objekts

Ab Windows 8 und Windows Server 2012 können Sie ein wiederverwendbares Hash Objekt für Szenarien erstellen, in denen Sie mehrere Hashes oder HMACs in schneller Folge berechnen müssen. Geben Sie hierzu beim Aufrufen der Funktion " [**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) " das wieder **\_ \_ verwendbare \_ bcrypt-Hash-Flag** an. Alle Microsoft-Hash Algorithmus Anbieter unterstützen dieses Flag. Ein Hash Objekt, das mit diesem Flag erstellt wurde, kann sofort nach dem Aufruf von [**BCryptFinishHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptfinishhash) wieder verwendet werden, als ob es durch den Aufruf von [**BCryptCreateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash)erstellt wurde. Führen Sie die folgenden Schritte aus, um ein wiederverwendbares Hash Objekt zu erstellen:

1.  Öffnen Sie einen Algorithmusanbieter, der den gewünschten Hash Algorithmus unterstützt. Aufrufen der Funktion " [**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) " und angeben des entsprechenden Algorithmus-Bezeichners im *pszalgid* -Parameter und des **bcrypt-Hash-wieder \_ \_ verwendbaren \_ Flags** im *dwFlags* -Parameter. Die-Funktion gibt ein Handle für den Anbieter zurück.
2.  Führen Sie die folgenden Schritte aus, um das Hash Objekt zu erstellen:

    1.  Rufen Sie die Größe des Objekts ab, indem Sie die Funktion [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) aufrufen, um die Eigenschaft **bcrypt- \_ Objekt \_ Länge** abzurufen.
    2.  Speicherplatz zum Speichern des Hash Objekts zuweisen.
    3.  Erstellen Sie das-Objekt, indem Sie die Funktion " [**BCryptCreateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash) " aufrufen. Geben Sie das **bcrypt- \_ Hash wieder \_ verwendbare \_ Flag** im *dwFlags* -Parameter an.

3.  Hash der Daten durch Aufrufen der [**BCryptHashData**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcrypthashdata) -Funktion.
4.  Führen Sie die folgenden Schritte aus, um den Hashwert abzurufen:

    1.  Rufen Sie die Größe des Hashwerts ab, indem Sie die Funktion [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) aufrufen, um die Eigenschaft **bcrypt- \_ \_ Hashlänge** abzurufen.
    2.  Speicherplatz zum Speichern des Werts zuweisen.
    3.  Rufen Sie den Hashwert ab, indem Sie [**BCryptFinishHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptfinishhash)aufrufen.

5.  Wenn Sie das Hash Objekt mit neuen Daten wieder verwenden möchten, fahren Sie mit Schritt 3 fort.
6.  Um dieses Verfahren abzuschließen, müssen Sie die folgenden Bereinigungs Schritte ausführen:

    1.  Schließen Sie das Hash Objekt, indem Sie das Hashhandle an die Funktion " [**BCryptDestroyHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdestroyhash) " übergeben.
    2.  Freigeben des Speichers, den Sie für das Hash Objekt zugewiesen haben.
    3.  Wenn Sie keine weiteren Hash Objekte erstellen, schließen Sie den Algorithmusanbieter, indem Sie das Anbieter Handle an die Funktion " [**bcryptclosealgorithmprovider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptclosealgorithmprovider) " übergeben.
    4.  Wenn Sie die Verwendung des Hash Wert Speichers abgeschlossen haben, können Sie ihn freigeben.

## <a name="duplicating-a-hash-object"></a>Duplizieren eines Hash Objekts

In einigen Fällen kann es nützlich sein, eine gewisse Menge an allgemeinen Daten zu Hashen und dann zwei separate Hash Objekte aus den gemeinsamen Daten zu erstellen. Um dies zu erreichen, müssen Sie nicht zwei separate Hash Objekte erstellen und die allgemeinen Daten zweimal hashten. Sie können ein einzelnes Hash Objekt erstellen und dem Hash Objekt alle allgemeinen Daten hinzufügen. Anschließend können Sie die Funktion " [**bcryptduplierehash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptduplicatehash) " verwenden, um ein Duplikat des ursprünglichen Hash Objekts zu erstellen. Das doppelte Hash Objekt enthält die gleichen Zustandsinformationen und Hash Daten wie das ursprüngliche, aber es handelt sich um ein vollständig unabhängiges Hash Objekt. Sie können jetzt den einzelnen Hash Objekten die eindeutigen Daten hinzufügen und den Hashwert abrufen, wie im Beispiel gezeigt. Diese Vorgehensweise ist nützlich, wenn ein Hashwert für eine möglicherweise große Menge an allgemeinen Daten erfolgt. Sie müssen die allgemeinen Daten nur einmal zum ursprünglichen Hash hinzufügen. Anschließend können Sie das Hash Objekt duplizieren, um ein eindeutiges Hash Objekt zu erhalten.

 

 
