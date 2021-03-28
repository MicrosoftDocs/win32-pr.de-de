---
description: Eine Anwendung füllt das Innere eines Bereichs durch Aufrufen der fillrgn-Funktion und Bereitstellen eines Handles, das einen bestimmten Pinsel identifiziert.
ms.assetid: 6174b2ea-836a-4538-a0ad-e123c88fc6f6
title: Auffüllen von Regionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62709869f5f25a6cde11812844efdab6162b1e9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041968"
---
# <a name="filling-regions"></a><span data-ttu-id="8cfce-103">Auffüllen von Regionen</span><span class="sxs-lookup"><span data-stu-id="8cfce-103">Filling Regions</span></span>

<span data-ttu-id="8cfce-104">Eine Anwendung füllt das Innere eines Bereichs durch Aufrufen der [**fillrgn**](/windows/desktop/api/Wingdi/nf-wingdi-fillrgn) -Funktion und Bereitstellen eines Handles, das einen bestimmten Pinsel identifiziert.</span><span class="sxs-lookup"><span data-stu-id="8cfce-104">An application fills the interior of a region by calling the [**FillRgn**](/windows/desktop/api/Wingdi/nf-wingdi-fillrgn) function and supplying a handle that identifies a specific brush.</span></span> <span data-ttu-id="8cfce-105">Wenn eine Anwendung fillrgn aufruft, füllt das System den Bereich mit dem Pinsel, indem der aktuelle Füll Modus für den angegebenen Gerätekontext verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8cfce-105">When an application calls FillRgn , the system fills the region with the brush by using the current fill mode for the specified device context.</span></span> <span data-ttu-id="8cfce-106">Es gibt zwei Füll Modi: "Alternative" und "Winding".</span><span class="sxs-lookup"><span data-stu-id="8cfce-106">There are two fill modes: alternate and winding.</span></span> <span data-ttu-id="8cfce-107">Die Anwendung kann den Füll Modus für einen Gerätekontext durch Aufrufen der [**setpolyfillmode**](/windows/desktop/api/Wingdi/nf-wingdi-setpolyfillmode) -Funktion festlegen.</span><span class="sxs-lookup"><span data-stu-id="8cfce-107">The application can set the fill mode for a device context by calling the [**SetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-setpolyfillmode) function.</span></span> <span data-ttu-id="8cfce-108">Die Anwendung kann den aktuellen Füllmodus für einen Gerätekontext abrufen, indem die [**getpolyfillmode**](/windows/desktop/api/Wingdi/nf-wingdi-getpolyfillmode) -Funktion aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="8cfce-108">The application can retrieve the current fill mode for a device context by calling the [**GetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-getpolyfillmode) function.</span></span>

<span data-ttu-id="8cfce-109">In der folgenden Abbildung sind zwei identische Bereiche dargestellt: eine mit dem alternativen Modus und die andere mit dem Auffüllmodus.</span><span class="sxs-lookup"><span data-stu-id="8cfce-109">The following illustration shows two identical regions: one filled using alternate mode and the other filled using winding mode.</span></span>

![Abbildung mit 2 5-Spitzen Sternen: eine, die nur in den Punkten gefüllt ist, die andere vollständig ausgefüllt](images/csrgn-03.png)

## <a name="alternate-mode"></a><span data-ttu-id="8cfce-111">Alternativer Modus</span><span class="sxs-lookup"><span data-stu-id="8cfce-111">Alternate Mode</span></span>

<span data-ttu-id="8cfce-112">Führen Sie den folgenden Test aus, um zu bestimmen, welche Pixel das System hervorhebt, wenn der Alternative Modus angegeben ist:</span><span class="sxs-lookup"><span data-stu-id="8cfce-112">To determine which pixels the system highlights when alternate mode is specified, perform the following test:</span></span>

1.  <span data-ttu-id="8cfce-113">Wählen Sie ein Pixel im Inneren des Bereichs aus.</span><span class="sxs-lookup"><span data-stu-id="8cfce-113">Select a pixel within the region's interior.</span></span>
2.  <span data-ttu-id="8cfce-114">Zeichnen Sie ein imaginäres Strahl in der positiven x-Richtung von diesem Pixel bis unendlich.</span><span class="sxs-lookup"><span data-stu-id="8cfce-114">Draw an imaginary ray, in the positive x-direction, from that pixel toward infinity.</span></span>
3.  <span data-ttu-id="8cfce-115">Jedes Mal, wenn das Strahl eine Begrenzungs Linie schneidet, erhöhen Sie einen Count-Wert.</span><span class="sxs-lookup"><span data-stu-id="8cfce-115">Each time the ray intersects a boundary line, increment a count value.</span></span>

<span data-ttu-id="8cfce-116">Das System hebt das Pixel hervor, wenn der Count-Wert eine ungerade Zahl ist.</span><span class="sxs-lookup"><span data-stu-id="8cfce-116">The system highlights the pixel if the count value is an odd number.</span></span>

## <a name="winding-mode"></a><span data-ttu-id="8cfce-117">Lademodus</span><span class="sxs-lookup"><span data-stu-id="8cfce-117">Winding Mode</span></span>

<span data-ttu-id="8cfce-118">Führen Sie den folgenden Test aus, um zu bestimmen, welche Pixel das System hervorhebt, wenn der Wickel Modus angegeben ist:</span><span class="sxs-lookup"><span data-stu-id="8cfce-118">To determine which pixels the system highlights when winding mode is specified, perform the following test:</span></span>

1.  <span data-ttu-id="8cfce-119">Bestimmen Sie die Richtung, in der die einzelnen Begrenzungs Linien gezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="8cfce-119">Determine the direction in which each boundary line is drawn.</span></span>
2.  <span data-ttu-id="8cfce-120">Wählen Sie ein Pixel im Inneren des Bereichs aus.</span><span class="sxs-lookup"><span data-stu-id="8cfce-120">Select a pixel within the region's interior.</span></span>
3.  <span data-ttu-id="8cfce-121">Zeichnen Sie ein imaginäres Ray, das in der positiven x-Richtung verläuft, vom Pixel bis zum unendlich.</span><span class="sxs-lookup"><span data-stu-id="8cfce-121">Draw an imaginary ray, in the positive x-direction, from the pixel toward infinity.</span></span>
4.  <span data-ttu-id="8cfce-122">Jedes Mal, wenn das Strahl eine Begrenzungs Linie mit einer positiven y-Komponente schneidet, erhöhen Sie einen Count-Wert.</span><span class="sxs-lookup"><span data-stu-id="8cfce-122">Each time the ray intersects a boundary line with a positive y-component, increment a count value.</span></span> <span data-ttu-id="8cfce-123">Jedes Mal, wenn das Strahl eine Begrenzungs Linie mit einer negativen y-Komponente schneidet, wird der Count-Wert verringert.</span><span class="sxs-lookup"><span data-stu-id="8cfce-123">Each time the ray intersects a boundary line with a negative y-component, decrement the count value.</span></span>

<span data-ttu-id="8cfce-124">Das System hebt das Pixel hervor, wenn der Count-Wert ungleich 0 (null) ist.</span><span class="sxs-lookup"><span data-stu-id="8cfce-124">The system highlights the pixel if the count value is nonzero.</span></span>

 

 



