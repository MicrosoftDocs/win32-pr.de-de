---
description: In diesem Abschnitt wird beschrieben, wie eine benutzerdefinierte Media Foundation Transformation (MFT) geschrieben wird.
ms.assetid: a95828d3-afc5-4f6b-aedd-5b6a72621e0e
title: Schreiben eines benutzerdefinierten MFT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d15b9d5ae655ba67d4a526aeb8a82eb9d3912da9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865571"
---
# <a name="writing-a-custom-mft"></a><span data-ttu-id="5b888-103">Schreiben eines benutzerdefinierten MFT</span><span class="sxs-lookup"><span data-stu-id="5b888-103">Writing a Custom MFT</span></span>

<span data-ttu-id="5b888-104">In diesem Abschnitt wird beschrieben, wie eine benutzerdefinierte Media Foundation Transformation (MFT) geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="5b888-104">This section describes how to write a custom Media Foundation Transform (MFT).</span></span>

## <a name="mft-checklist"></a><span data-ttu-id="5b888-105">MFT-Checkliste</span><span class="sxs-lookup"><span data-stu-id="5b888-105">MFT Checklist</span></span>

<span data-ttu-id="5b888-106">Wenn Sie einen benutzerdefinierten MFT implementieren, verwenden Sie die folgende Checkliste, um die Anforderungen zu bestimmen:</span><span class="sxs-lookup"><span data-stu-id="5b888-106">When you implement a custom MFT, use the following checklist to determine the requirements:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5b888-107">Alle MFTs</span><span class="sxs-lookup"><span data-stu-id="5b888-107">All MFTs</span></span></td>
<td><span data-ttu-id="5b888-108">Alle MFTs müssen " <a href="/windows/desktop/api/mftransform/nn-mftransform-imftransform"><strong>IMF Transform</strong></a>" implementieren.</span><span class="sxs-lookup"><span data-stu-id="5b888-108">All MFTs must implement <a href="/windows/desktop/api/mftransform/nn-mftransform-imftransform"><strong>IMFTransform</strong></a>.</span></span><br/> <span data-ttu-id="5b888-109">Die folgenden Themen stellen weitere Informationen zur Implementierung dieser Schnittstelle zur Verfügung:</span><span class="sxs-lookup"><span data-stu-id="5b888-109">The following topics give more information about implementing this interface:</span></span>
<ul>
<li><span data-ttu-id="5b888-110"><a href="basic-mft-processing-model.md">Einfaches MFT-Verarbeitungsmodell</a></span><span class="sxs-lookup"><span data-stu-id="5b888-110"><a href="basic-mft-processing-model.md">Basic MFT Processing Model</a></span></span></li>
<li><span data-ttu-id="5b888-111"><a href="time-stamps-and-durations.md">Zeitstempel und Dauer</a></span><span class="sxs-lookup"><span data-stu-id="5b888-111"><a href="time-stamps-and-durations.md">Time Stamps and Durations</a></span></span></li>
<li><span data-ttu-id="5b888-112"><a href="handling-stream-changes.md">Verarbeiten von streamänderungen</a></span><span class="sxs-lookup"><span data-stu-id="5b888-112"><a href="handling-stream-changes.md">Handling Stream Changes</a></span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b888-113">Encoder und Decoder</span><span class="sxs-lookup"><span data-stu-id="5b888-113">Encoders and decoders</span></span></td>
<td><span data-ttu-id="5b888-114">Anforderungen: siehe <a href="implementing-a-codec-mft.md">Implementieren eines Codec-MFT</a>.</span><span class="sxs-lookup"><span data-stu-id="5b888-114">Requirements: See <a href="implementing-a-codec-mft.md">Implementing a Codec MFT</a>.</span></span><br/> <span data-ttu-id="5b888-115">Empfohlen: Implementieren Sie <a href="/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise"><strong>imfqualityrecommended</strong></a> oder <a href="/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2"><strong>IMFQualityAdvise2</strong></a>, um QoS-Benachrichtigungen (Quality of Service) zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="5b888-115">Recommended: Implement <a href="/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise"><strong>IMFQualityAdvise</strong></a> or <a href="/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2"><strong>IMFQualityAdvise2</strong></a>, to support quality-of-service (QoS) notifications.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b888-116">Video-Decoder und Video Prozessoren</span><span class="sxs-lookup"><span data-stu-id="5b888-116">Video decoders and video processors</span></span></td>
<td><span data-ttu-id="5b888-117">Optional: Unterstützung der DirectX-Video Beschleunigung.</span><span class="sxs-lookup"><span data-stu-id="5b888-117">Optional: Support DirectX Video Acceleration.</span></span><br/>
<ul>
<li><span data-ttu-id="5b888-118"><a href="direct3d-aware-mfts.md">Direct3D-kompatible MFTs</a></span><span class="sxs-lookup"><span data-stu-id="5b888-118"><a href="direct3d-aware-mfts.md">Direct3D-Aware MFTs</a></span></span></li>
<li><span data-ttu-id="5b888-119"><a href="supporting-dxva-2-0-in-media-foundation.md">Unterstützung von DXVA 2,0 in Media Foundation</a></span><span class="sxs-lookup"><span data-stu-id="5b888-119"><a href="supporting-dxva-2-0-in-media-foundation.md">Supporting DXVA 2.0 in Media Foundation</a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b888-120">Hardware-Codecs</span><span class="sxs-lookup"><span data-stu-id="5b888-120">Hardware codecs</span></span></td>
<td><span data-ttu-id="5b888-121">Siehe <a href="hardware-mfts.md">Hardware-MFTs</a>.</span><span class="sxs-lookup"><span data-stu-id="5b888-121">See <a href="hardware-mfts.md">Hardware MFTs</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b888-122">So machen Sie die MFT durch Anwendungen auffindbar...</span><span class="sxs-lookup"><span data-stu-id="5b888-122">To make your MFT discoverable by applications...</span></span></td>
<td><span data-ttu-id="5b888-123">Weitere Informationen finden Sie unter <a href="registering-and-enumerating-mfts.md">registrieren und Auflisten von MFTs</a>.</span><span class="sxs-lookup"><span data-stu-id="5b888-123">See <a href="registering-and-enumerating-mfts.md">Registering and Enumerating MFTs</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b888-124">Asynchrone Datenverarbeitung</span><span class="sxs-lookup"><span data-stu-id="5b888-124">Asynchronous data processing</span></span></td>
<td><span data-ttu-id="5b888-125">Das MFT-Standardmodell verwendet synchrone (blockierende) Aufrufe, um Daten zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="5b888-125">The default MFT model uses synchronous (blocking) calls to process data.</span></span> <span data-ttu-id="5b888-126">Bei einigen MFTs kann die asynchrone Verarbeitung effizienter sein.</span><span class="sxs-lookup"><span data-stu-id="5b888-126">For some MFTs, asynchronous processing can be more efficient.</span></span> <span data-ttu-id="5b888-127">Es ist jedoch auch komplexer, Sie zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="5b888-127">However, it is also more complex to implement.</span></span><br/> <span data-ttu-id="5b888-128">Weitere Informationen finden Sie unter <a href="asynchronous-mfts.md">asynchrone MFTs</a>.</span><span class="sxs-lookup"><span data-stu-id="5b888-128">For more information, see <a href="asynchronous-mfts.md">Asynchronous MFTs</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b888-129">Raten Steuerung, Trick Modus oder umgekehrte Wiedergabe</span><span class="sxs-lookup"><span data-stu-id="5b888-129">Rate control, trick mode, or reverse playback</span></span></td>
<td><span data-ttu-id="5b888-130">Siehe <a href="implementing-rate-control.md">Implementieren der Raten Kontrolle</a>.</span><span class="sxs-lookup"><span data-stu-id="5b888-130">See <a href="implementing-rate-control.md">Implementing Rate Control</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b888-131">Wenn Ihr MFT Threads erstellt...</span><span class="sxs-lookup"><span data-stu-id="5b888-131">If your MFT creates threads...</span></span></td>
<td><span data-ttu-id="5b888-132">Implementieren Sie die <a href="/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient"><strong>imfrealtimeclient</strong></a> -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="5b888-132">Implement the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient"><strong>IMFRealTimeClient</strong></a> interface.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b888-133">Wenn Ihr MFT über Lizenzierungs Einschränkungen verfügt...</span><span class="sxs-lookup"><span data-stu-id="5b888-133">If your MFT has licensing restrictions...</span></span></td>
<td><span data-ttu-id="5b888-134">Verwenden Sie ggf. den Feld-of-use-Mechanismus.</span><span class="sxs-lookup"><span data-stu-id="5b888-134">Consider using the field-of-use mechanism.</span></span> <span data-ttu-id="5b888-135">Siehe <a href="field-of-use-restrictions.md">Einschränkungen für Felder</a>.</span><span class="sxs-lookup"><span data-stu-id="5b888-135">See <a href="field-of-use-restrictions.md">Field of Use Restrictions</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b888-136">Wenn Sie ein vorhandenes DirectX-Medienobjekt (DMO) portieren...</span><span class="sxs-lookup"><span data-stu-id="5b888-136">If you are porting an existing DirectX Media Object (DMO)...</span></span></td>
<td><span data-ttu-id="5b888-137">Weitere Informationen finden Sie <a href="comparison-of-mfts-and-dmos.md">unter Vergleich von MFTs und DMOS</a>.</span><span class="sxs-lookup"><span data-stu-id="5b888-137">See <a href="comparison-of-mfts-and-dmos.md">Comparison of MFTs and DMOs</a>.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="5b888-138">Dieser Abschnitt enthält die folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="5b888-138">This section contains the following topics:</span></span>

