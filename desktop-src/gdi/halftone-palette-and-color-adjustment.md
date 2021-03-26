---
description: Halftone-Paletten können immer verwendet werden, wenn der streckungs Modus eines Geräte Kontexts auf "Halftone" festgelegt ist.
ms.assetid: ee171379-2ab3-4c38-8e86-ff80fa63a357
title: "\"Halftone\"-Palette und Farbanpassung"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b3e6708aff92387b792424f07e9b82a1f6125ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528340"
---
# <a name="halftone-palette-and-color-adjustment"></a><span data-ttu-id="24511-103">"Halftone"-Palette und Farbanpassung</span><span class="sxs-lookup"><span data-stu-id="24511-103">Halftone Palette and Color Adjustment</span></span>

<span data-ttu-id="24511-104">Halftone-Paletten können immer verwendet werden, wenn der streckungs Modus eines Geräte Kontexts auf "Halftone" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="24511-104">Halftone palettes are intended to be used whenever the stretching mode of a device context is set to HALFTONE.</span></span> <span data-ttu-id="24511-105">Eine Anwendung erstellt eine halbftone-Palette mithilfe der [**CreateHalftonePalette**](/windows/desktop/api/Wingdi/nf-wingdi-createhalftonepalette) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="24511-105">An application creates a halftone palette by using the [**CreateHalftonePalette**](/windows/desktop/api/Wingdi/nf-wingdi-createhalftonepalette) function.</span></span> <span data-ttu-id="24511-106">Die Anwendung muss diese Palette vor dem Aufrufen der Funktion [**StretchBlt**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt) oder [**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) in den Gerätekontext auswählen und diese nutzen.</span><span class="sxs-lookup"><span data-stu-id="24511-106">The application must select and realize this palette into the device context before calling the [**StretchBlt**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt) or [**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) function.</span></span>

<span data-ttu-id="24511-107">Das System passt die Eingabe Farbe der Quell Bitmaps automatisch an, wenn Anwendungen die Funktionen [**StretchBlt**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt) und [**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) aufzurufen und der streckungs Modus eines Geräte Kontexts auf Halftone festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="24511-107">The system automatically adjusts the input color of source bitmaps whenever applications call the [**StretchBlt**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt) and [**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) functions and the stretching mode of a device context is set to HALFTONE.</span></span> <span data-ttu-id="24511-108">Diese Farbanpassungen beeinflussen bestimmte Attribute des Bilds, z. b. Kontrast und Helligkeit.</span><span class="sxs-lookup"><span data-stu-id="24511-108">These color adjustments affect certain attributes of the image, such as contrast and brightness.</span></span> <span data-ttu-id="24511-109">Eine Anwendung kann die Farb Anpassungs Werte mithilfe der [**setcoloradjustment**](/windows/desktop/api/Wingdi/nf-wingdi-setcoloradjustment) -Funktion festlegen.</span><span class="sxs-lookup"><span data-stu-id="24511-109">An application can set the color adjustment values by using the [**SetColorAdjustment**](/windows/desktop/api/Wingdi/nf-wingdi-setcoloradjustment) function.</span></span> <span data-ttu-id="24511-110">Die Anwendung kann die Farb Anpassungs Werte für den angegebenen Gerätekontext mithilfe der [**getcoloradjustment**](/windows/desktop/api/Wingdi/nf-wingdi-getcoloradjustment) -Funktion abrufen.</span><span class="sxs-lookup"><span data-stu-id="24511-110">The application can retrieve the color adjustment values for the specified device context by using the [**GetColorAdjustment**](/windows/desktop/api/Wingdi/nf-wingdi-getcoloradjustment) function.</span></span>

 

 



