---
description: Die DVDTimeCode2bstr-Methode ruft eine Zeichenfolge ab, die die aktuelle Uhrzeit auf dem Laufwerk angibt.
ms.assetid: 0a477274-ac56-4f46-8461-53411362b33e
title: DVDTimeCode2bstr-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 042c6889fd2d5ee76aa42fc4e92f1c2754a5c95d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106346601"
---
# <a name="dvdtimecode2bstr-method"></a><span data-ttu-id="75121-103">DVDTimeCode2bstr-Methode</span><span class="sxs-lookup"><span data-stu-id="75121-103">DVDTimeCode2bstr Method</span></span>

> [!Note]  
> <span data-ttu-id="75121-104">Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="75121-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="75121-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="75121-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="75121-106">Die- `DVDTimeCode2bstr` Methode ruft eine Zeichenfolge ab, die die aktuelle Uhrzeit auf dem Laufwerk angibt.</span><span class="sxs-lookup"><span data-stu-id="75121-106">The `DVDTimeCode2bstr` method retrieves a string indicating the current time on the disc.</span></span>

``` syntax
[ sTimeCode = ] MSWebDVD.DVDTimeCode2bstr(nTimeCode)
```

## <a name="parameters"></a><span data-ttu-id="75121-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="75121-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75121-108"><span id="sTimeCode"></span><span id="stimecode"></span><span id="STIMECODE"></span>*stimecode*</span><span class="sxs-lookup"><span data-stu-id="75121-108"><span id="sTimeCode"></span><span id="stimecode"></span><span id="STIMECODE"></span>*sTimeCode*</span></span>
</dt> <dd>

<span data-ttu-id="75121-109">Gibt die aktuelle Uhrzeit auf der Festplatte relativ zum Anfang des Titels als Zahl an, die über das [**\_ \_ aktuelle \_ hmsf- \_ Zeit**](ec-dvd-current-hmsf-time.md) Ereignis der EC-DVD abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="75121-109">Specifies the current time on the disc relative to the start of the title as a Number obtained through the [**EC\_DVD\_CURRENT\_HMSF\_TIME**](ec-dvd-current-hmsf-time.md) event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75121-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="75121-110">Return Value</span></span>

<span data-ttu-id="75121-111">Gibt eine Zeichenfolge mit 11 Zeichen im Format "hh: mm: SS: FF" zurück, die die Stunden, Minuten, Sekunden und Frames darstellt, die die aktuelle Uhrzeit definieren.</span><span class="sxs-lookup"><span data-stu-id="75121-111">Returns an 11-character String in the format "hh:mm:ss:ff" representing the hours, minutes, seconds and frames that define the current time.</span></span>

## <a name="remarks"></a><span data-ttu-id="75121-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="75121-112">Remarks</span></span>

<span data-ttu-id="75121-113">Diese Methode ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="75121-113">This method is read only.</span></span>

## <a name="see-also"></a><span data-ttu-id="75121-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="75121-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75121-115">Behandeln von DVD-Ereignis Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="75121-115">Handling DVD Event Notifications</span></span>](handling-dvd-event-notifications.md)
</dt> </dl>

 

 



