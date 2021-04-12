---
description: Die playattimeingetitle-Methode startet die Wiedergabe zum angegebenen Zeitpunkt innerhalb des angegebenen Titels.
ms.assetid: 82726885-8393-409b-b8a1-29a8e9e9ac65
title: Playattimeingetitle-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c40373b4327b6df5fc341ca392c223d464a70a8b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104480598"
---
# <a name="playattimeintitle-method"></a><span data-ttu-id="efe6b-103">Playattimeingetitle-Methode</span><span class="sxs-lookup"><span data-stu-id="efe6b-103">PlayAtTimeInTitle Method</span></span>

> [!Note]  
> <span data-ttu-id="efe6b-104">Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="efe6b-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="efe6b-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="efe6b-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="efe6b-106">Die- `PlayAtTimeInTitle` Methode startet die Wiedergabe zum angegebenen Zeitpunkt innerhalb des angegebenen Titels.</span><span class="sxs-lookup"><span data-stu-id="efe6b-106">The `PlayAtTimeInTitle` method starts playback at the specified time within the specified title.</span></span>

``` syntax
MSWebDVD.PlayAtTimeInTitle(sTime, iTitle)
```

## <a name="parameters"></a><span data-ttu-id="efe6b-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="efe6b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="efe6b-108"><span id="sTime"></span><span id="stime"></span><span id="STIME"></span>*stime*</span><span class="sxs-lookup"><span data-stu-id="efe6b-108"><span id="sTime"></span><span id="stime"></span><span id="STIME"></span>*sTime*</span></span>
</dt> <dd>

<span data-ttu-id="efe6b-109">Gibt die Uhrzeit an, zu der die Wiedergabe als Zeichenfolge gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="efe6b-109">Specifies the time at which to start playback as a string.</span></span> <span data-ttu-id="efe6b-110">Die Zeichenfolge muss das Format "hh: mm: SS: FF" aufweisen (Stunden, Minuten, Sekunden, Rahmen angeben).</span><span class="sxs-lookup"><span data-stu-id="efe6b-110">The string must be in the format "hh:mm:ss:ff" (specifying hours, minutes, seconds, frames).</span></span>

</dd> <dt>

<span data-ttu-id="efe6b-111"><span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*ititle*</span><span class="sxs-lookup"><span data-stu-id="efe6b-111"><span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*iTitle*</span></span>
</dt> <dd>

<span data-ttu-id="efe6b-112">Gibt den Index des Titels als Ganzzahl an.</span><span class="sxs-lookup"><span data-stu-id="efe6b-112">Specifies the index of the title as an Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="efe6b-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="efe6b-113">Return Value</span></span>

<span data-ttu-id="efe6b-114">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="efe6b-114">No return value.</span></span>

## <a name="see-also"></a><span data-ttu-id="efe6b-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="efe6b-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efe6b-116">**Currenttitle**</span><span class="sxs-lookup"><span data-stu-id="efe6b-116">**CurrentTitle**</span></span>](currenttitle-property.md)
</dt> <dt>

[<span data-ttu-id="efe6b-117">**Playattime**</span><span class="sxs-lookup"><span data-stu-id="efe6b-117">**PlayAtTime**</span></span>](playattime-method.md)
</dt> <dt>

[<span data-ttu-id="efe6b-118">**Titlesavailable**</span><span class="sxs-lookup"><span data-stu-id="efe6b-118">**TitlesAvailable**</span></span>](titlesavailable-property.md)
</dt> </dl>

 

 



