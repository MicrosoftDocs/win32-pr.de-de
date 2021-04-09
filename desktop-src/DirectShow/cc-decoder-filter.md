---
description: CC-Decoderfilter
ms.assetid: 57ef75f6-411c-4b1f-b0dc-ac293ebc0b9c
title: CC-Decoderfilter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d93995207e4f1a397db28f743d1f972b871b0553
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103957788"
---
# <a name="cc-decoder-filter"></a><span data-ttu-id="8a292-103">CC-Decoderfilter</span><span class="sxs-lookup"><span data-stu-id="8a292-103">CC Decoder Filter</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8a292-104">Diese Komponente wurde aus Windows Vista und höheren Betriebssystemen entfernt.</span><span class="sxs-lookup"><span data-stu-id="8a292-104">This component has been removed from Windows Vista and later operating systems.</span></span> <span data-ttu-id="8a292-105">Es ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="8a292-105">It is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span>

 

<span data-ttu-id="8a292-106">Der CC VBI-Decoder ist ein streamklassenfilter im Kernel Modus.</span><span class="sxs-lookup"><span data-stu-id="8a292-106">The CC VBI Decoder is a kernel-mode stream class filter.</span></span> <span data-ttu-id="8a292-107">Es wird in GraphEdit unter der Kategorie "WDM Streaming VBI Codecs" angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8a292-107">It appears in GraphEdit under the "WDM Streaming VBI Codecs" category.</span></span> <span data-ttu-id="8a292-108">Er akzeptiert Beispiel Wellen Formulare, die von einem Erfassungs Filter bereitgestellt werden, und übermittelt decodierte, geschlossene Daten an den [Line 21-Decoder](line-21-decoder-filter.md) und/oder an interessierte Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="8a292-108">It accepts sample waveforms delivered by a capture filter and delivers decoded closed-captioning data to the [Line 21 Decoder](line-21-decoder-filter.md) and/or to interested applications.</span></span>

<span data-ttu-id="8a292-109">Dieser Filter verfügt über zwei Eingabe Pins: VBI und HWCC.</span><span class="sxs-lookup"><span data-stu-id="8a292-109">This filter has two input pins, VBI and HWCC.</span></span> <span data-ttu-id="8a292-110">Die VBI-PIN wird für unformatierte VBI-Daten verwendet, und die HWCC-PIN wird verwendet, wenn die VBI-Decodierung mithilfe des Erfassungs Filters auf der Hardware ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8a292-110">The VBI pin is used for raw VBI data, and the HWCC pin is used when the VBI decoding is performed in hardware by the capture filter.</span></span> <span data-ttu-id="8a292-111">Wenn die Daten in der HWCC-Pin empfangen werden, wird der CC-Decoder im Pass-Through-Modus ausgeführt und sendet die Daten direkt an den "Line 21"-Decoder, ohne Sie zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="8a292-111">When the data is received on the HWCC pin, the CC Decoder operates in "pass-through" mode, and sends the data directly to the Line 21 Decoder without processing it in any way.</span></span> <span data-ttu-id="8a292-112">Wenn der Erfassungs Filter eine HWCC-Pin verfügbar macht, muss Sie direkt mit der entsprechenden PIN im CC-Decoder verbunden werden.</span><span class="sxs-lookup"><span data-stu-id="8a292-112">If the capture filter exposes an HWCC pin, it must be connected directly to the corresponding pin on the CC Decoder.</span></span> <span data-ttu-id="8a292-113">Die PIN-Kategorie lautet **Pinname \_ Video \_ CC \_ Capture**.</span><span class="sxs-lookup"><span data-stu-id="8a292-113">The pin category is **PINNAME\_VIDEO\_CC\_CAPTURE**.</span></span>

<span data-ttu-id="8a292-114">Der CC-Decoder verfügt über bis zu acht Ausgabe Pins, von denen jeder ihre eigenen Zeilen und unter Ströme auswählen kann.</span><span class="sxs-lookup"><span data-stu-id="8a292-114">The CC Decoder has up to eight output pins, each of which can select their own lines and substreams.</span></span> <span data-ttu-id="8a292-115">Der erste Ausgabepin ist mit dem Line-21-Decoder verbunden.</span><span class="sxs-lookup"><span data-stu-id="8a292-115">The first output pin is connected to the Line-21 Decoder.</span></span>

<span data-ttu-id="8a292-116">Der CC-Decoderfilter wird in der Filterkategorie "WDM Streaming VBI Codecs" (**am \_ kscategory \_ vbicodec**) angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8a292-116">The CC Decoder filter appears in the "WDM Streaming VBI Codecs" filter category (**AM\_KSCATEGORY\_VBICODEC**).</span></span>

<span data-ttu-id="8a292-117">Da es sich hierbei um einen Kernel Modus-Filter handelt, können Anwendungen ihn nicht direkt mithilfe von **cokreateinstance** erstellen.</span><span class="sxs-lookup"><span data-stu-id="8a292-117">Because this is a kernel-mode filter, applications cannot create it directly using **CoCreateInstance**.</span></span> <span data-ttu-id="8a292-118">Verwenden Sie stattdessen den [Enumerator "System Geräte](system-device-enumerator.md)".</span><span class="sxs-lookup"><span data-stu-id="8a292-118">Instead, use the [System Device Enumerator](system-device-enumerator.md).</span></span> <span data-ttu-id="8a292-119">Weitere Informationen finden Sie unter [Erstellen von Kernel-Mode filtern](creating-kernel-mode-filters.md).</span><span class="sxs-lookup"><span data-stu-id="8a292-119">For more information, see [Creating Kernel-Mode Filters](creating-kernel-mode-filters.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8a292-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8a292-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8a292-121">DirectShow-Filter</span><span class="sxs-lookup"><span data-stu-id="8a292-121">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="8a292-122">Anzeigen von Untertiteln</span><span class="sxs-lookup"><span data-stu-id="8a292-122">Viewing Closed Captions</span></span>](viewing-closed-captions.md)
</dt> </dl>

 

 



