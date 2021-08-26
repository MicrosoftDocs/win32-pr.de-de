---
description: Eine Anwendung erstellt einen Bereich durch Aufrufen einer Funktion, die einer bestimmten Form zugeordnet ist. In der folgenden Tabelle sind die Funktionen aufgeführt, die den einzelnen Standardformen zugeordnet sind.
ms.assetid: e94ae371-8365-4e42-ac8c-04c3928fcffb
title: Erstellen und Auswählen von Regionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75ce2711b2d1ae9dc6641748c72fd586d02e25964102a8c034593d6e60cbaa33
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120092690"
---
# <a name="region-creation-and-selection"></a>Erstellen und Auswählen von Regionen

Eine Anwendung erstellt einen Bereich durch Aufrufen einer Funktion, die einer bestimmten Form zugeordnet ist. In der folgenden Tabelle sind die Funktionen aufgeführt, die den einzelnen Standardformen zugeordnet sind.



| Formen                                   | Funktion                                                                                                                         |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| Rechteckiger Bereich                      | [**CreateRectRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createrectrgn), [**CreateRectRgnIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createrectrgnindirect), [**SetRectRgn**](/windows/desktop/api/Wingdi/nf-wingdi-setrectrgn) |
| Rechteckiger Bereich mit abgerundeten Ecken | [**CreateRoundRectRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createroundrectrgn)                                                                                 |
| Elliptischer Bereich                       | [**CreateEllipticRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createellipticrgn), [ **CreateEllipticRgnIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createellipticrgnindirect)                   |
| Polygonaler Bereich                        | [**CreatePolygonRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createpolygonrgn), [ **CreatePolyPolygonRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createpolypolygonrgn)                               |



 

Jede Funktion zum Erstellen von Regionen gibt ein Handle zurück, das den neuen Bereich identifiziert. Eine Anwendung kann dieses Handle verwenden, um die Region in einem Gerätekontext auszuwählen, indem sie die [**SelectObject-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) aufruft und dieses Handle als zweites Argument an die Hand gibt. Nachdem eine Region in einem Gerätekontext ausgewählt wurde, kann die Anwendung verschiedene Vorgänge ausführen.

 

 



