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
# <a name="halftone-palette-and-color-adjustment"></a>"Halftone"-Palette und Farbanpassung

Halftone-Paletten können immer verwendet werden, wenn der streckungs Modus eines Geräte Kontexts auf "Halftone" festgelegt ist. Eine Anwendung erstellt eine halbftone-Palette mithilfe der [**CreateHalftonePalette**](/windows/desktop/api/Wingdi/nf-wingdi-createhalftonepalette) -Funktion. Die Anwendung muss diese Palette vor dem Aufrufen der Funktion [**StretchBlt**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt) oder [**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) in den Gerätekontext auswählen und diese nutzen.

Das System passt die Eingabe Farbe der Quell Bitmaps automatisch an, wenn Anwendungen die Funktionen [**StretchBlt**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt) und [**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) aufzurufen und der streckungs Modus eines Geräte Kontexts auf Halftone festgelegt ist. Diese Farbanpassungen beeinflussen bestimmte Attribute des Bilds, z. b. Kontrast und Helligkeit. Eine Anwendung kann die Farb Anpassungs Werte mithilfe der [**setcoloradjustment**](/windows/desktop/api/Wingdi/nf-wingdi-setcoloradjustment) -Funktion festlegen. Die Anwendung kann die Farb Anpassungs Werte für den angegebenen Gerätekontext mithilfe der [**getcoloradjustment**](/windows/desktop/api/Wingdi/nf-wingdi-getcoloradjustment) -Funktion abrufen.

 

 



