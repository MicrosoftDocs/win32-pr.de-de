---
description: Die SetRect-Funktion erstellt ein Rechteck, die copyrect-Funktion erstellt eine Kopie eines angegebenen Rechtecks, und die Funktion setrectempty erstellt ein leeres Rechteck.
ms.assetid: 982d6283-673b-41a1-abc7-10ef87ff3c6f
title: Rechteck Vorgänge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3117fda697000e92258c99cf90af470e8815e237
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344639"
---
# <a name="rectangle-operations"></a>Rechteck Vorgänge

Die [**SetRect**](/windows/desktop/api/Winuser/nf-winuser-setrect) -Funktion erstellt ein Rechteck, die [**copyrect**](/windows/desktop/api/Winuser/nf-winuser-copyrect) -Funktion erstellt eine Kopie eines angegebenen Rechtecks, und die Funktion [**setrectempty**](/windows/desktop/api/Winuser/nf-winuser-setrectempty) erstellt ein leeres Rechteck. Ein leeres Rechteck ist ein beliebiges Rechteck, das eine Breite, eine Höhe von 0 (null) oder beides aufweist. Die [**isrectempty**](/windows/desktop/api/Winuser/nf-winuser-isrectempty) -Funktion bestimmt, ob ein bestimmtes Rechteck leer ist. Die [**equalrect**](/windows/desktop/api/Winuser/nf-winuser-equalrect) -Funktion bestimmt, ob zwei Rechtecke identisch sind, d. h., ob Sie die gleichen Koordinaten aufweisen.

Die [**inflaterect**](/windows/desktop/api/Winuser/nf-winuser-inflaterect) -Funktion vergrößert oder verringert die Breite oder Höhe eines Rechtecks oder beides. Sie kann die Breite von beiden Enden des Rechtecks hinzufügen oder entfernen. die Höhe kann dem oberen und unteren Rand des Rechtecks hinzugefügt oder daraus entfernt werden.

Die [**offsetrect**](/windows/desktop/api/Winuser/nf-winuser-offsetrect) -Funktion verschiebt ein Rechteck um einen angegebenen Betrag. Er verschiebt das Rechteck durch Hinzufügen der angegebenen x-Amount-, y-Amount-oder x-und y-Beträge zu den Eckkoordinaten.

Die [**PtInRect**](/windows/desktop/api/Winuser/nf-winuser-ptinrect) -Funktion bestimmt, ob ein angegebener Punkt innerhalb eines angegebenen Rechtecks liegt. Der Punkt befindet sich im Rechteck, wenn er auf der linken oder oberen Seite liegt oder sich vollständig innerhalb des Rechtecks befindet. Der Punkt befindet sich nicht im Rechteck, wenn er sich auf der rechten oder unteren Seite befindet.

Die [**intersectRect**](/windows/desktop/api/Winuser/nf-winuser-intersectrect) -Funktion erstellt ein neues Rechteck, bei dem es sich um die Schnittmenge zweier bestehender Rechtecke handelt, wie in der folgenden Abbildung dargestellt.

![Abbildung mit zwei überlappenden Rechtecke, mit dunkler Schattierung zum Angeben der Schnittmenge ](images/csrec-01.png)

Die [**unionrect**](/windows/desktop/api/Winuser/nf-winuser-unionrect) -Funktion erstellt ein neues Rechteck, das die Union zweier bestehender Rechtecke darstellt, wie in der folgenden Abbildung dargestellt.

![Abbildung von zwei überlappenden Rechtecke mit dunkler Schattierung, die Bereiche innerhalb der Union, aber nicht innerhalb eines der beiden Rechtecks anzeigt](images/csrec-02.png)

Informationen zu Funktionen, die Ellipsen und Polygone zeichnen, finden Sie unter [gefüllte Formen](filled-shapes.md).

 

 



