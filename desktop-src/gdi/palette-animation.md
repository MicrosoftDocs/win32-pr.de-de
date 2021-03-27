---
description: Die Palette-Animation ist eine Technik zum Simulieren von Bewegung, indem die Farben ausgewählter Einträge in einer Farbpalette schnell geändert werden.
ms.assetid: fc5b8061-fd4f-4751-883d-877fa32cdfcc
title: Palette-Animation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9761e99033e7a01fa875fce7c41e5a35cf40ab6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754337"
---
# <a name="palette-animation"></a>Palette-Animation

Die Palette-Animation ist eine Technik zum Simulieren von Bewegung, indem die Farben ausgewählter Einträge in einer Farbpalette schnell geändert werden. Eine Anwendung kann eine palettenanimation durchführen, indem Sie eine logische Palette erstellt, die "reservierte" Einträge enthält, und dann die [**AnimatePalette**](/windows/desktop/api/Wingdi/nf-wingdi-animatepalette) -Funktion verwenden, um die Farben in diesen reservierten Einträgen zu ändern.

Eine Anwendung erstellt einen reservierten Eintrag in einer logischen Palette durch Festlegen des **pfflags** -Members der [**PaletteEntry**](/previous-versions//dd162769(v=vs.85)) -Struktur auf das \_ reservierte PC-Flag. Nachdem diese logische Palette ausgewählt und erkannt wurde, kann die Anwendung die [**AnimatePalette**](/windows/desktop/api/Wingdi/nf-wingdi-animatepalette) -Funktion zum Ändern von mindestens einem reservierten Eintrag aufruft. Wenn die angegebene Palette dem aktiven Fenster zugeordnet ist, aktualisiert das System die Farben auf dem Bildschirm sofort.

 

 
