---
description: Jeder Monitor kann über eine eigene Farbtiefe verfügen.
ms.assetid: 8d1ba8d2-b43d-498d-be5a-100fe9fc0f61
title: Farben auf mehreren Anzeige Monitoren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50410631cf0ea3ac0a1b9967f1116809be0a4851
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959312"
---
# <a name="colors-on-multiple-display-monitors"></a>Farben auf mehreren Anzeige Monitoren

Jeder Monitor kann über eine eigene Farbtiefe verfügen. Das System passt Farben automatisch an, wenn Fenster über Monitore mit unterschiedlicher Farbtiefe bewegt werden. Im allgemeinen ergibt dies gute Ergebnisse. Dies ist jedoch nicht immer optimal. Wenn Sie die Farbfunktionen verschiedener Monitore nutzen möchten, finden Sie entsprechende Informationen im folgenden Abschnitt zeichnen [auf mehreren Anzeige Monitoren](painting-on-multiple-display-monitors.md) .

Um zu ermitteln, ob alle Monitore das gleiche Farb Format aufweisen, müssen Sie [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) mit SM \_ samedisplayformat aufrufen.

Wenn der primäre Monitor palettisiert ist, funktionieren [**SelectPalette**](/windows/desktop/api/Wingdi/nf-wingdi-selectpalette) und [**RealizePalette**](/windows/desktop/api/Wingdi/nf-wingdi-realizepalette) genauso wie zuvor, aber über alle Monitore hinweg. Außerdem werden die Paletten aller palettengeräte synchronisiert. Wenn der primäre Monitor nicht palettisiert ist, wählen **SelectPalette** und **RealizePalette** die Palette im Hintergrund aus, und die Geräte werden nicht synchronisiert.

 

 
