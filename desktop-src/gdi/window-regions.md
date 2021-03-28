---
description: Zusätzlich zum Update Bereich verfügt jedes Fenster über einen sichtbaren Bereich, der den für den Benutzer sichtbaren Fenster Teil definiert.
ms.assetid: 9d8beba1-93c0-437d-a138-76880a40bc79
title: Fensterbereiche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02555339412c604f79f69294febbab524fc92a70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042650"
---
# <a name="window-regions"></a>Fensterbereiche

Zusätzlich zum Update Bereich verfügt jedes Fenster über einen *sichtbaren Bereich* , der den für den Benutzer sichtbaren Fenster Teil definiert. Das System ändert den sichtbaren Bereich für das Fenster, wenn die Größe des Fensters geändert wird oder wenn ein anderes Fenster verschoben wird, sodass es einen Teil des Fensters verdeckt oder verfügbar macht. Anwendungen können den sichtbaren Bereich nicht direkt ändern, aber das System verwendet automatisch den sichtbaren Bereich, um den Clippingbereich für jeden für das Fenster abgerufenen Anzeigegeräte Kontext zu erstellen.

Der *Clippingbereich* bestimmt, wo das System das Zeichnen zulässt. Wenn die Anwendung einen Anzeigegeräte Kontext mithilfe der [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint)-, [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc)-oder [**getdcex**](/windows/desktop/api/Winuser/nf-winuser-getdcex) -Funktion abruft, legt das System den Clippingbereich für den Gerätekontext auf die Schnittmenge des sichtbaren Bereichs und des Aktualisierungs Bereichs fest. Anwendungen können den Clippingbereich mithilfe von Funktionen wie " [**setwindowrgn**](/windows/desktop/api/Winuser/nf-winuser-setwindowrgn)", " [**selectclippath**](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath) " und " [**selectcliprgn**](/windows/desktop/api/Wingdi/nf-wingdi-selectcliprgn)" ändern, um das Zeichnen auf einen bestimmten Teil des Aktualisierungs Bereichs weiter einzuschränken.

Die \_ Stile WS clipchildren und WS Clip-untergeordnete Elemente \_ geben an, wie das System den sichtbaren Bereich für ein Fenster berechnet. Wenn ein Fenster einen oder beide Formate enthält, schließt der sichtbare Bereich alle untergeordneten Fenster oder neben geordneten Fenster (Fenster mit dem gleichen übergeordneten Fenster) aus. Daher wird das Zeichnen, das andernfalls in diesen Fenstern eingedrungen wäre, immer abgeschnitten.

 

 



