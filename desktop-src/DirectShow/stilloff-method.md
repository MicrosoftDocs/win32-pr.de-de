---
description: Die Methode "stilloff" setzt die Wiedergabe fort und bricht den Modus "immer" ab
ms.assetid: 62091aad-8a78-4543-a844-a4227aed81df
title: Stilloff-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8986b62585768b83fc5737012a924e6cf33daf5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357880"
---
# <a name="stilloff-method"></a><span data-ttu-id="2d895-103">Stilloff-Methode</span><span class="sxs-lookup"><span data-stu-id="2d895-103">StillOff Method</span></span>

> [!Note]  
> <span data-ttu-id="2d895-104">Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2d895-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="2d895-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="2d895-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="2d895-106">Die Methode setzt die Wiedergabe fort und bricht den Modus "immer" ab `StillOff` .</span><span class="sxs-lookup"><span data-stu-id="2d895-106">The `StillOff` method resumes playback, canceling still mode.</span></span>

``` syntax
MSWebDVD.StillOff()
```

## <a name="return-value"></a><span data-ttu-id="2d895-107">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2d895-107">Return Value</span></span>

<span data-ttu-id="2d895-108">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="2d895-108">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d895-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2d895-109">Remarks</span></span>

<span data-ttu-id="2d895-110">Der [DVD-Navigator](dvd-navigator-filter.md) wechselt in den Modus "immer wieder", wenn er auf einen noch auf der CD erstellten Frame trifft. Sie benachrichtigt Ihre Anwendung, indem eine EC- \_ DVD \_ an das Ereignis gesendet wird \_ .</span><span class="sxs-lookup"><span data-stu-id="2d895-110">The [DVD Navigator](dvd-navigator-filter.md) goes into still mode when it encounters a still frame authored on the disc. It notifies your application by sending an EC\_DVD\_STILL\_ON event.</span></span> <span data-ttu-id="2d895-111">Der Modus unterscheidet sich nicht vom DVD-Navigator aufgrund eines Benutzer Vorgangs in einem angehaltenen Zustand.</span><span class="sxs-lookup"><span data-stu-id="2d895-111">Still mode is different from the DVD Navigator being in a paused state because of a user operation.</span></span> <span data-ttu-id="2d895-112">`StillOff`Beim Aufrufen von wird die Wiedergabe aus dem weiterhin Modus wieder aufgenommen, aber der DVD-Navigator wird nicht neu gestartet, wenn Sie sich im angehaltenen Zustand</span><span class="sxs-lookup"><span data-stu-id="2d895-112">Calling `StillOff` resumes playback from still mode but does not restart the DVD Navigator when it is in a paused state.</span></span>

 

 



