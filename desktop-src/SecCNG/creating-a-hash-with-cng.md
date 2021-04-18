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
# <a name="creating-a-hash-with-cng"></a><span data-ttu-id="b3d93-103">Erstellen eines Hash mit CNG</span><span class="sxs-lookup"><span data-stu-id="b3d93-103">Creating a Hash with CNG</span></span>

<span data-ttu-id="b3d93-104">Bei einem [*Hash*](/windows/desktop/SecGloss/h-gly) handelt es sich um einen unidirektionalen Vorgang, der für einen Datenblock ausgeführt wird, um einen eindeutigen Hashwert zu erstellen, der den Inhalt der Daten darstellt.</span><span class="sxs-lookup"><span data-stu-id="b3d93-104">A [*hash*](/windows/desktop/SecGloss/h-gly) is a one way operation that is performed on a block of data to create a unique hash value that represents the contents of the data.</span></span> <span data-ttu-id="b3d93-105">Unabhängig von der Durchführung des Hashwerts erzeugt derselbe Hash Algorithmus, der für die gleichen Daten ausgeführt wird, immer denselben [*Hashwert*](/windows/desktop/SecGloss/h-gly) .</span><span class="sxs-lookup"><span data-stu-id="b3d93-105">No matter when the hash is performed, the same [*hashing algorithm*](/windows/desktop/SecGloss/h-gly) performed on the same data will always produce the same hash value.</span></span> <span data-ttu-id="b3d93-106">Wenn eine der Daten geändert wird, ändert sich der Hashwert entsprechend.</span><span class="sxs-lookup"><span data-stu-id="b3d93-106">If any of the data changes, the hash value will change appropriately.</span></span>

<span data-ttu-id="b3d93-107">Hashes sind nicht für die Verschlüsselung von Daten nützlich, da Sie nicht zum Reproduzieren der ursprünglichen Daten aus dem Hashwert verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b3d93-107">Hashes are not useful for encrypting data because they are not intended to be used to reproduce the original data from the hash value.</span></span> <span data-ttu-id="b3d93-108">Hashes sind besonders nützlich, um die Integrität der Daten zu überprüfen, wenn Sie mit einem asymmetrischen Signatur Algorithmus verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b3d93-108">Hashes are most useful to verify the integrity of the data when used with an asymmetric signing algorithm.</span></span> <span data-ttu-id="b3d93-109">Wenn Sie z. b. einen Hashwert für eine Textnachricht, den Hash signiert und den Hashwert mit Vorzeichen mit der ursprünglichen Nachricht eingefügt haben, könnte der Empfänger den signierten Hash überprüfen, den Hashwert für die empfangene Nachricht erstellen und diesen Hashwert mit dem mit Vorzeichen signierten Hashwert vergleichen, der in der ursprünglichen Nachricht enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="b3d93-109">For example, if you hashed a text message, signed the hash, and included the signed hash value with the original message, the recipient could verify the signed hash, create the hash value for the received message, and then compare this hash value with the signed hash value included with the original message.</span></span> <span data-ttu-id="b3d93-110">Wenn die beiden Hashwerte identisch sind, kann der Empfänger sicher sein, dass die ursprüngliche Nachricht nicht geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="b3d93-110">If the two hash values are identical, the recipient can be reasonably sure that the original message has not been modified.</span></span>

<span data-ttu-id="b3d93-111">Die Größe des Hashwerts ist für einen bestimmten Hash Algorithmus korrigiert.</span><span class="sxs-lookup"><span data-stu-id="b3d93-111">The size of the hash value is fixed for a particular hashing algorithm.</span></span> <span data-ttu-id="b3d93-112">Dies bedeutet, dass unabhängig davon, wie groß oder klein der Datenblock ist, der Hashwert immer dieselbe Größe hat.</span><span class="sxs-lookup"><span data-stu-id="b3d93-112">What this means is that no matter how large or small the data block is, the hash value will always be the same size.</span></span> <span data-ttu-id="b3d93-113">Der SHA256-Hash Algorithmus hat z. b. eine Hashwert-Größe von 256 Bits.</span><span class="sxs-lookup"><span data-stu-id="b3d93-113">As an example, the SHA256 hashing algorithm has a hash value size of 256 bits.</span></span>

