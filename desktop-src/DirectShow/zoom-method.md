---
description: Mit der Zoom-Methode wird die Videoanzeige ein-oder ausgehend vergrößert, wobei eine bestimmte Gruppe von Bildschirm Koordinaten zentriert ist.
ms.assetid: 050f1264-8fbe-4322-970c-184275d5b219
title: Zoom-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2625e6c4facf006a0d904e49068853720e20c29e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485638"
---
# <a name="zoom-method"></a><span data-ttu-id="6acf2-103">Zoom-Methode</span><span class="sxs-lookup"><span data-stu-id="6acf2-103">Zoom Method</span></span>

> [!Note]  
> <span data-ttu-id="6acf2-104">Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6acf2-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="6acf2-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="6acf2-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="6acf2-106">Mit der- `Zoom` Methode wird die Videoanzeige ein-oder ausgehend vergrößert, wobei eine bestimmte Gruppe von Bildschirm Koordinaten zentriert ist.</span><span class="sxs-lookup"><span data-stu-id="6acf2-106">The `Zoom` method zooms the video display in or out, centered on a given set of screen coordinates.</span></span>

``` syntax
MSWebDVD.Zoom(iXPos, iYPos, iZoomRatio)
```

## <a name="parameters"></a><span data-ttu-id="6acf2-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="6acf2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6acf2-108"><span id="iXPos"></span><span id="ixpos"></span><span id="IXPOS"></span>*IXPOS*</span><span class="sxs-lookup"><span data-stu-id="6acf2-108"><span id="iXPos"></span><span id="ixpos"></span><span id="IXPOS"></span>*iXPos*</span></span>
</dt> <dd>

<span data-ttu-id="6acf2-109">Gibt die x-Koordinate in der Mitte des rechteckigen Zoombereichs als ganze Zahl an.</span><span class="sxs-lookup"><span data-stu-id="6acf2-109">Specifies the x-coordinate at the center of the rectangular zoom area as an Integer.</span></span>

</dd> <dt>

<span data-ttu-id="6acf2-110"><span id="iYPos"></span><span id="iypos"></span><span id="IYPOS"></span>*iypos*</span><span class="sxs-lookup"><span data-stu-id="6acf2-110"><span id="iYPos"></span><span id="iypos"></span><span id="IYPOS"></span>*iYPos*</span></span>
</dt> <dd>

<span data-ttu-id="6acf2-111">Gibt die y-Koordinate in der Mitte des Rechtecks an, das als ganze Zahl vergrößert werden soll.</span><span class="sxs-lookup"><span data-stu-id="6acf2-111">Specifies the y-coordinate at the center of the rectangle to be zoomed as an Integer.</span></span>

</dd> <dt>

<span data-ttu-id="6acf2-112"><span id="iZoomRatio"></span><span id="izoomratio"></span><span id="IZOOMRATIO"></span>*izoomratio*</span><span class="sxs-lookup"><span data-stu-id="6acf2-112"><span id="iZoomRatio"></span><span id="izoomratio"></span><span id="IZOOMRATIO"></span>*iZoomRatio*</span></span>
</dt> <dd>

<span data-ttu-id="6acf2-113">Gibt den Vergrößerungsfaktor an, der auf den aktuellen Zoomwert als ganze Zahl angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="6acf2-113">Specifies the magnification factor applied to the current zoom value as an Integer.</span></span> <span data-ttu-id="6acf2-114">Der maximale Gesamtwert hängt davon ab, was vom Hardware Overlay unterstützt werden kann. Dies ist normalerweise ein Faktor von 32 bis 64 der ursprünglichen Größe.</span><span class="sxs-lookup"><span data-stu-id="6acf2-114">The total maximum value depends on what the hardware overlay can support; this is typically a factor of 32 to 64 times the original size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6acf2-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6acf2-115">Return Value</span></span>

<span data-ttu-id="6acf2-116">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="6acf2-116">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6acf2-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6acf2-117">Remarks</span></span>

<span data-ttu-id="6acf2-118">Das neue Zoomverhältnis bleibt in Kraft, bis es in der ursprünglichen Größe wieder hergestellt oder erneut geändert wird.</span><span class="sxs-lookup"><span data-stu-id="6acf2-118">The new zoom ratio stays in effect until it is restored to the original size or changed again.</span></span> <span data-ttu-id="6acf2-119">Mit anderen Worten: zwei Aufrufe dieser Methode, die ein *izoomratio* von zwei angeben, führen zu einem Zoomverhältnis, das viermal größer als die ursprüngliche Videogröße ist.</span><span class="sxs-lookup"><span data-stu-id="6acf2-119">In other words, two calls to this method specifying an *iZoomRatio* of two will result in a zoom ratio four times larger than the original video size.</span></span> <span data-ttu-id="6acf2-120">Wenn der Benutzer versucht, die von der Hardware unterstützten Hardware zu vergrößern, ist diese Methode zwar erfolgreich, aber es wird keine Aktion ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6acf2-120">If the user tries to zoom beyond what the hardware can support, this method will succeed but do nothing.</span></span>

<span data-ttu-id="6acf2-121">Die [**setclipvideorect**](setclipvideorect-method.md) -Methode ist eine weitere Möglichkeit zum vergrößern. der einzige Unterschied zwischen den beiden Methoden ist die Art und Weise, in der das Zoom Rechteck angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="6acf2-121">The [**SetClipVideoRect**](setclipvideorect-method.md) method is another way to zoom in; the only difference between the two methods is the way in which the zoom rectangle is specified.</span></span>

 

 



