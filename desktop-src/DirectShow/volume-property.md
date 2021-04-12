---
description: Die Volume-Eigenschaft legt das Lautstärke-Volume für die audiostreamausgabe fest oder ruft es ab.
ms.assetid: b6e22d07-525b-4af2-898c-ce3ed16ea9c1
title: Volume-Eigenschaft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c9c85bc2d20a613e61d454f75b9663284188c16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527806"
---
# <a name="volume-property"></a><span data-ttu-id="210f8-103">Volume-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="210f8-103">Volume Property</span></span>

> [!Note]  
> <span data-ttu-id="210f8-104">Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="210f8-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="210f8-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="210f8-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="210f8-106">Die `Volume` -Eigenschaft legt das Lautsprecher Volume für die audiostreamausgabe fest oder ruft es ab.</span><span class="sxs-lookup"><span data-stu-id="210f8-106">The `Volume` property sets or retrieves the speaker volume for the audio stream output.</span></span>

``` syntax
[ iVolume = ] MSWebDVD.Volume
```

## <a name="return-value"></a><span data-ttu-id="210f8-107">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="210f8-107">Return Value</span></span>

<span data-ttu-id="210f8-108">Gibt den volumengrad als Dämpfung in Dezibel als Ganzzahl zurück.</span><span class="sxs-lookup"><span data-stu-id="210f8-108">Returns the volume level as attenuation in decibels as an Integer.</span></span>

## <a name="remarks"></a><span data-ttu-id="210f8-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="210f8-109">Remarks</span></span>

<span data-ttu-id="210f8-110">Diese Eigenschaft ist Lese-/Schreibzugriff mit einem Standardwert von 0.</span><span class="sxs-lookup"><span data-stu-id="210f8-110">This property is read/write with a default value of 0.</span></span> <span data-ttu-id="210f8-111">Das vollständige Volume ist 0, und 10.000 ist Ruhe. die Skala ist logarithmisch.</span><span class="sxs-lookup"><span data-stu-id="210f8-111">Full volume is 0, and 10,000 is silence; the scale is logarithmic.</span></span> <span data-ttu-id="210f8-112">Multiplizieren Sie die gewünschte Dezibelskala-Ebene um 100 (z. b. 10.000 = 100 dB).</span><span class="sxs-lookup"><span data-stu-id="210f8-112">Multiply the desired decibel level by 100 (for example 10,000 = 100 dB).</span></span>

 

 



