---
description: Halbtonpaletten sind für die Verwendung vorgesehen, wenn der Stretchingmodus eines Gerätekontexts auf HALFTONE festgelegt ist.
ms.assetid: ee171379-2ab3-4c38-8e86-ff80fa63a357
title: Halbtonpalette und Farbanpassung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8be13f780dc5496173ffb4ddb990a96f7dbe462223e41e8a48d4a58329451277
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118761004"
---
# <a name="halftone-palette-and-color-adjustment"></a>Halbtonpalette und Farbanpassung

Halbtonpaletten sind für die Verwendung vorgesehen, wenn der Stretchingmodus eines Gerätekontexts auf HALFTONE festgelegt ist. Eine Anwendung erstellt mithilfe der [**CreateHalftonePalette-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-createhalftonepalette) eine Halbtonpalette. Die Anwendung muss diese Palette auswählen und in den Gerätekontext integrieren, bevor sie die [**StretchBlt-**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt) oder [**StretchDIBits-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) aufruft.

Das System passt die Eingabefarbe von Quellbitmaps automatisch an, wenn Anwendungen die [**StretchBlt-**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt) und [**StretchDIBits-Funktionen**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) aufrufen und der Stretchingmodus eines Gerätekontexts auf HALFTONE festgelegt ist. Diese Farbanpassungen wirken sich auf bestimmte Attribute des Bilds aus, z. B. Kontrast und Helligkeit. Eine Anwendung kann die Farbanpassungswerte mithilfe der [**SetColorAdjustment-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-setcoloradjustment) festlegen. Die Anwendung kann die Farbanpassungswerte für den angegebenen Gerätekontext mithilfe der [**GetColorAdjustment-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-getcoloradjustment) abrufen.

 

 



