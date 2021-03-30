---
description: Eine Anwendung kehrt durch Aufrufen der Funktion invertrgn die Farben um, die innerhalb eines Bereichs angezeigt werden.
ms.assetid: bcd9fe61-0f92-41bc-b953-a66e01e43a75
title: Umkehren von Regionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7e3c4b4d01f9ed8f09e819d59bf3268a1ccae4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104993951"
---
# <a name="inverting-regions"></a><span data-ttu-id="94a74-103">Umkehren von Regionen</span><span class="sxs-lookup"><span data-stu-id="94a74-103">Inverting Regions</span></span>

<span data-ttu-id="94a74-104">Eine Anwendung kehrt durch Aufrufen der Funktion [**invertrgn**](/windows/desktop/api/Wingdi/nf-wingdi-invertrgn) die Farben um, die innerhalb eines Bereichs angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="94a74-104">An application inverts the colors that appear within a region by calling the [**InvertRgn**](/windows/desktop/api/Wingdi/nf-wingdi-invertrgn) function.</span></span> <span data-ttu-id="94a74-105">Bei monochrom-anzeigen werden durch **invertrgn** weiße Pixel schwarz und schwarz Pixel weiß.</span><span class="sxs-lookup"><span data-stu-id="94a74-105">On monochrome displays, **InvertRgn** makes white pixels black and black pixels white.</span></span> <span data-ttu-id="94a74-106">Auf Farb Schirmen hängt diese Inversion vom Typ der Technologie ab, die zum Generieren der Farben für den Bildschirm verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="94a74-106">On color screens, this inversion is dependent on the type of technology used to generate the colors for the screen.</span></span>

 

 



