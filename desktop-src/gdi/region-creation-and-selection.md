---
description: Eine Anwendung erstellt durch Aufrufen einer Funktion, die einer bestimmten Form zugeordnet ist, einen Bereich. In der folgenden Tabelle werden die Funktionen angezeigt, die den einzelnen Standardformen zugeordnet sind.
ms.assetid: e94ae371-8365-4e42-ac8c-04c3928fcffb
title: Regionale Erstellung und-Auswahl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d27a7887e41a04a62015fa3fc9d82f5beeb01d6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978352"
---
# <a name="region-creation-and-selection"></a>Regionale Erstellung und-Auswahl

Eine Anwendung erstellt durch Aufrufen einer Funktion, die einer bestimmten Form zugeordnet ist, einen Bereich. In der folgenden Tabelle werden die Funktionen angezeigt, die den einzelnen Standardformen zugeordnet sind.



| Form                                   | Funktion                                                                                                                         |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| Rechteckiger Bereich                      | " [**Kreaterectrgn**](/windows/desktop/api/Wingdi/nf-wingdi-createrectrgn)", " [**kreaterectrgnindirekte**](/windows/desktop/api/Wingdi/nf-wingdi-createrectrgnindirect)", " [**setrectrgn**](/windows/desktop/api/Wingdi/nf-wingdi-setrectrgn) " |
| Rechteckiger Bereich mit abgerundeten Ecken | [**"Kreateroundrectrgn"**](/windows/desktop/api/Wingdi/nf-wingdi-createroundrectrgn)                                                                                 |
| Elliptische Region                       | " [**Kreateellipticrgn**](/windows/desktop/api/Wingdi/nf-wingdi-createellipticrgn)", " [ **kreateellipticrgnindirekte** "](/windows/desktop/api/Wingdi/nf-wingdi-createellipticrgnindirect)                   |
| Polygonaler Bereich                        | " [**Kreatepolygonrgn**](/windows/desktop/api/Wingdi/nf-wingdi-createpolygonrgn)", " [ **kreatepolypolygonrgn** "](/windows/desktop/api/Wingdi/nf-wingdi-createpolypolygonrgn)                               |



 

Jede Regions Erstellungs Funktion gibt ein Handle zurück, das den neuen Bereich identifiziert. Eine Anwendung kann dieses Handle verwenden, um den Bereich in einen Gerätekontext auszuwählen, indem die [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) -Funktion aufgerufen und dieses Handle als zweites Argument bereitgestellt wird. Nachdem ein Bereich in einen Gerätekontext ausgewählt wurde, kann die Anwendung verschiedene Vorgänge ausführen.

 

 



