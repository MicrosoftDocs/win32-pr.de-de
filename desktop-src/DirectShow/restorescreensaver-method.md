---
description: Die dvdadm. restoreskreensaver-Methode stellt die Einstellungen des System Bildschirmschoners wieder her.
ms.assetid: 606ab850-95bf-4c60-b7cf-e3a94ceee7a7
title: Restoreskreensaver-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85b747aa21815bb37cc7db2296347c9890a06914
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106343551"
---
# <a name="restorescreensaver-method"></a><span data-ttu-id="f5320-103">Restoreskreensaver-Methode</span><span class="sxs-lookup"><span data-stu-id="f5320-103">RestoreScreenSaver Method</span></span>

> [!Note]  
> <span data-ttu-id="f5320-104">Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f5320-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="f5320-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="f5320-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="f5320-106">Die- `DVDAdm.RestoreScreenSaver` Methode stellt die Einstellungen des System Bildschirmschoners wieder her.</span><span class="sxs-lookup"><span data-stu-id="f5320-106">The `DVDAdm.RestoreScreenSaver` method restores the system screen saver settings.</span></span>

``` syntax
DVD.DVDAdm.RestoreScreenSaver()
```

## <a name="return-value"></a><span data-ttu-id="f5320-107">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f5320-107">Return Value</span></span>

<span data-ttu-id="f5320-108">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="f5320-108">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f5320-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f5320-109">Remarks</span></span>

<span data-ttu-id="f5320-110">Im allgemeinen deaktiviert eine DVD-Anwendung beim Start den Bildschirmschoner des Systems, indem die [**disablescreen**](disablescreensaver-property.md) -Eigenschaft auf true festgelegt wird. Anschließend wird der Bildschirmschoner erneut aktiviert, wenn die DVD-Anwendung durch Aufrufen von geschlossen wird `RestoreScreenSaver` .</span><span class="sxs-lookup"><span data-stu-id="f5320-110">Generally, a DVD application will disable the system's screen saver on startup by setting the [**DisableScreenSaver**](disablescreensaver-property.md) property to true, and then re-enable the screen saver again when the DVD application is closed by calling `RestoreScreenSaver`.</span></span> <span data-ttu-id="f5320-111">Wenn eine Anwendung die Bildschirmschoner Einstellungen des Systems nicht verwendet, muss diese Methode nicht aufgerufen oder die **disablescreen** -Eigenschaft festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="f5320-111">If an application does not use the system's screen saver settings, it does not have to call this method or set the **DisableScreenSaver** property.</span></span>

## <a name="see-also"></a><span data-ttu-id="f5320-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f5320-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5320-113">Msdvdadm-Objekt</span><span class="sxs-lookup"><span data-stu-id="f5320-113">MSDVDAdm Object</span></span>](msdvdadm-object.md)
</dt> </dl>

 

 



