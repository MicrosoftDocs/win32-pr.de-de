---
description: Die Aufzeichnungsmethode erfasst ein Image aus dem Videoframe, wenn sich das mswebdvd-Objekt im fensterlosen Modus befindet.
ms.assetid: 704e64ef-3593-403c-8ecf-625fb4983882
title: Capture-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1db16bbc6ef50de303dbcdac66bd066861bb5811
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123643"
---
# <a name="capture-method"></a><span data-ttu-id="f9daf-103">Capture-Methode</span><span class="sxs-lookup"><span data-stu-id="f9daf-103">Capture Method</span></span>

> [!Note]  
> <span data-ttu-id="f9daf-104">Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f9daf-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="f9daf-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="f9daf-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="f9daf-106">Die- `Capture` Methode erfasst ein Image aus dem Videoframe, wenn sich das mswebdvd-Objekt im fensterlosen Modus befindet.</span><span class="sxs-lookup"><span data-stu-id="f9daf-106">The `Capture` method captures a still image from the video frame when the MSWebDVD object is in windowless mode.</span></span>

``` syntax
MSWebDVD.Capture()
```

## <a name="remarks"></a><span data-ttu-id="f9daf-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f9daf-107">Remarks</span></span>

<span data-ttu-id="f9daf-108">Diese Methode erfasst den aktuellen Frame aus dem DVD-Video Bild und fügt ihn in ein Fenster ein, aus dem der Benutzer das Bild speichern oder bearbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="f9daf-108">This method captures the current frame from the DVD-Video image and pastes it into a window from which the user can save or edit the image.</span></span> <span data-ttu-id="f9daf-109">Das mswebdvd-Objekt muss sich im fensterlosen Modus befinden, damit diese Methode erfolgreich ausgeführt werden konnte.</span><span class="sxs-lookup"><span data-stu-id="f9daf-109">The MSWebDVD object must be in windowless mode for this method to succeed.</span></span>

 

 



