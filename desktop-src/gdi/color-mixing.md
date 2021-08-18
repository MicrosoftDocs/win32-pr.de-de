---
description: Durch Farbmischung kann eine Anwendung neue Farben erstellen, indem die Stift- oder Pinselfarbe mit Farben im vorhandenen Bild kombiniert wird.
ms.assetid: 4a5dff8c-f75f-41d2-8367-33d97d4fd010
title: Farbmischung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed1adde68360d7050e0cebb6e7d5ac073b36a3c18c3687990c1f2aea6a5719f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105729"
---
# <a name="color-mixing"></a>Farbmischung

Durch Farbmischung kann eine Anwendung neue Farben erstellen, indem die Stift- oder Pinselfarbe mit Farben im vorhandenen Bild kombiniert wird. Die Anwendung kann entweder den Stift oder die Pinselfarbe wie vorhanden zeichnen (effektiv über ein vorhandenes Bild zeichnen) oder die Farbe mit den bereits vorhandenen Farben mischen.

Der Vordergrundmischungsmodus, der manchmal als binärer Rastervorgang bezeichnet wird, bestimmt, wie diese Farben gemischt werden. Eine Anwendung kann Farben zusammenführen und dabei alle Komponenten beider Farben beibehalten. Maskieren von Farben, Entfernen oder Moderieren von Komponenten, die nicht üblich sind; oder ausschließlich Farben maskieren, entfernen oder moderieren Komponenten, die häufig verwendet werden. Es gibt mehrere Variationen dieser grundlegenden Mischungsvorgänge.

Die Farbmischung unterliegt der Farbannäherung. Wenn das Ergebnis der Farbmischung eine Farbe ist, die das Gerät nicht generieren kann, wird das Ergebnis vom System mithilfe einer Farbe, die es generieren kann, an das Ergebnis an ungefähr. Wenn eine Anwendung ditherierte Farben gemischt, werden die einzelnen Farben, die zum Erstellen der dithered-Farbe verwendet werden, gemischt, und die Ergebnisse unterliegen der Farbannäherung.

Eine Anwendung legt den Vordergrundmischungsmodus mithilfe der [**SetROP2-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-setrop2) fest und ruft den aktuellen Modus mithilfe der [**GetROP2-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-getrop2) ab.

Obwohl es einen Hintergrundmischungsmodus gibt, kontrolliert dieser Modus das Mischen von Farben nicht. Stattdessen wird angegeben, ob eine Hintergrundfarbe verwendet wird, wenn linienformatierte Linien, schraffierte Pinsel und Text gestrichen werden.

 

 