-   [<span data-ttu-id="5b888-139">Zeitstempel und Dauer</span><span class="sxs-lookup"><span data-stu-id="5b888-139">Time Stamps and Durations</span></span>](time-stamps-and-durations.md)
-   [<span data-ttu-id="5b888-140">Verarbeiten von streamänderungen</span><span class="sxs-lookup"><span data-stu-id="5b888-140">Handling Stream Changes</span></span>](handling-stream-changes.md)
-   [<span data-ttu-id="5b888-141">Implementieren eines Codec-MFT</span><span class="sxs-lookup"><span data-stu-id="5b888-141">Implementing a Codec MFT</span></span>](implementing-a-codec-mft.md)
-   [<span data-ttu-id="5b888-142">Direct3D-kompatible MFTs</span><span class="sxs-lookup"><span data-stu-id="5b888-142">Direct3D-Aware MFTs</span></span>](direct3d-aware-mfts.md)
-   [<span data-ttu-id="5b888-143">Hardware-MFTs</span><span class="sxs-lookup"><span data-stu-id="5b888-143">Hardware MFTs</span></span>](hardware-mfts.md)
-   [<span data-ttu-id="5b888-144">Codec-Verdienst</span><span class="sxs-lookup"><span data-stu-id="5b888-144">Codec Merit</span></span>](codec-merit.md)

## <a name="related-topics"></a><span data-ttu-id="5b888-145">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5b888-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5b888-146">Media Foundation Transformationen</span><span class="sxs-lookup"><span data-stu-id="5b888-146">Media Foundation Transforms</span></span>](media-foundation-transforms.md)
</dt> </dl>

 

 




