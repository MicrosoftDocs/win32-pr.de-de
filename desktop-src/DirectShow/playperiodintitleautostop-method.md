---
description: Die playperiodintitleautostoppt-Methode startet die Wiedergabe zum angegebenen Zeitpunkt im angegebenen Titel bis zur angegebenen Endzeit.
ms.assetid: 0c4df76d-3991-4a6c-a8e5-5fd713eeffc2
title: Playperiodintitleautostoppt-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d05899b66b7f1a11f8f5b177d311b9634a52595b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860180"
---
# <a name="playperiodintitleautostop-method"></a><span data-ttu-id="a770d-103">Playperiodintitleautostoppt-Methode</span><span class="sxs-lookup"><span data-stu-id="a770d-103">PlayPeriodInTitleAutoStop Method</span></span>

> [!Note]  
> <span data-ttu-id="a770d-104">Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a770d-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="a770d-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="a770d-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="a770d-106">Die- `PlayPeriodInTitleAutoStop` Methode startet die Wiedergabe zum angegebenen Zeitpunkt im angegebenen Titel bis zur angegebenen Endzeit.</span><span class="sxs-lookup"><span data-stu-id="a770d-106">The `PlayPeriodInTitleAutoStop` method starts playback at the specified time in the specified title until the specified stop time.</span></span>

``` syntax
MSWebDVD.PlayPeriodInTitleAutoStop(iTitle, sStartTime, sEndTime)
```

## <a name="parameters"></a><span data-ttu-id="a770d-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="a770d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a770d-108"><span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*ititle*</span><span class="sxs-lookup"><span data-stu-id="a770d-108"><span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*iTitle*</span></span>
</dt> <dd>

<span data-ttu-id="a770d-109">Gibt den Titel als Ganzzahl an.</span><span class="sxs-lookup"><span data-stu-id="a770d-109">Specifies the title as an Integer.</span></span>

</dd> <dt>

<span data-ttu-id="a770d-110"><span id="sStartTime"></span><span id="sstarttime"></span><span id="SSTARTTIME"></span>*sstarttime*</span><span class="sxs-lookup"><span data-stu-id="a770d-110"><span id="sStartTime"></span><span id="sstarttime"></span><span id="SSTARTTIME"></span>*sStartTime*</span></span>
</dt> <dd>

<span data-ttu-id="a770d-111">Gibt die Startzeit als Zeichenfolge im Format "hh: mm: SS: FF" an (Stunden, Minuten, Sekunden, Rahmen werden angegeben).</span><span class="sxs-lookup"><span data-stu-id="a770d-111">Specifies the start time as a string in "hh:mm:ss:ff" format (specifying hours, minutes, seconds, frames).</span></span>

</dd> <dt>

<span data-ttu-id="a770d-112"><span id="sEndTime"></span><span id="sendtime"></span><span id="SENDTIME"></span>*sendtime*</span><span class="sxs-lookup"><span data-stu-id="a770d-112"><span id="sEndTime"></span><span id="sendtime"></span><span id="SENDTIME"></span>*sEndTime*</span></span>
</dt> <dd>

<span data-ttu-id="a770d-113">Gibt die Endzeit als Zeichenfolge im Format "hh: mm: SS: FF" an.</span><span class="sxs-lookup"><span data-stu-id="a770d-113">Specifies the end time as a String in "hh:mm:ss:ff" format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a770d-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a770d-114">Return Value</span></span>

<span data-ttu-id="a770d-115">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="a770d-115">No return value.</span></span>

## <a name="see-also"></a><span data-ttu-id="a770d-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a770d-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a770d-117">**Playchaptersauto-Beendigung**</span><span class="sxs-lookup"><span data-stu-id="a770d-117">**PlayChaptersAutoStop**</span></span>](playchaptersautostop-method.md)
</dt> </dl>

 

 



