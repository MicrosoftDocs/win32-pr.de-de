---
description: Zusätzlich zum Updatebereich verfügt jedes Fenster über einen sichtbaren Bereich, der den für den Benutzer sichtbaren Fensterteil definiert.
ms.assetid: 9d8beba1-93c0-437d-a138-76880a40bc79
title: Fensterbereiche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac3f751303d8a971d010ea7dabf7604c24db892f88d9a4029f0189d303cf5a80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119727410"
---
# <a name="window-regions"></a>Fensterbereiche

Zusätzlich zum Updatebereich verfügt jedes Fenster über einen *sichtbaren Bereich,* der den für den Benutzer sichtbaren Fensterteil definiert. Das System ändert den sichtbaren Bereich für das Fenster, wenn sich die Größe des Fensters ändert oder wenn ein anderes Fenster so verschoben wird, dass es einen Teil des Fensters verdeckt oder verfügbar macht. Anwendungen können den sichtbaren Bereich nicht direkt ändern, aber das System verwendet automatisch den sichtbaren Bereich, um den Clippingbereich für alle Anzeigegerätekontexte zu erstellen, die für das Fenster abgerufen werden.

Der *Clippingbereich* bestimmt, wo das System Zeichnen zulässt. Wenn die Anwendung mithilfe der [**BeginPaint-,**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) [**GetDC-**](/windows/desktop/api/Winuser/nf-winuser-getdc)oder [**GetDCEx-Funktion**](/windows/desktop/api/Winuser/nf-winuser-getdcex) einen Anzeigegerätekontext abruft, legt das System den Clippingbereich für den Gerätekontext auf die Schnittmenge des sichtbaren Bereichs und des Updatebereichs fest. Anwendungen können den Clippingbereich mithilfe von Funktionen wie [**SetWindowRgn,**](/windows/desktop/api/Winuser/nf-winuser-setwindowrgn) [**SelectClipPath**](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath) und [**SelectClipRgn**](/windows/desktop/api/Wingdi/nf-wingdi-selectcliprgn)ändern, um das Zeichnen auf einen bestimmten Teil des Aktualisierungsbereichs weiter einzuschränken.

Die Stile WS \_ CLIPCHILDREN und WS \_ CLIPSIBLINGS geben weiter an, wie das System den sichtbaren Bereich für ein Fenster berechnet. Wenn ein Fenster einen oder beide dieser Stile aufweist, schließt der sichtbare Bereich alle untergeordneten Fenster oder nebengeordneten Fenster aus (Fenster mit demselben übergeordneten Fenster). Daher wird das Zeichnen, das andernfalls in diese Fenster eindringt, immer abgeschnitten.

 

 



