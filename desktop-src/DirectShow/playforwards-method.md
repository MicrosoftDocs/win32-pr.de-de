---
description: Die playforward-Methode startet die Wiedergabe von der aktuellen Position mit der angegebenen Geschwindigkeit.
ms.assetid: 4f1a3e74-b343-413d-8df7-6c4bea39c62d
title: Playforward-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10d49d8d6d80613c4dd5b2b8a374002b37d9baa4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746793"
---
# <a name="playforwards-method"></a><span data-ttu-id="4935d-103">Playforward-Methode</span><span class="sxs-lookup"><span data-stu-id="4935d-103">PlayForwards Method</span></span>

> [!Note]  
> <span data-ttu-id="4935d-104">Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="4935d-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="4935d-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="4935d-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="4935d-106">Mit der-Methode wird die `PlayForwards` Wiedergabe von der aktuellen Position mit der angegebenen Geschwindigkeit gestartet.</span><span class="sxs-lookup"><span data-stu-id="4935d-106">The `PlayForwards` method starts forward playback from the current location at the specified speed.</span></span>

``` syntax
MSWebDVD.PlayForwards(nSpeed)
```

## <a name="parameters"></a><span data-ttu-id="4935d-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="4935d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4935d-108"><span id="nSpeed"></span><span id="nspeed"></span><span id="NSPEED"></span>*ngeschwindigkeit*</span><span class="sxs-lookup"><span data-stu-id="4935d-108"><span id="nSpeed"></span><span id="nspeed"></span><span id="NSPEED"></span>*nSpeed*</span></span>
</dt> <dd>

<span data-ttu-id="4935d-109">Gibt die Geschwindigkeit an, mit der als ganzzahliger Wert abgespielt werden soll.</span><span class="sxs-lookup"><span data-stu-id="4935d-109">Specifies the speed at which to play as an Integer value.</span></span> <span data-ttu-id="4935d-110">Dieser Wert ist ein Multiplikator – 1.0 ist eine normale Wiedergabegeschwindigkeit. 2,0 ist eine doppelte Geschwindigkeit, 0,5 ist halb Geschwindigkeit usw.</span><span class="sxs-lookup"><span data-stu-id="4935d-110">This value is a multiplier—1.0 is normal playback speed; 2.0 is double speed, 0.5 is half speed, and so on.</span></span> <span data-ttu-id="4935d-111">Wenn "**nspeed**" nicht gleich 1,0 ist, wird das audiobild stumm geschaltet, und das Teilbild ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="4935d-111">When **nSpeed** does not equal 1.0, audio is muted and the subpicture is turned off.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4935d-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4935d-112">Return Value</span></span>

<span data-ttu-id="4935d-113">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="4935d-113">No return value.</span></span>

## <a name="see-also"></a><span data-ttu-id="4935d-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4935d-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4935d-115">**Playrückwärts**</span><span class="sxs-lookup"><span data-stu-id="4935d-115">**PlayBackwards**</span></span>](playbackwards-method.md)
</dt> </dl>

 

 



