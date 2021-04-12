---
description: Decoder-Schnittstellen
ms.assetid: b88517cc-06fe-4d83-a6a9-76e1f34293f4
title: Decoder-Schnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef90ca2dd521c15460295505a6d5b7ea451c4dba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218037"
---
# <a name="decoder-interfaces"></a><span data-ttu-id="ee240-103">Decoder-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="ee240-103">Decoder Interfaces</span></span>

<span data-ttu-id="ee240-104">In den folgenden Tabellen werden die von Windows Imaging Component (WIC)-Decodern implementierten Schnittstellen angezeigt, und das Klassendiagramm zeigt die Vererbungs Hierarchie.</span><span class="sxs-lookup"><span data-stu-id="ee240-104">The following tables show the interfaces implemented by Windows Imaging Component (WIC) decoders, and the class diagram shows the inheritance hierarchy.</span></span>

<span data-ttu-id="ee240-105">Container-Level Decoder-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="ee240-105">Container-Level Decoder Interfaces</span></span>



| <span data-ttu-id="ee240-106">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="ee240-106">Interface</span></span>                                                                                       | <span data-ttu-id="ee240-107">Aufgaben</span><span class="sxs-lookup"><span data-stu-id="ee240-107">Responsibilities</span></span>                             | <span data-ttu-id="ee240-108">Implementierung</span><span class="sxs-lookup"><span data-stu-id="ee240-108">Implementation</span></span>                                                             |
|-------------------------------------------------------------------------------------------------|----------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="ee240-109">IWICBitmapDecoder</span><span class="sxs-lookup"><span data-stu-id="ee240-109">IWICBitmapDecoder</span></span>](-wic-imp-iwicbitmapdecoder.md)                                             | <span data-ttu-id="ee240-110">Dienste auf Container Ebene</span><span class="sxs-lookup"><span data-stu-id="ee240-110">Container-level services</span></span>                     | <span data-ttu-id="ee240-111">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="ee240-111">Required</span></span>                                                                   |
| [<span data-ttu-id="ee240-112">IWICBitmapCodecProgressNotification</span><span class="sxs-lookup"><span data-stu-id="ee240-112">IWICBitmapCodecProgressNotification</span></span>](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md) | <span data-ttu-id="ee240-113">Unterstützung für die Fortschritts Benachrichtigung & Abbruch</span><span class="sxs-lookup"><span data-stu-id="ee240-113">Progress notification & cancellation support</span></span> | <span data-ttu-id="ee240-114">Empfohlen</span><span class="sxs-lookup"><span data-stu-id="ee240-114">Recommended</span></span>                                                                |
| [<span data-ttu-id="ee240-115">IWICMetadataBlockReader</span><span class="sxs-lookup"><span data-stu-id="ee240-115">IWICMetadataBlockReader</span></span>](-wic-imp-iwicmetadatablockreader.md)                                 | <span data-ttu-id="ee240-116">Metadatenenumeration</span><span class="sxs-lookup"><span data-stu-id="ee240-116">Metadata enumeration</span></span>                         | <span data-ttu-id="ee240-117">Optional (nur für Formate erforderlich, die Metadaten auf Container Ebene unterstützen)</span><span class="sxs-lookup"><span data-stu-id="ee240-117">Optional (Required only for formats that support container-level metadata)</span></span> |



 

<span data-ttu-id="ee240-118">Frame-Level Decoder-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="ee240-118">Frame-Level Decoder Interfaces</span></span>



| <span data-ttu-id="ee240-119">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="ee240-119">Interface</span></span>                                                           | <span data-ttu-id="ee240-120">Aufgaben</span><span class="sxs-lookup"><span data-stu-id="ee240-120">Responsibilities</span></span>          | <span data-ttu-id="ee240-121">Implementierung</span><span class="sxs-lookup"><span data-stu-id="ee240-121">Implementation</span></span>                |
|---------------------------------------------------------------------|---------------------------|-------------------------------|
| [<span data-ttu-id="ee240-122">IWICBitmapFrameDecode</span><span class="sxs-lookup"><span data-stu-id="ee240-122">IWICBitmapFrameDecode</span></span>](-wic-imp-iwicbitmapframedecode.md)         | <span data-ttu-id="ee240-123">Dienste auf Frame-Ebene</span><span class="sxs-lookup"><span data-stu-id="ee240-123">Frame-level services</span></span>      | <span data-ttu-id="ee240-124">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="ee240-124">Required</span></span>                      |
| [<span data-ttu-id="ee240-125">IWICMetadataBlockReader</span><span class="sxs-lookup"><span data-stu-id="ee240-125">IWICMetadataBlockReader</span></span>](-wic-imp-iwicmetadatablockreader.md)     | <span data-ttu-id="ee240-126">Metadatenenumeration</span><span class="sxs-lookup"><span data-stu-id="ee240-126">Metadata enumeration</span></span>      | <span data-ttu-id="ee240-127">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="ee240-127">Required</span></span>                      |
| [<span data-ttu-id="ee240-128">IWICBitmapSourceTransform</span><span class="sxs-lookup"><span data-stu-id="ee240-128">IWICBitmapSourceTransform</span></span>](-wic-imp-iwicbitmapsourcetransform.md) | <span data-ttu-id="ee240-129">Native Decoder-Transformationen</span><span class="sxs-lookup"><span data-stu-id="ee240-129">Native decoder transforms</span></span> | <span data-ttu-id="ee240-130">Empfohlen</span><span class="sxs-lookup"><span data-stu-id="ee240-130">Recommended</span></span>                   |
| [<span data-ttu-id="ee240-131">IWICDevelopRaw</span><span class="sxs-lookup"><span data-stu-id="ee240-131">IWICDevelopRaw</span></span>](-wic-imp-iwicdevelopraw.md)                       | <span data-ttu-id="ee240-132">Rohverarbeitungs Dienste</span><span class="sxs-lookup"><span data-stu-id="ee240-132">Raw processing services</span></span>   | <span data-ttu-id="ee240-133">Nur für RAW-Formate erforderlich</span><span class="sxs-lookup"><span data-stu-id="ee240-133">Required for Raw formats only</span></span> |



 

![WIC-Schnittstellen Vererbungs Hierarchie](graphics/wicinterfaces.png)

## <a name="related-topics"></a><span data-ttu-id="ee240-135">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ee240-135">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="ee240-136">**Licher**</span><span class="sxs-lookup"><span data-stu-id="ee240-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ee240-137">Implementieren eines WIC-Enabled Decoders</span><span class="sxs-lookup"><span data-stu-id="ee240-137">Implementing a WIC-Enabled Decoder</span></span>](-wic-implementingwicdecoder.md)
</dt> <dt>

[<span data-ttu-id="ee240-138">Implementieren von IWICBitmapDecoder</span><span class="sxs-lookup"><span data-stu-id="ee240-138">Implementing IWICBitmapDecoder</span></span>](-wic-imp-iwicbitmapdecoder.md)
</dt> <dt>

[<span data-ttu-id="ee240-139">Schreiben eines WIC-Enabled Codecs</span><span class="sxs-lookup"><span data-stu-id="ee240-139">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="ee240-140">Übersicht über die Windows Imaging-Komponente</span><span class="sxs-lookup"><span data-stu-id="ee240-140">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



