---
title: Verschlüsseln und Importieren von Medien Beispielen
description: Verschlüsseln und Importieren von Medien Beispielen
ms.assetid: f9784c9a-c672-432d-a3ad-eb2ed73ac523
keywords:
- Windows Media-Format-SDK, DRM-Import
- SDK für Windows Media-Format, importieren
- Windows Media-Format-SDK, Verschlüsseln von Medien Beispielen
- Digital Rights Management (DRM), importieren
- DRM (Digital Rights Management), importieren
- Digital Rights Management (DRM), Verschlüsseln von Medien Beispielen
- DRM (Digital Rights Management), Verschlüsseln von Medien Beispielen
- Erweiterte APIs für den DRM-Client, Import
- Erweiterte Client-APIs, importieren
- Erweiterte APIs für den DRM-Client, Verschlüsseln von Medien Beispielen
- Erweiterte Client-APIs, Verschlüsseln von Medien Beispielen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 473db9580990b62818842aaa5eeea3e82f38c5ad
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104389863"
---
# <a name="encrypting-and-importing-media-samples"></a><span data-ttu-id="1e971-114">Verschlüsseln und Importieren von Medien Beispielen</span><span class="sxs-lookup"><span data-stu-id="1e971-114">Encrypting and Importing Media Samples</span></span>

<span data-ttu-id="1e971-115">Sie müssen für jedes Medien Beispiel, das Sie mithilfe von Windows Media DRM verschlüsseln, einen Salt-Wert generieren, der streng größer als der vorherige ist (monoton erhöht).</span><span class="sxs-lookup"><span data-stu-id="1e971-115">For each media sample that you encrypt using Windows Media DRM, you must generate a salt value that is strictly bigger than the previous one (monotonically increasing).</span></span> <span data-ttu-id="1e971-116">Verwenden Sie den neuen Salt-Wert, um einen transitiven Verschlüsselungsschlüssel zu erstellen, indem Sie den SHA-1-Verschlüsselungsalgorithmus auf den Initialisierungs Vektor anwenden, der mit dem Salt-Wert verkettet ist.</span><span class="sxs-lookup"><span data-stu-id="1e971-116">Use the new salt value to create a transitory encryption key by applying the SHA-1 encryption algorithm to the initialization vector concatenated with the salt value.</span></span>

<span data-ttu-id="1e971-117">Verschlüsseln Sie anschließend das Beispiel gemäß dem RC4-Algorithmus, indem Sie den generierten vorübergehendes-Schlüssel verwenden.</span><span class="sxs-lookup"><span data-stu-id="1e971-117">Next, encrypt the sample according to the RC4 algorithm using the generated transitory key.</span></span> <span data-ttu-id="1e971-118">Bevor das Beispiel an das SDK übermittelt wird, muss die Anwendung den Salt-Wert dem Beispiel zuordnen, indem ein Erweiterungs Attribut festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="1e971-118">Before the sample is passed to the SDK, your application must associate the salt value with the sample by setting an extension attribute.</span></span>

<span data-ttu-id="1e971-119">Hier finden Sie die Schritte zum Verschlüsseln von Medien Beispielen:</span><span class="sxs-lookup"><span data-stu-id="1e971-119">Here are the steps for encrypting media samples:</span></span>

1.  <span data-ttu-id="1e971-120">Ruft die **QueryInterface** -Methode des Sample-Objekts auf, um die [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) -Schnittstelle abzurufen.</span><span class="sxs-lookup"><span data-stu-id="1e971-120">Call the **QueryInterface** method of the sample object to get the [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) interface.</span></span>
2.  <span data-ttu-id="1e971-121">Erhöhen Sie den Salt-Wert.</span><span class="sxs-lookup"><span data-stu-id="1e971-121">Increment the salt value.</span></span>
3.  <span data-ttu-id="1e971-122">Verschlüsseln Sie das Beispiel mit einem RC1-Verschlüsselungsalgorithmus.</span><span class="sxs-lookup"><span data-stu-id="1e971-122">Encrypt the sample using an RC1 encryption algorithm.</span></span> <span data-ttu-id="1e971-123">Für die Verschlüsselung erstellen Sie einen Schlüssel, indem Sie den Initialisierungs Vektor und den Salt-Wert verketten.</span><span class="sxs-lookup"><span data-stu-id="1e971-123">For the encryption you create a key by concatenating the initialization vector and the salt value.</span></span>
4.  <span data-ttu-id="1e971-124">Geben Sie den Salt-Wert für das SDK durch Aufrufen von [**inssbuffer:: SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty)an.</span><span class="sxs-lookup"><span data-stu-id="1e971-124">Provide the salt value to the SDK by calling [**INSSBuffer::SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1e971-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1e971-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1e971-126">**DRM-Import**</span><span class="sxs-lookup"><span data-stu-id="1e971-126">**DRM Import**</span></span>](drm-import.md)
</dt> <dt>

[<span data-ttu-id="1e971-127">**Beispiel für eine Beispiel Verschlüsselung für Medien**</span><span class="sxs-lookup"><span data-stu-id="1e971-127">**Media Sample Encryption Example**</span></span>](media-sample-encryption-example.md)
</dt> </dl>

 

 




