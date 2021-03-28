---
description: Das System behandelt Farben in Bitmaps anders als Farben in den Stiften, Pinseln und Text.
ms.assetid: c315dd6e-87ee-4905-b193-186ea580ac0a
title: Farbe in Bitmaps
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 834744f35ccc8bd0c8714fa5bbb438b59c8b8db3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130817"
---
# <a name="color-in-bitmaps"></a>Farbe in Bitmaps

Das System behandelt Farben in Bitmaps anders als Farben in den Stiften, Pinseln und Text. Kompatible Bitmaps, die mithilfe der Funktion "up- [**Bitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap) " oder der Funktion " [**kreatecompatiblebitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) " erstellt wurden, sind gerätespezifisch und behalten Farbinformationen in einem geräteabhängigen Format bei. Es werden keine Farbwerte verwendet, und die Farben unterliegen keinem Näherungs-und Dithering.

Geräteunabhängige Bitmaps (Disb) behalten Farbinformationen entweder als Farbwerte oder Farb palettenindizes bei. Wenn Farbwerte verwendet werden, unterliegen die Farben Näherungs-, aber nicht Dithering. Farbpalette-Indizes können nur mit Geräten verwendet werden, die Farbpaletten unterstützen. Obwohl das System keine Näherungs-oder Dithering Farben durch Indizes identifiziert, kann sich die resultierende Farbe von der vorgesehenen Farbe unterscheiden, da die Indizes gültige Ergebnisse nur im Kontext der Farbpalette ergeben, der zum Zeitpunkt der Erstellung der Bitmap aktuell war. Wenn die Palette geändert wird, ändern Sie die Farben in der Bitmap. Weitere Informationen zu palettenindizes finden Sie unter " [Standardpalette](default-palette.md) " und " [**paletteindex**](/windows/desktop/api/Wingdi/nf-wingdi-paletteindex)".

Zusätzlich zum Verweisen auf die logische Palette kann eine Anwendung auch auf einen Wert in einer DIB-Farbtabelle verweisen. Um eine Farbe in einer DIB-Farbtabelle auszuwählen, nennen Sie [**dibindex**](/windows/desktop/api/Mmsystem/nf-mmsystem-dibindex). Beachten Sie, dass dies nur für einen Gerätekontext möglich ist, für den ein DIB ausgewählt ist.

 

 



