---
description: Das Beispiel in Pinseln verwendet Bereiche zum Simulieren eines &\# 0034; vergrößert&\# 0034; Ansicht einer 8-Bit-Monochrom-Bitmap mit 8 Pixeln.
ms.assetid: a8e0cbfe-f05b-46ae-b420-ae34a5efbff3
title: Verwenden von Regionen zum Durchführen von Treffer Tests
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb50ca1f837213b85619af381b86c2bd76efcbb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215647"
---
# <a name="using-regions-to-perform-hit-testing"></a><span data-ttu-id="d1337-103">Verwenden von Regionen zum Durchführen von Treffer Tests</span><span class="sxs-lookup"><span data-stu-id="d1337-103">Using Regions to Perform Hit Testing</span></span>

<span data-ttu-id="d1337-104">Im Beispiel in [Pinseln](brushes.md) werden Bereiche verwendet, um eine "Zoomansicht" einer 8-Bit-monochrome Bitmap zu simulieren.</span><span class="sxs-lookup"><span data-stu-id="d1337-104">The example in [Brushes](brushes.md) uses regions to simulate a "zoomed" view of an 8- by 8-pixel monochrome bitmap.</span></span> <span data-ttu-id="d1337-105">Durch Klicken auf die Pixel in dieser Bitmap erstellt der Benutzer einen benutzerdefinierten Pinsel, der für Zeichnungsvorgänge geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="d1337-105">By clicking on the pixels in this bitmap, the user creates a custom brush suitable for drawing operations.</span></span> <span data-ttu-id="d1337-106">Das Beispiel zeigt, wie die [**PtInRegion**](/windows/desktop/api/Wingdi/nf-wingdi-ptinregion) -Funktion zum Ausführen von Treffer Tests und die [**invertrgn**](/windows/desktop/api/Wingdi/nf-wingdi-invertrgn) -Funktion verwendet wird, um die Farben in einem Bereich umzukehren.</span><span class="sxs-lookup"><span data-stu-id="d1337-106">The example shows how to use the [**PtInRegion**](/windows/desktop/api/Wingdi/nf-wingdi-ptinregion) function to perform hit testing and the [**InvertRgn**](/windows/desktop/api/Wingdi/nf-wingdi-invertrgn) function to invert the colors in a region.</span></span>

 

 



