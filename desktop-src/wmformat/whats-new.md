---
title: Neuigkeiten (Windows Media-Format 11 SDK)
description: Neuerungen
ms.assetid: af04b99a-4653-4c82-944a-7005cf1181fe
keywords:
- Windows Media-Format-SDK, Neuerungen
- Windows Media-Format-SDK, Features
- Windows Media-Format-SDK, neue Funktionen
- Windows Media-Format-SDK, erweiterte Client-APIs
- Windows Media-Format-SDK, DRM-Updates
- Windows Media-Format-SDK, Codec-Updates
- Windows Media-Format-SDK, Miniaturbilder
- Digital Rights Management (DRM), neue Features
- DRM (Digital Rights Management), neue Features
- Miniaturansichtsbilder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f63d85f00f89f940ab22754d1f6f458430868d7c
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "103739504"
---
# <a name="whats-new-windows-media-format-11-sdk"></a><span data-ttu-id="88285-113">Neuigkeiten (Windows Media-Format 11 SDK)</span><span class="sxs-lookup"><span data-stu-id="88285-113">What's New (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="88285-114">Das SDK für Windows Media-Format 11 führt neue Features für Digital Rights Management (DRM) ein.</span><span class="sxs-lookup"><span data-stu-id="88285-114">The Windows Media Format 11 SDK introduces new digital rights management (DRM) features.</span></span> <span data-ttu-id="88285-115">Die folgenden Änderungen wurden seit der Version 9,5 an dem SDK vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="88285-115">The following changes have been made to the SDK since the 9.5 release.</span></span>

## <a name="windows-media-drm-client-extended-apis"></a><span data-ttu-id="88285-116">Erweiterte APIs für den Windows Media DRM-Client</span><span class="sxs-lookup"><span data-stu-id="88285-116">Windows Media DRM Client Extended APIs</span></span>

<span data-ttu-id="88285-117">Das SDK für Windows Media-Format 11 ist mit einem neuen Satz von DRM-APIs ausgeliefert.</span><span class="sxs-lookup"><span data-stu-id="88285-117">The Windows Media Format 11 SDK ships with a new set of DRM APIs.</span></span> <span data-ttu-id="88285-118">Diese APIs werden in ihrer eigenen Bibliothek implementiert.</span><span class="sxs-lookup"><span data-stu-id="88285-118">These APIs are implemented in their own library.</span></span> <span data-ttu-id="88285-119">Viele der DRM-Features, die von den Objekten des Windows Media Format SDK unterstützt werden, werden auch von den erweiterten APIs des Windows Media DRM-Clients unterstützt.</span><span class="sxs-lookup"><span data-stu-id="88285-119">Many of the DRM features supported by the objects of the Windows Media Format SDK are also supported by the Windows Media DRM Client Extended APIs.</span></span> <span data-ttu-id="88285-120">Der Hauptunterschied zwischen den neuen APIs besteht darin, dass Sie sich nicht darauf verlassen, dass eine ASF-Datei funktioniert.</span><span class="sxs-lookup"><span data-stu-id="88285-120">The primary difference in the new APIs is that they do not rely on having an ASF file to work.</span></span> <span data-ttu-id="88285-121">Stattdessen befassen sich die neuen APIs direkt mit dem lokalen Lizenz Speicher, wobei häufig die Schlüssel-ID zur Identifizierung von Lizenzen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="88285-121">Instead, the new APIs deal with the local license store directly, often using the key ID to identify licenses.</span></span>

<span data-ttu-id="88285-122">Weitere Informationen finden Sie in der Dokumentation zu [erweiterten APIs für den Windows Media DRM-Client](windows-media-drm-client-extended-apis.md) .</span><span class="sxs-lookup"><span data-stu-id="88285-122">For more information, see the [Windows Media DRM Client Extended APIs](windows-media-drm-client-extended-apis.md) documentation.</span></span>

## <a name="updated-codecs"></a><span data-ttu-id="88285-123">Aktualisierte Codecs</span><span class="sxs-lookup"><span data-stu-id="88285-123">Updated Codecs</span></span>

<span data-ttu-id="88285-124">Der erweiterte profilcodec von Windows Media Video 9 wurde aktualisiert, um einen komprimierten Bitstream zu erstellen, der mit dem veröffentlichten SMPTE VC-1-Standard kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="88285-124">The Windows Media Video 9 Advanced Profile codec has been updated to produce a compressed bit stream that is compliant with the published SMPTE VC-1 standard.</span></span>

<span data-ttu-id="88285-125">Der Windows Media Audio 10 Professional-Codec ist auch in dieser Version des SDK enthalten.</span><span class="sxs-lookup"><span data-stu-id="88285-125">The Windows Media Audio 10 Professional codec is also included in this release of the SDK.</span></span> <span data-ttu-id="88285-126">Der neue Audiocodec bietet verbesserte Qualität bei niedrigeren Bitraten.</span><span class="sxs-lookup"><span data-stu-id="88285-126">The new audio codec features improved quality at lower bit rates.</span></span>

## <a name="thumbnail-right"></a><span data-ttu-id="88285-127">Miniaturansicht rechts</span><span class="sxs-lookup"><span data-stu-id="88285-127">Thumbnail Right</span></span>

<span data-ttu-id="88285-128">Anwendungen können eine neue DRM-Aktion zum Lesen aus dem Video anfordern, um ein Miniaturbild zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="88285-128">Applications can request a new DRM action to read from video to create a thumbnail image.</span></span> <span data-ttu-id="88285-129">Dadurch können Anwendungen Miniaturbilder für Videodateien erstellen und anzeigen, ohne die Datei für die Wiedergabe zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="88285-129">This enables applications to create and display thumbnail images for video files without opening the file for playback.</span></span>

## <a name="related-topics"></a><span data-ttu-id="88285-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="88285-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="88285-131">**Informationen zum Windows Media-Format-SDK**</span><span class="sxs-lookup"><span data-stu-id="88285-131">**About the Windows Media Format SDK**</span></span>](about-the-windows-media-format-sdk.md)
</dt> </dl>

 

 




