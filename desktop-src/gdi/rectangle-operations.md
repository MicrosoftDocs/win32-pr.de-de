---
description: Die SetRect-Funktion erstellt ein Rechteck, die CopyRect-Funktion erstellt eine Kopie eines bestimmten Rechtecks, und die SetRectEmpty-Funktion erstellt ein leeres Rechteck.
ms.assetid: 982d6283-673b-41a1-abc7-10ef87ff3c6f
title: Rechteckvorgänge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 161df56d3534f85cd37701956db0330be59236e3cbbeeed81ef390edd17656bb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120092760"
---
# <a name="rectangle-operations"></a>Rechteckvorgänge

Die [**SetRect-Funktion**](/windows/desktop/api/Winuser/nf-winuser-setrect) erstellt ein Rechteck, die [**CopyRect-Funktion**](/windows/desktop/api/Winuser/nf-winuser-copyrect) erstellt eine Kopie eines bestimmten Rechtecks, und die [**SetRectEmpty-Funktion**](/windows/desktop/api/Winuser/nf-winuser-setrectempty) erstellt ein leeres Rechteck. Ein leeres Rechteck ist ein beliebiges Rechteck mit einer Breite von null, einer Höhe von null oder beidem. Die [**IsRectEmpty-Funktion**](/windows/desktop/api/Winuser/nf-winuser-isrectempty) bestimmt, ob ein angegebenes Rechteck leer ist. Die [**EqualRect-Funktion**](/windows/desktop/api/Winuser/nf-winuser-equalrect) bestimmt, ob zwei Rechtecke identisch sind, d. h. ob sie die gleichen Koordinaten aufweisen.

Die [**Funktion InflateRect**](/windows/desktop/api/Winuser/nf-winuser-inflaterect) erhöht oder verringert die Breite oder Höhe eines Rechtecks oder beides. Die Breite kann an beiden Enden des Rechtecks hinzugefügt oder entfernt werden. Sie kann die Höhe sowohl am oberen als auch am unteren Rand des Rechtecks hinzufügen oder entfernen.

Die [**OffsetRect-Funktion**](/windows/desktop/api/Winuser/nf-winuser-offsetrect) verschiebt ein Rechteck um einen bestimmten Betrag. Sie verschiebt das Rechteck, indem den angegebenen x-Betrag, y-Betrag oder x- und y-Betrag den Eckkoordinaten hinzugefügt wird.

Die [**PtInRect-Funktion**](/windows/desktop/api/Winuser/nf-winuser-ptinrect) bestimmt, ob ein angegebener Punkt innerhalb eines bestimmten Rechtecks liegt. Der Punkt befindet sich im Rechteck, wenn er links oder oben liegt oder sich vollständig innerhalb des Rechtecks befindet. Der Punkt befindet sich nicht im Rechteck, wenn er sich auf der rechten oder unteren Seite befindet.

Die [**IntersectRect-Funktion**](/windows/desktop/api/Winuser/nf-winuser-intersectrect) erstellt ein neues Rechteck, das die Schnittmenge zweier vorhandener Rechtecke darstellt, wie in der folgenden Abbildung dargestellt.

![Abbildung, die zwei überlappende Rechtecke mit dunklerer Schattierung zeigt, um die Schnittmenge anzugeben ](images/csrec-01.png)

Die [**UnionRect-Funktion**](/windows/desktop/api/Winuser/nf-winuser-unionrect) erstellt ein neues Rechteck, das die Vereinigung zweier vorhandener Rechtecke darstellt, wie in der folgenden Abbildung dargestellt.

![Abbildung von zwei überlappenden Rechtecke mit dunklerer Schattierung, die Bereiche innerhalb der Union angibt, jedoch nicht innerhalb eines rechteckigen Rechtecks](images/csrec-02.png)

Informationen zu Funktionen, die Ellipsen und Polygone zeichnen, finden Sie unter [Gefüllte Formen.](filled-shapes.md)

 

 



