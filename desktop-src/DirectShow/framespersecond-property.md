---
description: Die framesPerSecond-Eigenschaft ruft die Video Frame Rate für den aktuellen DVD-Titel ab.
ms.assetid: c5d36308-1447-4636-9b3a-4a3f93d27789
title: FramesPerSecond (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e00ec3281d88a2901f630c9231edbf1e76a89c23
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106344781"
---
# <a name="framespersecond-property"></a><span data-ttu-id="33357-103">FramesPerSecond (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="33357-103">FramesPerSecond Property</span></span>

> [!Note]  
> <span data-ttu-id="33357-104">Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="33357-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="33357-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="33357-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="33357-106">Die- `FramesPerSecond` Eigenschaft ruft die Video Frame Rate für den aktuellen DVD-Titel ab.</span><span class="sxs-lookup"><span data-stu-id="33357-106">The `FramesPerSecond` property retrieves the video frame rate for the current DVD title.</span></span>

``` syntax
[ iFramesPerSec = ] MSWebDVD.FramesPerSecond
```

## <a name="return-value"></a><span data-ttu-id="33357-107">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="33357-107">Return Value</span></span>

<span data-ttu-id="33357-108">Gibt einen ganzzahligen Wert zurück, der die Video Frame Rate darstellt. entweder 25 oder 30 Frames pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="33357-108">Returns an integer value representing the video frame rate; either 25 or 30 frames per second.</span></span>

## <a name="remarks"></a><span data-ttu-id="33357-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="33357-109">Remarks</span></span>

<span data-ttu-id="33357-110">Diese Eigenschaft ist schreibgeschützt und weist keinen Standardwert auf.</span><span class="sxs-lookup"><span data-stu-id="33357-110">This property is read-only with no default value.</span></span> <span data-ttu-id="33357-111">NTSC-Videosignale werden bei 30 Frames pro Sekunde angezeigt.</span><span class="sxs-lookup"><span data-stu-id="33357-111">NTSC video signals are displayed at 30 frames per second.</span></span> <span data-ttu-id="33357-112">PAL wird bei 25 Frames pro Sekunde angezeigt.</span><span class="sxs-lookup"><span data-stu-id="33357-112">PAL is displayed at 25 frames per second.</span></span> <span data-ttu-id="33357-113">Ein Disc ist für die Wiedergabe in NTSC oder PAL codiert, kann aber nicht auf beiden spielen.</span><span class="sxs-lookup"><span data-stu-id="33357-113">A disc is encoded to play on either NTSC or PAL, but cannot play on both.</span></span>

 

 



