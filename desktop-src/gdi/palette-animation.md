---
description: Palettenanimation ist eine Technik zum Simulieren von Bewegung durch schnelles Ändern der Farben ausgewählter Einträge in einer Farbpalette.
ms.assetid: fc5b8061-fd4f-4751-883d-877fa32cdfcc
title: Palettenanimation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18ea2d557ddd071a8f8e993f3a797fb42c2f4fef9abc68fc13737cded96a18fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119965590"
---
# <a name="palette-animation"></a>Palettenanimation

Palettenanimation ist eine Technik zum Simulieren von Bewegung durch schnelles Ändern der Farben ausgewählter Einträge in einer Farbpalette. Eine Anwendung kann Palettenanimation durchführen, indem sie eine logische Palette mit "reservierten" Einträgen erstellt und dann die [**Funktion "AnimatePalette"**](/windows/desktop/api/Wingdi/nf-wingdi-animatepalette) verwendet, um die Farben in diesen reservierten Einträgen zu ändern.

Eine Anwendung erstellt einen reservierten Eintrag in einer logischen Palette, indem das **peFlags-Member** der [**PALETTEENTRY-Struktur**](/previous-versions//dd162769(v=vs.85)) auf das FLAG PC \_ RESERVED (PC RESERVED) festlegen. Sobald diese logische Palette ausgewählt und realisiert wurde, kann die Anwendung die [**Funktion AnimatePalette**](/windows/desktop/api/Wingdi/nf-wingdi-animatepalette) aufrufen, um einen oder mehrere reservierte Einträge zu ändern. Wenn die gegebene Palette dem aktiven Fenster zugeordnet ist, aktualisiert das System die Farben auf dem Bildschirm sofort.

 

 
