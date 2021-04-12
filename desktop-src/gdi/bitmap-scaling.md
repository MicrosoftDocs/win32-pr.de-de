---
description: Die StretchBlt-Funktion skaliert eine Bitmap, indem eine Bitblock Übertragung von einem Rechteck in einem Quell Gerätekontext in ein Rechteck in einem Zielgeräte Kontext durchgeführt wird.
ms.assetid: 34390ff9-8d5f-497e-87aa-a1019d01bba6
title: Bitmapskalierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4011b06e6a7269be29e1834e90928c4f531b1023
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130848"
---
# <a name="bitmap-scaling"></a><span data-ttu-id="ac39e-103">Bitmapskalierung</span><span class="sxs-lookup"><span data-stu-id="ac39e-103">Bitmap Scaling</span></span>

<span data-ttu-id="ac39e-104">Die [**StretchBlt**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt) -Funktion skaliert eine Bitmap, indem eine Bitblock Übertragung von einem Rechteck in einem Quell Gerätekontext in ein Rechteck in einem Zielgeräte Kontext durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ac39e-104">The [**StretchBlt**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt) function scales a bitmap by performing a bit-block transfer from a rectangle in a source device context into a rectangle in a destination device context.</span></span> <span data-ttu-id="ac39e-105">Anders als bei der [**BitBLT**](/windows/desktop/api/Wingdi/nf-wingdi-bitblt) -Funktion, mit der die Quell Rechteck Dimensionen im Ziel Rechteck dupliziert werden, kann eine Anwendung mithilfe von **StretchBlt** die Dimensionen der Quell-und Ziel Rechtecke angeben.</span><span class="sxs-lookup"><span data-stu-id="ac39e-105">However, unlike the [**BitBlt**](/windows/desktop/api/Wingdi/nf-wingdi-bitblt) function, which duplicates the source rectangle dimensions in the destination rectangle, **StretchBlt** allows an application to specify the dimensions of both the source and the destination rectangles.</span></span> <span data-ttu-id="ac39e-106">Wenn die Ziel Bitmap kleiner ist als die Quell Bitmap, kombiniert das System Zeilen oder Spalten von Farbdaten (oder beides) vor dem Rendern des entsprechenden Bilds auf dem Anzeigegerät.</span><span class="sxs-lookup"><span data-stu-id="ac39e-106">When the destination bitmap is smaller than the source bitmap, the system combines rows or columns of color data (or both) in the bitmap before rendering the corresponding image on the display device.</span></span> <span data-ttu-id="ac39e-107">Das System kombiniert die Farbdaten gemäß dem angegebenen streckungs Modus, der von der Anwendung durch Aufrufen der [**setstretchbltmode**](/windows/desktop/api/Wingdi/nf-wingdi-setstretchbltmode) -Funktion definiert wird.</span><span class="sxs-lookup"><span data-stu-id="ac39e-107">The system combines the color data according to the specified stretch mode, which the application defines by calling the [**SetStretchBltMode**](/windows/desktop/api/Wingdi/nf-wingdi-setstretchbltmode) function.</span></span> <span data-ttu-id="ac39e-108">Wenn die Ziel Bitmap größer als die Quell Bitmap ist, skaliert oder vergrößert das System jedes Pixel im resultierenden Bild entsprechend.</span><span class="sxs-lookup"><span data-stu-id="ac39e-108">When the destination bitmap is larger than the source bitmap, the system scales or magnifies each pixel in the resultant image accordingly.</span></span>

 

 



