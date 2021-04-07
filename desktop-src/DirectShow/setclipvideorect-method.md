---
description: Die setclipvideorect-Methode zoomt die Videoanzeige in das angegebene unter Rechteck.
ms.assetid: 3940a382-8d53-4ff9-b024-38de1aa00f54
title: Setclipvideorect-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ff7f4b003ef20b82f1e783ebf074e8bbd5cc793
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746296"
---
# <a name="setclipvideorect-method"></a><span data-ttu-id="dfd7e-103">Setclipvideorect-Methode</span><span class="sxs-lookup"><span data-stu-id="dfd7e-103">SetClipVideoRect Method</span></span>

> [!Note]  
> <span data-ttu-id="dfd7e-104">Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="dfd7e-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="dfd7e-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="dfd7e-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="dfd7e-106">Mit der- `SetClipVideoRect` Methode wird die Videoanzeige in das angegebene unter Rechteck vergrößert.</span><span class="sxs-lookup"><span data-stu-id="dfd7e-106">The `SetClipVideoRect` method zooms the video display to the specified subrectangle.</span></span>

``` syntax
MSWebDVD.SetClipVideoRect(oRect)
```

## <a name="parameters"></a><span data-ttu-id="dfd7e-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="dfd7e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dfd7e-108"><span id="oRect"></span><span id="orect"></span><span id="ORECT"></span>*orect*</span><span class="sxs-lookup"><span data-stu-id="dfd7e-108"><span id="oRect"></span><span id="orect"></span><span id="ORECT"></span>*oRect*</span></span>
</dt> <dd>

<span data-ttu-id="dfd7e-109">Gibt ein [dvdrect](dvdrect-object.md) -Objekt an, das das Clippingrechteck enthält.</span><span class="sxs-lookup"><span data-stu-id="dfd7e-109">Specifies a [DVDRect](dvdrect-object.md) object, which contains the clipping rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dfd7e-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dfd7e-110">Return Value</span></span>

<span data-ttu-id="dfd7e-111">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="dfd7e-111">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="dfd7e-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dfd7e-112">Remarks</span></span>

<span data-ttu-id="dfd7e-113">Beim Festlegen eines neuen clippingrechtecks vergrößert das Objekt den Bereich, sodass er in die Gesamt Anzeige Dimensionen der Anwendung passt.</span><span class="sxs-lookup"><span data-stu-id="dfd7e-113">When you set a new clipping rectangle, the object enlarges that area to fit within the application's overall display dimensions.</span></span> <span data-ttu-id="dfd7e-114">Dadurch wird die Auswirkung auf einen bestimmten Bereich des Bildschirms vergrößert.</span><span class="sxs-lookup"><span data-stu-id="dfd7e-114">This creates the effect zooming in on a particular area of the screen.</span></span> <span data-ttu-id="dfd7e-115">Um das Rechteck anzugeben, erstellen Sie ein neues [dvdrect](dvdrect-object.md) -Objekt, und füllen Sie seine Eigenschaften aus.</span><span class="sxs-lookup"><span data-stu-id="dfd7e-115">To specify the rectangle, create a new [DVDRect](dvdrect-object.md) object and fill in its properties.</span></span>

<span data-ttu-id="dfd7e-116">Das häufigste Rechteck für die Videoanzeige ist 720 x 540.</span><span class="sxs-lookup"><span data-stu-id="dfd7e-116">The most common rectangle for video display is 720 x 540.</span></span>

## <a name="see-also"></a><span data-ttu-id="dfd7e-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dfd7e-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfd7e-118">**Getclipvideorect**</span><span class="sxs-lookup"><span data-stu-id="dfd7e-118">**GetClipVideoRect**</span></span>](getclipvideorect-method.md)
</dt> </dl>

 

 



