---
description: Die totaltitletime-Eigenschaft ruft die Gesamt Wiedergabezeit für den aktuellen Titel ab.
ms.assetid: b05bb76b-d4ba-42e6-92ea-8e48f4c8f409
title: Totaltitletime (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73a300a2da8de2698a74e0d72362818bd8a2a5ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865788"
---
# <a name="totaltitletime-property"></a><span data-ttu-id="05e4f-103">Totaltitletime (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="05e4f-103">TotalTitleTime Property</span></span>

> [!Note]  
> <span data-ttu-id="05e4f-104">Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="05e4f-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="05e4f-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="05e4f-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="05e4f-106">Die- `TotalTitleTime` Eigenschaft ruft die Gesamt Wiedergabezeit für den aktuellen Titel ab.</span><span class="sxs-lookup"><span data-stu-id="05e4f-106">The `TotalTitleTime` property retrieves the total playback time for the current title.</span></span>

``` syntax
[ sTotalTime = ] MSWebDVD.TotalTitleTime
```

## <a name="return-value"></a><span data-ttu-id="05e4f-107">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="05e4f-107">Return Value</span></span>

<span data-ttu-id="05e4f-108">Gibt die Gesamt Wiedergabezeit des aktuellen Titels als Zeichenfolge im Format "hh: mm: SS: FF" zurück.</span><span class="sxs-lookup"><span data-stu-id="05e4f-108">Returns the total playing time of the current title as a String in the format "hh:mm:ss:ff".</span></span>

## <a name="remarks"></a><span data-ttu-id="05e4f-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="05e4f-109">Remarks</span></span>

<span data-ttu-id="05e4f-110">Diese Eigenschaft ist schreibgeschützt und weist keinen Standardwert auf.</span><span class="sxs-lookup"><span data-stu-id="05e4f-110">This property is read-only with no default value.</span></span> <span data-ttu-id="05e4f-111">Die zurückgegebene Zeichenfolge hat eine Länge von 11 Zeichen im Format "hh: mm: SS: FF" (Stunden, Minuten, Sekunden, Rahmen).</span><span class="sxs-lookup"><span data-stu-id="05e4f-111">The returned string will be 11 characters long in the format "hh:mm:ss:ff" (hours, minutes, seconds, frames).</span></span>

## <a name="see-also"></a><span data-ttu-id="05e4f-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="05e4f-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05e4f-113">**Playattime**</span><span class="sxs-lookup"><span data-stu-id="05e4f-113">**PlayAtTime**</span></span>](playattime-method.md)
</dt> <dt>

[<span data-ttu-id="05e4f-114">**Playattimeingetitle**</span><span class="sxs-lookup"><span data-stu-id="05e4f-114">**PlayAtTimeInTitle**</span></span>](playattimeintitle-method.md)
</dt> </dl>

 

 



