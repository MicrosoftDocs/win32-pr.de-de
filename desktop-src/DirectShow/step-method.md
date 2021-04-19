---
description: Mit der Step-Methode wird der DVD-Video Stream um die angegebene Anzahl von Frames erweitert.
ms.assetid: 6f67335e-51c7-4b81-8ab3-86a3d70ac871
title: Step-Methode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29b9c3f20e41c52bfa32c2cf0138c9e286c98e13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362612"
---
# <a name="step-method"></a><span data-ttu-id="2a35d-103">Step-Methode</span><span class="sxs-lookup"><span data-stu-id="2a35d-103">Step Method</span></span>

> [!Note]  
> <span data-ttu-id="2a35d-104">Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2a35d-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="2a35d-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="2a35d-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="2a35d-106">Die- `Step` Methode verschiebt den DVD-Video Stream um die angegebene Anzahl von Frames.</span><span class="sxs-lookup"><span data-stu-id="2a35d-106">The `Step` method advances the DVD-Video stream by the specified number of frames.</span></span>

``` syntax
MSWebDVD.Step(iFrames)
```

## <a name="parameters"></a><span data-ttu-id="2a35d-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="2a35d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a35d-108"><span id="iFrames"></span><span id="iframes"></span><span id="IFRAMES"></span>*iFrames*</span><span class="sxs-lookup"><span data-stu-id="2a35d-108"><span id="iFrames"></span><span id="iframes"></span><span id="IFRAMES"></span>*iFrames*</span></span>
</dt> <dd>

<span data-ttu-id="2a35d-109">Gibt die Anzahl der Rahmen an, die als ganze Zahl durchlaufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="2a35d-109">Specifies the number of frames to step as an Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a35d-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2a35d-110">Return Value</span></span>

<span data-ttu-id="2a35d-111">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="2a35d-111">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a35d-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2a35d-112">Remarks</span></span>

<span data-ttu-id="2a35d-113">Rufen Sie vor dem Aufrufen dieser Methode [**canstep**](canstep-method.md) auf, um zu bestimmen, ob der Decoder Frame-Step unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2a35d-113">Before calling this method, call [**CanStep**](canstep-method.md) to determine whether the decoder supports frame stepping.</span></span>

<span data-ttu-id="2a35d-114">Wenn die DVD-Video im umgekehrten Modus wiedergegeben wird, wenn diese Methode aufgerufen wird, und der Decoder die umgekehrte Frame Ausführung unterstützt, erfolgt die schrittweise Ausführung der Frame Ausführung in umgekehrter Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="2a35d-114">If the DVD-Video is playing in reverse mode when this method is called, and the decoder supports reverse frame stepping, then the frame stepping is done in reverse.</span></span>

 

 



