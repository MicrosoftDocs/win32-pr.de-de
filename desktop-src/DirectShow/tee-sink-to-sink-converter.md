---
description: Tee/Sink-zu-Sink-Konverter
ms.assetid: 8ee5e20c-f37a-4a9b-9382-2ed94333c6ec
title: Tee/Sink-zu-Sink-Konverter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cf85e3eb58f601273ff352a3878d352ca0f0d5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368954"
---
# <a name="teesink-to-sink-converter"></a><span data-ttu-id="bbb69-103">Tee/Sink-zu-Sink-Konverter</span><span class="sxs-lookup"><span data-stu-id="bbb69-103">Tee/Sink-to-Sink Converter</span></span>

<span data-ttu-id="bbb69-104">Der "Tee/Sink-to-Sink"-Konverter ist ein auf einem Kernel Modus basierender, ksproxy-basierter Filter.</span><span class="sxs-lookup"><span data-stu-id="bbb69-104">The Tee/Sink-to-Sink Converter is a kernel-mode, KsProxy-based filter.</span></span> <span data-ttu-id="bbb69-105">Sie wird in analogen Video-TV-Filter Diagrammen verwendet, in denen VBI-Daten gerendert oder aufgezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="bbb69-105">It is used in analog video television filter graphs where VBI data is being rendered or captured.</span></span> <span data-ttu-id="bbb69-106">Der Filter ist mit dem [WDM-Video Erfassungs Filter](wdm-video-capture-filter.md) verbunden und bietet eine effiziente Möglichkeit, Datenströme innerhalb des Kernel Modus zu duplizieren, ohne die aufwendigen Übergänge zwischen Kernel-und Benutzermodus.</span><span class="sxs-lookup"><span data-stu-id="bbb69-106">The filter is connected upstream to the [WDM Video Capture Filter](wdm-video-capture-filter.md) and provides an efficient means to duplicate streams of data within kernel mode without the expensive transitions between kernel and user mode.</span></span> <span data-ttu-id="bbb69-107">Jeder empfangene Datenblock wird an alle Ausgabe Pins übermittelt, und der Downstream-Codec ist für die Suche nach bestimmten VBI-Daten zum Decodieren verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="bbb69-107">It delivers each received data block to all output pins, and the downstream codec is responsible for finding the specific VBI data to decode.</span></span>

<span data-ttu-id="bbb69-108">Der "Tee/Sink-to-Sink"-Konverter wird in der Filterkategorie "WDM-Streaming-Tee/Splitter Geräte" (am \_ kscategory- \_ Splitter) angezeigt.</span><span class="sxs-lookup"><span data-stu-id="bbb69-108">The Tee/Sink-to-Sink Converter appears in the "WDM Streaming Tee/Splitter Devices" filter category (AM\_KSCATEGORY\_SPLITTER).</span></span>

<span data-ttu-id="bbb69-109">Da es sich hierbei um einen Kernel Modus-Filter handelt, können Anwendungen ihn nicht direkt mithilfe von [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)erstellen.</span><span class="sxs-lookup"><span data-stu-id="bbb69-109">Because this is a kernel-mode filter, applications cannot create it directly using [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span> <span data-ttu-id="bbb69-110">Verwenden Sie stattdessen den [Enumerator "System Geräte](system-device-enumerator.md)".</span><span class="sxs-lookup"><span data-stu-id="bbb69-110">Instead, use the [System Device Enumerator](system-device-enumerator.md).</span></span> <span data-ttu-id="bbb69-111">Weitere Informationen finden Sie unter [Erstellen von Kernel-Mode filtern](creating-kernel-mode-filters.md).</span><span class="sxs-lookup"><span data-stu-id="bbb69-111">For more information, see [Creating Kernel-Mode Filters](creating-kernel-mode-filters.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="bbb69-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="bbb69-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bbb69-113">DirectShow-Filter</span><span class="sxs-lookup"><span data-stu-id="bbb69-113">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 