-   [<span data-ttu-id="b3d93-114">Erstellen eines Hash Objekts</span><span class="sxs-lookup"><span data-stu-id="b3d93-114">Creating a Hashing Object</span></span>](#creating-a-hashing-object)
-   [<span data-ttu-id="b3d93-115">Erstellen eines wiederverwendbaren Hash Objekts</span><span class="sxs-lookup"><span data-stu-id="b3d93-115">Creating a Reusable Hashing Object</span></span>](#creating-a-reusable-hashing-object)
-   [<span data-ttu-id="b3d93-116">Duplizieren eines Hash Objekts</span><span class="sxs-lookup"><span data-stu-id="b3d93-116">Duplicating a Hash Object</span></span>](#duplicating-a-hash-object)

## <a name="creating-a-hashing-object"></a><span data-ttu-id="b3d93-117">Erstellen eines Hash Objekts</span><span class="sxs-lookup"><span data-stu-id="b3d93-117">Creating a Hashing Object</span></span>

<span data-ttu-id="b3d93-118">Führen Sie die folgenden Schritte aus, um einen Hash mithilfe von CNG zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="b3d93-118">To create a hash using CNG, perform the following steps:</span></span>

1.  <span data-ttu-id="b3d93-119">Öffnen Sie einen Algorithmusanbieter, der den gewünschten Algorithmus unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b3d93-119">Open an algorithm provider that supports the desired algorithm.</span></span> <span data-ttu-id="b3d93-120">Typische Hash Algorithmen sind MD2, MD4, MD5, SHA-1 und SHA256.</span><span class="sxs-lookup"><span data-stu-id="b3d93-120">Typical hashing algorithms include MD2, MD4, MD5, SHA-1, and SHA256.</span></span> <span data-ttu-id="b3d93-121">Aufrufen der Funktion " [**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) " und angeben des entsprechenden Algorithmus-Bezeichners im *pszalgid* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="b3d93-121">Call the [**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) function and specify the appropriate algorithm identifier in the *pszAlgId* parameter.</span></span> <span data-ttu-id="b3d93-122">Die-Funktion gibt ein Handle für den Anbieter zurück.</span><span class="sxs-lookup"><span data-stu-id="b3d93-122">The function returns a handle to the provider.</span></span>
2.  <span data-ttu-id="b3d93-123">Führen Sie die folgenden Schritte aus, um das Hash Objekt zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="b3d93-123">Perform the following steps to create the hashing object:</span></span>

    1.  <span data-ttu-id="b3d93-124">Rufen Sie die Größe des Objekts ab, indem Sie die Funktion [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) aufrufen, um die Eigenschaft **bcrypt- \_ Objekt \_ Länge** abzurufen.</span><span class="sxs-lookup"><span data-stu-id="b3d93-124">Obtain the size of the object by calling the [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) function to retrieve the **BCRYPT\_OBJECT\_LENGTH** property.</span></span>
    2.  <span data-ttu-id="b3d93-125">Speicherplatz zum Speichern des Hash Objekts zuweisen.</span><span class="sxs-lookup"><span data-stu-id="b3d93-125">Allocate memory to hold the hash object.</span></span>
    3.  <span data-ttu-id="b3d93-126">Erstellen Sie das-Objekt, indem Sie die Funktion " [**BCryptCreateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash) " aufrufen.</span><span class="sxs-lookup"><span data-stu-id="b3d93-126">Create the object by calling the [**BCryptCreateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash) function.</span></span>

3.  <span data-ttu-id="b3d93-127">Hash der Daten.</span><span class="sxs-lookup"><span data-stu-id="b3d93-127">Hash the data.</span></span> <span data-ttu-id="b3d93-128">Dies bedeutet, dass die Funktion " [**BCryptHashData**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcrypthashdata) " einmal oder mehrmals aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="b3d93-128">This involves calling the [**BCryptHashData**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcrypthashdata) function one or more times.</span></span> <span data-ttu-id="b3d93-129">Jeder-Befehl fügt die angegebenen Daten an den Hash an.</span><span class="sxs-lookup"><span data-stu-id="b3d93-129">Each call appends the specified data to the hash.</span></span>
4.  <span data-ttu-id="b3d93-130">Führen Sie die folgenden Schritte aus, um den Hashwert abzurufen:</span><span class="sxs-lookup"><span data-stu-id="b3d93-130">Perform the following steps to obtain the hash value:</span></span>

    1.  <span data-ttu-id="b3d93-131">Rufen Sie die Größe des Werts ab, indem Sie die Funktion [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) aufrufen, um die Eigenschaft **bcrypt- \_ \_ Hashlänge** abzurufen.</span><span class="sxs-lookup"><span data-stu-id="b3d93-131">Retrieve the size of the value by calling the [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) function to get the **BCRYPT\_HASH\_LENGTH** property.</span></span>
    2.  <span data-ttu-id="b3d93-132">Speicherplatz zum Speichern des Werts zuweisen.</span><span class="sxs-lookup"><span data-stu-id="b3d93-132">Allocate memory to hold the value.</span></span>
    3.  <span data-ttu-id="b3d93-133">Rufen Sie den Hashwert durch Aufrufen der [**BCryptFinishHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptfinishhash) -Funktion ab.</span><span class="sxs-lookup"><span data-stu-id="b3d93-133">Retrieve the hash value by calling the [**BCryptFinishHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptfinishhash) function.</span></span> <span data-ttu-id="b3d93-134">Nachdem diese Funktion aufgerufen wurde, ist das Hash Objekt nicht mehr gültig.</span><span class="sxs-lookup"><span data-stu-id="b3d93-134">After this function has been called, the hash object is no longer valid.</span></span>

5.  <span data-ttu-id="b3d93-135">Um dieses Verfahren abzuschließen, müssen Sie die folgenden Bereinigungs Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="b3d93-135">To complete this procedure, you must perform the following cleanup steps:</span></span>

    1.  <span data-ttu-id="b3d93-136">Schließen Sie das Hash Objekt, indem Sie das Hashhandle an die Funktion " [**BCryptDestroyHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdestroyhash) " übergeben.</span><span class="sxs-lookup"><span data-stu-id="b3d93-136">Close the hash object by passing the hash handle to the [**BCryptDestroyHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdestroyhash) function.</span></span>
    2.  <span data-ttu-id="b3d93-137">Freigeben des Speichers, den Sie für das Hash Objekt zugewiesen haben.</span><span class="sxs-lookup"><span data-stu-id="b3d93-137">Free the memory you allocated for the hash object.</span></span>
    3.  <span data-ttu-id="b3d93-138">Wenn Sie keine weiteren Hash Objekte erstellen, schließen Sie den Algorithmusanbieter, indem Sie das Anbieter Handle an die Funktion " [**bcryptclosealgorithmprovider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptclosealgorithmprovider) " übergeben.</span><span class="sxs-lookup"><span data-stu-id="b3d93-138">If you will not be creating any more hash objects, close the algorithm provider by passing the provider handle to the [**BCryptCloseAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptclosealgorithmprovider) function.</span></span>

        <span data-ttu-id="b3d93-139">Wenn Sie weitere Hash Objekte erstellen möchten, wird empfohlen, den Algorithmusanbieter wiederzuverwenden, anstatt denselben Algorithmusanbieter mehrmals zu erstellen und zu zerstören.</span><span class="sxs-lookup"><span data-stu-id="b3d93-139">If you will be creating more hash objects, we suggest you reuse the algorithm provider rather than creating and destroying the same type of algorithm provider many times.</span></span>

    4.  <span data-ttu-id="b3d93-140">Wenn Sie die Verwendung des Hash Wert Speichers abgeschlossen haben, können Sie ihn freigeben.</span><span class="sxs-lookup"><span data-stu-id="b3d93-140">When you have finished using the hash value memory, free it.</span></span>

<span data-ttu-id="b3d93-141">Im folgenden Beispiel wird gezeigt, wie ein Hashwert mithilfe von CNG erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="b3d93-141">The following example shows how to create a hash value by using CNG.</span></span>


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



## <a name="creating-a-reusable-hashing-object"></a><span data-ttu-id="b3d93-142">Erstellen eines wiederverwendbaren Hash Objekts</span><span class="sxs-lookup"><span data-stu-id="b3d93-142">Creating a Reusable Hashing Object</span></span>

<span data-ttu-id="b3d93-143">Ab Windows 8 und Windows Server 2012 können Sie ein wiederverwendbares Hash Objekt für Szenarien erstellen, in denen Sie mehrere Hashes oder HMACs in schneller Folge berechnen müssen.</span><span class="sxs-lookup"><span data-stu-id="b3d93-143">Beginning with Windows 8 and Windows Server 2012, you can create a reusable hashing object for scenarios that require you to compute multiple hashes or HMACs in rapid succession.</span></span> <span data-ttu-id="b3d93-144">Geben Sie hierzu beim Aufrufen der Funktion " [**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) " das wieder **\_ \_ verwendbare \_ bcrypt-Hash-Flag** an.</span><span class="sxs-lookup"><span data-stu-id="b3d93-144">Do this by specifying the **BCRYPT\_HASH\_REUSABLE\_FLAG** when calling the [**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) function.</span></span> <span data-ttu-id="b3d93-145">Alle Microsoft-Hash Algorithmus Anbieter unterstützen dieses Flag.</span><span class="sxs-lookup"><span data-stu-id="b3d93-145">All Microsoft hash algorithm providers support this flag.</span></span> <span data-ttu-id="b3d93-146">Ein Hash Objekt, das mit diesem Flag erstellt wurde, kann sofort nach dem Aufruf von [**BCryptFinishHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptfinishhash) wieder verwendet werden, als ob es durch den Aufruf von [**BCryptCreateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash)erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="b3d93-146">A hashing object created by using this flag can be reused immediately after calling [**BCryptFinishHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptfinishhash) just as if it had been freshly created by calling [**BCryptCreateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash).</span></span> <span data-ttu-id="b3d93-147">Führen Sie die folgenden Schritte aus, um ein wiederverwendbares Hash Objekt zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="b3d93-147">Perform the following steps to create a reusable hashing object:</span></span>

1.  <span data-ttu-id="b3d93-148">Öffnen Sie einen Algorithmusanbieter, der den gewünschten Hash Algorithmus unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b3d93-148">Open an algorithm provider that supports the desired hashing algorithm.</span></span> <span data-ttu-id="b3d93-149">Aufrufen der Funktion " [**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) " und angeben des entsprechenden Algorithmus-Bezeichners im *pszalgid* -Parameter und des **bcrypt-Hash-wieder \_ \_ verwendbaren \_ Flags** im *dwFlags* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="b3d93-149">Call the [**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) function and specify the appropriate algorithm identifier in the *pszAlgId* parameter and **BCRYPT\_HASH\_REUSABLE\_FLAG** in the *dwFlags* parameter.</span></span> <span data-ttu-id="b3d93-150">Die-Funktion gibt ein Handle für den Anbieter zurück.</span><span class="sxs-lookup"><span data-stu-id="b3d93-150">The function returns a handle to the provider.</span></span>
2.  <span data-ttu-id="b3d93-151">Führen Sie die folgenden Schritte aus, um das Hash Objekt zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="b3d93-151">Perform the following steps to create the hashing object:</span></span>

    1.  <span data-ttu-id="b3d93-152">Rufen Sie die Größe des Objekts ab, indem Sie die Funktion [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) aufrufen, um die Eigenschaft **bcrypt- \_ Objekt \_ Länge** abzurufen.</span><span class="sxs-lookup"><span data-stu-id="b3d93-152">Obtain the size of the object by calling the [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) function to retrieve the **BCRYPT\_OBJECT\_LENGTH** property.</span></span>
    2.  <span data-ttu-id="b3d93-153">Speicherplatz zum Speichern des Hash Objekts zuweisen.</span><span class="sxs-lookup"><span data-stu-id="b3d93-153">Allocate memory to hold the hash object.</span></span>
    3.  <span data-ttu-id="b3d93-154">Erstellen Sie das-Objekt, indem Sie die Funktion " [**BCryptCreateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash) " aufrufen.</span><span class="sxs-lookup"><span data-stu-id="b3d93-154">Create the object by calling the [**BCryptCreateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash) function.</span></span> <span data-ttu-id="b3d93-155">Geben Sie das **bcrypt- \_ Hash wieder \_ verwendbare \_ Flag** im *dwFlags* -Parameter an.</span><span class="sxs-lookup"><span data-stu-id="b3d93-155">Specify **BCRYPT\_HASH\_REUSABLE\_FLAG** in the *dwFlags* parameter.</span></span>

3.  <span data-ttu-id="b3d93-156">Hash der Daten durch Aufrufen der [**BCryptHashData**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcrypthashdata) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="b3d93-156">Hash the data by calling the [**BCryptHashData**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcrypthashdata) function.</span></span>
4.  <span data-ttu-id="b3d93-157">Führen Sie die folgenden Schritte aus, um den Hashwert abzurufen:</span><span class="sxs-lookup"><span data-stu-id="b3d93-157">Perform the following steps to obtain the hash value:</span></span>

    1.  <span data-ttu-id="b3d93-158">Rufen Sie die Größe des Hashwerts ab, indem Sie die Funktion [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) aufrufen, um die Eigenschaft **bcrypt- \_ \_ Hashlänge** abzurufen.</span><span class="sxs-lookup"><span data-stu-id="b3d93-158">Obtain the size of the hash value by calling the [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) function to get the **BCRYPT\_HASH\_LENGTH** property.</span></span>
    2.  <span data-ttu-id="b3d93-159">Speicherplatz zum Speichern des Werts zuweisen.</span><span class="sxs-lookup"><span data-stu-id="b3d93-159">Allocate memory to hold the value.</span></span>
    3.  <span data-ttu-id="b3d93-160">Rufen Sie den Hashwert ab, indem Sie [**BCryptFinishHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptfinishhash)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="b3d93-160">Get the hash value by calling [**BCryptFinishHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptfinishhash).</span></span>

5.  <span data-ttu-id="b3d93-161">Wenn Sie das Hash Objekt mit neuen Daten wieder verwenden möchten, fahren Sie mit Schritt 3 fort.</span><span class="sxs-lookup"><span data-stu-id="b3d93-161">To reuse the hashing object with new data, go to step 3.</span></span>
6.  <span data-ttu-id="b3d93-162">Um dieses Verfahren abzuschließen, müssen Sie die folgenden Bereinigungs Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="b3d93-162">To complete this procedure, you must perform the following cleanup steps:</span></span>

    1.  <span data-ttu-id="b3d93-163">Schließen Sie das Hash Objekt, indem Sie das Hashhandle an die Funktion " [**BCryptDestroyHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdestroyhash) " übergeben.</span><span class="sxs-lookup"><span data-stu-id="b3d93-163">Close the hash object by passing the hash handle to the [**BCryptDestroyHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdestroyhash) function.</span></span>
    2.  <span data-ttu-id="b3d93-164">Freigeben des Speichers, den Sie für das Hash Objekt zugewiesen haben.</span><span class="sxs-lookup"><span data-stu-id="b3d93-164">Free the memory you allocated for the hash object.</span></span>
    3.  <span data-ttu-id="b3d93-165">Wenn Sie keine weiteren Hash Objekte erstellen, schließen Sie den Algorithmusanbieter, indem Sie das Anbieter Handle an die Funktion " [**bcryptclosealgorithmprovider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptclosealgorithmprovider) " übergeben.</span><span class="sxs-lookup"><span data-stu-id="b3d93-165">If you will not be creating any more hash objects, close the algorithm provider by passing the provider handle to the [**BCryptCloseAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptclosealgorithmprovider) function.</span></span>
    4.  <span data-ttu-id="b3d93-166">Wenn Sie die Verwendung des Hash Wert Speichers abgeschlossen haben, können Sie ihn freigeben.</span><span class="sxs-lookup"><span data-stu-id="b3d93-166">When you have finished using the hash value memory, free it.</span></span>

## <a name="duplicating-a-hash-object"></a><span data-ttu-id="b3d93-167">Duplizieren eines Hash Objekts</span><span class="sxs-lookup"><span data-stu-id="b3d93-167">Duplicating a Hash Object</span></span>

<span data-ttu-id="b3d93-168">In einigen Fällen kann es nützlich sein, eine gewisse Menge an allgemeinen Daten zu Hashen und dann zwei separate Hash Objekte aus den gemeinsamen Daten zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b3d93-168">In some circumstances, it may be useful to hash some amount of common data and then create two separate hash objects from the common data.</span></span> <span data-ttu-id="b3d93-169">Um dies zu erreichen, müssen Sie nicht zwei separate Hash Objekte erstellen und die allgemeinen Daten zweimal hashten.</span><span class="sxs-lookup"><span data-stu-id="b3d93-169">You do not have to create two separate hash objects and hash the common data twice to accomplish this.</span></span> <span data-ttu-id="b3d93-170">Sie können ein einzelnes Hash Objekt erstellen und dem Hash Objekt alle allgemeinen Daten hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="b3d93-170">You can create a single hash object and add all of the common data to the hash object.</span></span> <span data-ttu-id="b3d93-171">Anschließend können Sie die Funktion " [**bcryptduplierehash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptduplicatehash) " verwenden, um ein Duplikat des ursprünglichen Hash Objekts zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b3d93-171">Then, you can use the [**BCryptDuplicateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptduplicatehash) function to create a duplicate of the original hash object.</span></span> <span data-ttu-id="b3d93-172">Das doppelte Hash Objekt enthält die gleichen Zustandsinformationen und Hash Daten wie das ursprüngliche, aber es handelt sich um ein vollständig unabhängiges Hash Objekt.</span><span class="sxs-lookup"><span data-stu-id="b3d93-172">The duplicate hash object contains all of the same state information and hashed data as the original, but it is a completely independent hash object.</span></span> <span data-ttu-id="b3d93-173">Sie können jetzt den einzelnen Hash Objekten die eindeutigen Daten hinzufügen und den Hashwert abrufen, wie im Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="b3d93-173">You can now add the unique data to each of the hash objects and obtain the hash value as shown in the example.</span></span> <span data-ttu-id="b3d93-174">Diese Vorgehensweise ist nützlich, wenn ein Hashwert für eine möglicherweise große Menge an allgemeinen Daten erfolgt.</span><span class="sxs-lookup"><span data-stu-id="b3d93-174">This technique is useful when hashing a possibly large amount of common data.</span></span> <span data-ttu-id="b3d93-175">Sie müssen die allgemeinen Daten nur einmal zum ursprünglichen Hash hinzufügen. Anschließend können Sie das Hash Objekt duplizieren, um ein eindeutiges Hash Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="b3d93-175">You only have to add the common data to the original hash one time, and then you can duplicate the hash object to obtain a unique hash object.</span></span>

 

 
