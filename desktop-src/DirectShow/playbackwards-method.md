---
description: Die playabwärts-Methode startet die Rückwärts Wiedergabe von der aktuellen Position mit der angegebenen Geschwindigkeit.
ms.assetid: 7f8421e7-f835-4a10-a9c9-0e43de159e4f
title: Playrückwärts-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90b396c3829569d3f3ad25f0c0e8718dfd23f268
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104480595"
---
# <a name="playbackwards-method"></a><span data-ttu-id="4c948-103">Playrückwärts-Methode</span><span class="sxs-lookup"><span data-stu-id="4c948-103">PlayBackwards Method</span></span>

> [!Note]  
> <span data-ttu-id="4c948-104">Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="4c948-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="4c948-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="4c948-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="4c948-106">Die- `PlayBackwards` Methode startet die Rückwärts Wiedergabe von der aktuellen Position mit der angegebenen Geschwindigkeit.</span><span class="sxs-lookup"><span data-stu-id="4c948-106">The `PlayBackwards` method starts backward playback from the current location at the specified speed.</span></span>

``` syntax
MSWebDVD.PlayBackwards(nSpeed)
```

## <a name="parameters"></a><span data-ttu-id="4c948-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="4c948-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c948-108"><span id="nSpeed"></span><span id="nspeed"></span><span id="NSPEED"></span>*ngeschwindigkeit*</span><span class="sxs-lookup"><span data-stu-id="4c948-108"><span id="nSpeed"></span><span id="nspeed"></span><span id="NSPEED"></span>*nSpeed*</span></span>
</dt> <dd>

<span data-ttu-id="4c948-109">Gibt die Geschwindigkeit an, mit der als Zahl abgespielt werden soll.</span><span class="sxs-lookup"><span data-stu-id="4c948-109">Specifies the speed at which to play as a number.</span></span> <span data-ttu-id="4c948-110">Diese Zahl ist ein Multiplikator – 1.0 ist eine normale Wiedergabegeschwindigkeit. 2,0 ist eine doppelte Geschwindigkeit, 0,5 ist halb Geschwindigkeit usw.</span><span class="sxs-lookup"><span data-stu-id="4c948-110">This number is a multiplier—1.0 is normal playback speed; 2.0 is double speed, 0.5 is half speed, and so on.</span></span> <span data-ttu-id="4c948-111">Wenn "**nspeed**" nicht gleich 1,0 ist, wird das audiobild stumm geschaltet, und das Teilbild ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="4c948-111">When **nSpeed** does not equal 1.0, audio is muted and the subpicture is turned off.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c948-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4c948-112">Return Value</span></span>

<span data-ttu-id="4c948-113">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="4c948-113">No return value.</span></span>

## <a name="see-also"></a><span data-ttu-id="4c948-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4c948-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c948-115">**Playforward**</span><span class="sxs-lookup"><span data-stu-id="4c948-115">**PlayForwards**</span></span>](playforwards-method.md)
</dt> </dl>

 

 



