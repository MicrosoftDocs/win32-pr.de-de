---
description: WST-Codec-Filter
ms.assetid: 0a06acbf-b842-4ab6-bcf9-d2d006301d83
title: WST-Codec-Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 338db987986a5f4706c144907d122eec3a0615a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349798"
---
# <a name="wst-codec-filter"></a><span data-ttu-id="a6136-103">WST-Codec-Filter</span><span class="sxs-lookup"><span data-stu-id="a6136-103">WST Codec Filter</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a6136-104">Diese Komponente wurde aus Windows Vista und höheren Betriebssystemen entfernt.</span><span class="sxs-lookup"><span data-stu-id="a6136-104">This component has been removed from Windows Vista and later operating systems.</span></span> <span data-ttu-id="a6136-105">Es ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a6136-105">It is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span>

 

<span data-ttu-id="a6136-106">Ab Windows Vista wird dieser Filter durch den vbicodec-Filter ersetzt, der in der Dokumentation zu Microsoft TV-Technologien dokumentiert ist.</span><span class="sxs-lookup"><span data-stu-id="a6136-106">Starting in Windows Vista, this filter is replaced by the VBICodec filter, which is documented in the Microsoft TV Technologies documentation.</span></span>

<span data-ttu-id="a6136-107">Der Weltstandard-Teletext (WST) ist der Europäische Standard für die Datenübertragung mithilfe von VBI auf PAL-Analog Fernsehsignale.</span><span class="sxs-lookup"><span data-stu-id="a6136-107">World Standard Teletext (WST) is the European standard for data transmission using VBI on PAL analog television signals.</span></span> <span data-ttu-id="a6136-108">Untertitel und Datendienste werden mithilfe dieses Standards bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="a6136-108">Both captioning and data services are provided using this standard.</span></span> <span data-ttu-id="a6136-109">Der WST-Codec ist ein kernelmodusfilter, der unformatierte VBI-Beispiele und optional decodierte teletextbeispiele aus dem Erfassungs Filter über den [Tee/Sink-to-Sink-konverterfilter](tee-sink-to-sink-converter.md) empfängt.</span><span class="sxs-lookup"><span data-stu-id="a6136-109">The WST Codec is a kernel-mode filter that receives raw VBI samples and, optionally, decoded Teletext samples from the Capture Filter via the [Tee/Sink-to-Sink Converter](tee-sink-to-sink-converter.md) filter.</span></span> <span data-ttu-id="a6136-110">Dieser Codec decodiert und/oder dupliziert die von decodierten und vorwärts Fehler korrigierten Teletextdaten für den [WST-Decoderfilter](wst-decoder-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="a6136-110">This codec decodes and/or duplicates the decoded and forward-error-corrected Teletext data for the [WST Decoder](wst-decoder-filter.md) filter.</span></span> <span data-ttu-id="a6136-111">Der WST-Codec entspricht dem CC-Decoderfilter für NTSC-Übertragungen.</span><span class="sxs-lookup"><span data-stu-id="a6136-111">The WST Codec corresponds to the CC Decoder filter for NTSC transmissions.</span></span> <span data-ttu-id="a6136-112">Der WST-Decoder entspricht dem " [Line 21](line-21-decoder-filter.md) "-Decoder für NTSC; Diese Filter erstellen die Bitmaps, die an den Overlay-Mixer oder den Video Mischungs-Renderer gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="a6136-112">The WST Decoder corresponds to the [Line 21 Decoder](line-21-decoder-filter.md) for NTSC; these filters create the bitmaps that are sent to the Overlay Mixer or the Video Mixing Renderer.</span></span>

<span data-ttu-id="a6136-113">Dieser Filter verfügt über zwei Eingabe Pins: VBI und HWCC.</span><span class="sxs-lookup"><span data-stu-id="a6136-113">This filter has two input pins, VBI and HWCC.</span></span> <span data-ttu-id="a6136-114">Die VBI-PIN wird für unformatierte VBI-Daten verwendet, und die HWCC-PIN wird verwendet, wenn die VBI-Decodierung mithilfe des Erfassungs Filters auf der Hardware ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a6136-114">The VBI pin is used for raw VBI data, and the HWCC pin is used when the VBI decoding is performed in hardware by the capture filter.</span></span> <span data-ttu-id="a6136-115">Wenn die Daten in der HWCC-Pin empfangen werden, arbeitet der WST-Codec im Pass-Through-Modus und sendet die Daten direkt an den WST-Decoder, ohne ihn in irgendeiner Weise zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="a6136-115">When the data is received on the HWCC pin, the WST Codec operates in "pass-through" mode, and sends the data directly to the WST Decoder without processing it in any way.</span></span> <span data-ttu-id="a6136-116">Wenn der Erfassungs Filter eine HWCC-Pin verfügbar macht, muss Sie direkt mit der entsprechenden PIN auf dem WST-Codec verbunden werden.</span><span class="sxs-lookup"><span data-stu-id="a6136-116">If the capture filter exposes an HWCC pin, it must be connected directly to the corresponding pin on the WST Codec.</span></span>

<span data-ttu-id="a6136-117">Der WST-Codec-Filter wird in der Filterkategorie "WDM Streaming VBI Codecs" (**am \_ kscategory \_ vbicodec**) angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a6136-117">The WST Codec filter appears in the "WDM Streaming VBI Codecs" filter category (**AM\_KSCATEGORY\_VBICODEC**).</span></span>

<span data-ttu-id="a6136-118">Da es sich hierbei um einen Kernel Modus-Filter handelt, können Anwendungen ihn nicht direkt mithilfe von **cokreateinstance** erstellen.</span><span class="sxs-lookup"><span data-stu-id="a6136-118">Because this is a kernel-mode filter, applications cannot create it directly using **CoCreateInstance**.</span></span> <span data-ttu-id="a6136-119">Verwenden Sie stattdessen den [Enumerator "System Geräte](system-device-enumerator.md)".</span><span class="sxs-lookup"><span data-stu-id="a6136-119">Instead, use the [System Device Enumerator](system-device-enumerator.md).</span></span> <span data-ttu-id="a6136-120">Weitere Informationen finden Sie unter [Erstellen von Kernel-Mode filtern](creating-kernel-mode-filters.md).</span><span class="sxs-lookup"><span data-stu-id="a6136-120">For more information, see [Creating Kernel-Mode Filters](creating-kernel-mode-filters.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a6136-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a6136-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a6136-122">DirectShow-Filter</span><span class="sxs-lookup"><span data-stu-id="a6136-122">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="a6136-123">Anzeigen von World Standard-Teletext</span><span class="sxs-lookup"><span data-stu-id="a6136-123">Viewing World Standard Teletext</span></span>](viewing-world-standard-teletext.md)
</dt> </dl>

 

 



