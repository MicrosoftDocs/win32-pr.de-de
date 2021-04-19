---
description: Ein Muster (oder benutzerdefinierter) Pinsel wird aus einer Anwendungs definierten Bitmap oder einer geräteunabhängigen Bitmap (DIB) erstellt. Die folgenden Rechtecke wurden mit unterschiedlichen Muster Pinseln gezeichnet.
ms.assetid: 0de89a6f-d9c7-4f33-8088-c24a48a3ceee
title: Muster Pinsel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66d39dd499d6a95b3fb61624b2aab8b421f51c34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988178"
---
# <a name="pattern-brush"></a><span data-ttu-id="ae051-104">Muster Pinsel</span><span class="sxs-lookup"><span data-stu-id="ae051-104">Pattern Brush</span></span>

<span data-ttu-id="ae051-105">Ein Muster (oder benutzerdefinierter) Pinsel wird aus einer Anwendungs definierten Bitmap oder einer geräteunabhängigen Bitmap (DIB) erstellt.</span><span class="sxs-lookup"><span data-stu-id="ae051-105">A pattern (or custom) brush is created from an application-defined bitmap or device-independent bitmap (DIB).</span></span> <span data-ttu-id="ae051-106">Die folgenden Rechtecke wurden mit unterschiedlichen Muster Pinseln gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="ae051-106">The following rectangles were painted by using different pattern brushes.</span></span>

![Abbildung, die drei Felder anzeigt, die jeweils mit einem anderen Muster gefüllt sind](images/csbru-05.png)

<span data-ttu-id="ae051-108">Zum Erstellen eines logischen Muster Pinsels muss eine Anwendung zuerst eine Bitmap erstellen.</span><span class="sxs-lookup"><span data-stu-id="ae051-108">To create a logical pattern brush, an application must first create a bitmap.</span></span> <span data-ttu-id="ae051-109">Nach dem Erstellen der Bitmap kann die Anwendung den logischen Muster Pinsel erstellen, indem Sie die [**CreatePatternBrush**](/windows/desktop/api/Wingdi/nf-wingdi-createpatternbrush) -oder [**createdibpatternbrushpt**](/windows/desktop/api/Wingdi/nf-wingdi-createdibpatternbrushpt) -Funktion aufrufen und ein Handle bereitstellen, das die Bitmap (oder DIB) identifiziert.</span><span class="sxs-lookup"><span data-stu-id="ae051-109">After creating the bitmap, the application can create the logical pattern brush by calling the [**CreatePatternBrush**](/windows/desktop/api/Wingdi/nf-wingdi-createpatternbrush) or [**CreateDIBPatternBrushPt**](/windows/desktop/api/Wingdi/nf-wingdi-createdibpatternbrushpt) function, supplying a handle that identifies the bitmap (or DIB).</span></span> <span data-ttu-id="ae051-110">Die Pinsel, die in der obigen Abbildung angezeigt werden, wurden aus Monochrom-Bitmaps erstellt.</span><span class="sxs-lookup"><span data-stu-id="ae051-110">The brushes that appear in the preceding illustration were created from monochrome bitmaps.</span></span> <span data-ttu-id="ae051-111">Eine Beschreibung der Bitmaps, Disb und der Funktionen, die Sie erstellen, finden Sie unter [Bitmaps](bitmaps.md).</span><span class="sxs-lookup"><span data-stu-id="ae051-111">For a description of bitmaps, DIBs, and the functions that create them, see [Bitmaps](bitmaps.md).</span></span>

 

 



