---
description: Mit der dvdadm. disablescreen-Eigenschaft wird der Bildschirmschoner des Systems aktiviert oder deaktiviert.
ms.assetid: 78a0512f-456a-45b6-8717-13593461a765
title: Disablebildschirm (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d651026f2bf09f872655a0ef58accb3a6173dcb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860011"
---
# <a name="disablescreensaver-property"></a><span data-ttu-id="95d05-103">Disablebildschirm (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="95d05-103">DisableScreenSaver Property</span></span>

> [!Note]  
> <span data-ttu-id="95d05-104">Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="95d05-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="95d05-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="95d05-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="95d05-106">Mit der- `DVDAdm.DisableScreenSaver` Eigenschaft wird der Bildschirmschoner des Systems ein-oder ausgeschaltet.</span><span class="sxs-lookup"><span data-stu-id="95d05-106">The `DVDAdm.DisableScreenSaver` property turns the system screen saver on or off.</span></span>

``` syntax
[ bDisabled = ] DVD.DVDAdm.DisableScreenSaver
```

## <a name="return-value"></a><span data-ttu-id="95d05-107">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="95d05-107">Return Value</span></span>

<span data-ttu-id="95d05-108">Gibt einen booleschen Wert zurück, der angibt, ob die Bildschirmschoner Einstellungen des Systems für die DVD-Player-Anwendung deaktiviert sind. "true" bedeutet, dass die Einstellungen deaktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="95d05-108">Returns a Boolean value indicating whether the system's screen saver settings are disabled for the DVD player application; true means the settings are disabled.</span></span>

## <a name="remarks"></a><span data-ttu-id="95d05-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="95d05-109">Remarks</span></span>

<span data-ttu-id="95d05-110">Diese Eigenschaft verfügt über Lese-/Schreibzugriff mit dem Standardwert true.</span><span class="sxs-lookup"><span data-stu-id="95d05-110">This property is read/write with a default value of true.</span></span> <span data-ttu-id="95d05-111">Beim Anzeigen einer DVD-Video Diskette verwendet ein Benutzer in der Regel nicht die Maus oder Tastatur für einen längeren Zeitraum.</span><span class="sxs-lookup"><span data-stu-id="95d05-111">When viewing a DVD-Video disc, a user typically does not use the mouse or keyboard for extended periods of time.</span></span> <span data-ttu-id="95d05-112">Das mswebdvd-ActiveX-®-Steuerelement deaktiviert daher standardmäßig den Bildschirmschoner des Systems.</span><span class="sxs-lookup"><span data-stu-id="95d05-112">The MSWebDVD ActiveX® control therefore disables the system screen saver by default.</span></span> <span data-ttu-id="95d05-113">Object</span><span class="sxs-lookup"><span data-stu-id="95d05-113">Object</span></span>

## <a name="see-also"></a><span data-ttu-id="95d05-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="95d05-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95d05-115">**Restoreskreensaver**</span><span class="sxs-lookup"><span data-stu-id="95d05-115">**RestoreScreenSaver**</span></span>](restorescreensaver-method.md)
</dt> <dt>

[<span data-ttu-id="95d05-116">Msdvdadm-Objekt</span><span class="sxs-lookup"><span data-stu-id="95d05-116">MSDVDAdm Object</span></span>](msdvdadm-object.md)
</dt> </dl>

 

 



