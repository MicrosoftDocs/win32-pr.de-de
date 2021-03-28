---
description: Die Abmessungen eines geometrischen Stifts werden in logischen Einheiten angegeben.
ms.assetid: e7030490-d10c-4d1c-87ae-5b4cc4858ee1
title: Geometrische Stifte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9725f6440f62458d4c87232400f16e27f9b978ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104993998"
---
# <a name="geometric-pens"></a>Geometrische Stifte

Die Abmessungen eines geometrischen Stifts werden in logischen Einheiten angegeben. Daher können Linien, die mit einem geometrischen Stift gezeichnet werden, skaliert werden, d. h., Sie können je nach aktueller Welt Transformation breiter oder schmaler erscheinen. Weitere Informationen zur weltweiten Transformation finden Sie unter [Koordinaten Bereiche und Transformationen](coordinate-spaces-and-transformations.md).

Zusätzlich zu den drei Attributen, die mit den kosmetischen stiften (Breite, Format und Farbe) gemeinsam genutzt werden, besitzen geometrische Stifte die folgenden vier Attribute: Muster, optionale Schraffur, Endstil und joinstil. Weitere Informationen zu diesen Attributen finden Sie unter [Pen-Attribute](pen-attributes.md).

Zum Erstellen eines geometrischen Stifts verwendet eine Anwendung die [**extkreatepen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) -Funktion. Wie bei den kosmetischen stiften wählt die [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) -Funktion einen geometrischen Stift in den DC der Anwendung aus.

 

 



