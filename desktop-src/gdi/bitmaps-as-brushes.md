---
description: Eine Reihe von Funktionen verwenden den aktuell ausgewählten Pinsel in einem Gerätekontext, um bitmapvorgänge auszuführen.
ms.assetid: 98fb2fd5-9cf4-4016-9e30-ec724e77cebc
title: Bitmaps als Pinsel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c693e3c144dec2d26eccca1f1b628252dea187c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215215"
---
# <a name="bitmaps-as-brushes"></a><span data-ttu-id="49d6e-103">Bitmaps als Pinsel</span><span class="sxs-lookup"><span data-stu-id="49d6e-103">Bitmaps as Brushes</span></span>

<span data-ttu-id="49d6e-104">Eine Reihe von Funktionen verwenden den aktuell ausgewählten Pinsel in einem Gerätekontext, um bitmapvorgänge auszuführen.</span><span class="sxs-lookup"><span data-stu-id="49d6e-104">A number of functions use the brush currently selected into a device context to perform bitmap operations.</span></span> <span data-ttu-id="49d6e-105">Beispielsweise wird der Pinsel mit der [**patblt**](/windows/desktop/api/Wingdi/nf-wingdi-patblt) -Funktion in einem rechteckigen Bereich innerhalb eines Fensters repliziert, und die Funktion zum [**Auffüllen**](/windows/desktop/api/Wingdi/nf-wingdi-floodfill) repliziert den Pinsel innerhalb eines Bereichs in einem Fenster, das durch die angegebene Farbe begrenzt ist (im Gegensatz zu **patblt** werden bei der über **flufill** -Funktion nicht rechteckige Formen aufgefüllt).</span><span class="sxs-lookup"><span data-stu-id="49d6e-105">For example, the [**PatBlt**](/windows/desktop/api/Wingdi/nf-wingdi-patblt) function replicates the brush in a rectangular region within a window, and the [**FloodFill**](/windows/desktop/api/Wingdi/nf-wingdi-floodfill) function replicates the brush inside an area in a window bounded by the specified color (unlike **PatBlt**, **FloodFill** does fill nonrectangular shapes).</span></span>

<span data-ttu-id="49d6e-106">Die [**flufill**](/windows/desktop/api/Wingdi/nf-wingdi-floodfill) -Funktion repliziert den Pinsel innerhalb eines Bereichs, der durch eine angegebene Farbe begrenzt ist.</span><span class="sxs-lookup"><span data-stu-id="49d6e-106">The [**FloodFill**](/windows/desktop/api/Wingdi/nf-wingdi-floodfill) function replicates the brush within a region bounded by a specified color.</span></span> <span data-ttu-id="49d6e-107">Anders als bei der [**patblt**](/windows/desktop/api/Wingdi/nf-wingdi-patblt) -Funktion kombiniert die über **flufill** -Funktion jedoch nicht die Farbdaten für den Pinsel mit den Farbdaten für die Pixel auf der Anzeige. Dadurch wird einfach die Farbe aller Pixel innerhalb des eingeschlossenen Bereichs auf der Anzeige auf die Farbe des Pinsels festgelegt, der derzeit im Gerätekontext ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="49d6e-107">However, unlike the [**PatBlt**](/windows/desktop/api/Wingdi/nf-wingdi-patblt) function, **FloodFill** does not combine the color data for the brush with the color data for the pixels on the display; it simply sets the color of all pixels within the enclosed region on the display to the color of the brush that is currently selected into the device context.</span></span>

 

 



