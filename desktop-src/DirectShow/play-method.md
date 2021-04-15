---
description: Die Play-Methode gibt den aktuellen DVD-Titel wieder.
ms.assetid: fe9dc266-5b12-479d-85cb-50cc6bb9d580
title: Play-Methode (DirectShow)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f62323c9c86be476a35977dadf554bbfca3bca91
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521296"
---
# <a name="play-method-directshow"></a><span data-ttu-id="9dcda-103">Play-Methode (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="9dcda-103">Play Method (DirectShow)</span></span>

> [!Note]  
> <span data-ttu-id="9dcda-104">Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9dcda-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="9dcda-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="9dcda-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="9dcda-106">Die- `Play` Methode gibt den aktuellen DVD-Titel wieder.</span><span class="sxs-lookup"><span data-stu-id="9dcda-106">The `Play` method plays the current DVD title.</span></span>

``` syntax
MSWebDVD.Play()
```

## <a name="return-value"></a><span data-ttu-id="9dcda-107">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9dcda-107">Return Value</span></span>

<span data-ttu-id="9dcda-108">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="9dcda-108">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9dcda-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9dcda-109">Remarks</span></span>

<span data-ttu-id="9dcda-110">Wenn die Wiedergabe angehalten oder beendet wird und [**enableresetonstopp**](enableresetonstop-property.md) den Wert true aufweist, wird die Wiedergabe mit normaler Geschwindigkeit am aktuellen Speicherort durch den Aufruf von **Play** wieder aufgenommen.</span><span class="sxs-lookup"><span data-stu-id="9dcda-110">If playback is paused or stopped and [**EnableResetOnStop**](enableresetonstop-property.md) is true, then calling **Play** will resume playback at normal speed at the current location.</span></span> <span data-ttu-id="9dcda-111">Wenn die Wiedergabe angehalten und **enableresetonend** auf false festgelegt ist, wird durch das Aufrufen von **Play** die Festplatte am Anfang des ersten Titels abgespielt.</span><span class="sxs-lookup"><span data-stu-id="9dcda-111">If playback is stopped and **EnableResetOnStop** is false, then calling **Play** will cause the disc to start playing at the beginning of the first title.</span></span>

## <a name="see-also"></a><span data-ttu-id="9dcda-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9dcda-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9dcda-113">**Fortsetzen**</span><span class="sxs-lookup"><span data-stu-id="9dcda-113">**Resume**</span></span>](resume-method.md)
</dt> </dl>

 

 



