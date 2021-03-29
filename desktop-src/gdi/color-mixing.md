---
description: Durch Farbmischung können Anwendungen neue Farben erstellen, indem Sie den Stift oder die Pinsel Farbe mit Farben im vorhandenen Bild kombinieren.
ms.assetid: 4a5dff8c-f75f-41d2-8367-33d97d4fd010
title: Farbmischung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffa85f6ea449fa13f7b7120160915ea72a0e3dd2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130813"
---
# <a name="color-mixing"></a>Farbmischung

Durch Farbmischung können Anwendungen neue Farben erstellen, indem Sie den Stift oder die Pinsel Farbe mit Farben im vorhandenen Bild kombinieren. Die Anwendung kann auswählen, ob der Stift oder die Pinsel Farbe unverändert gezeichnet werden soll (wodurch ein vorhandenes Bild tatsächlich gezeichnet wird) oder die Farbe mit den bereits vorhandenen Farben gemischt werden soll.

Der Vordergrund Mischungs Modus, der manchmal als binärer Raster Vorgang bezeichnet wird, bestimmt, wie diese Farben gemischt werden. Eine Anwendung kann Farben zusammenführen, wobei alle Komponenten beider Farben beibehalten werden. Masken Farben, entfernen oder moderieren von Komponenten, die nicht häufig vorkommen; oder exklusiv Masken Farben, entfernen oder moderieren allgemeiner Komponenten. Es gibt mehrere Variationen dieser grundlegenden Mischungs Vorgänge.

Farbmischung unterliegt der Farb Näherung. Wenn das Ergebnis der Farbmischung eine Farbe ist, die das Gerät nicht generieren kann, gleicht das System das Ergebnis mithilfe einer Farbe, die es generieren kann. Wenn eine Anwendung Dithering-Farben vermischt, werden die einzelnen Farben, die zum Erstellen der Dithering-Farbe verwendet werden, gemischt, und die Ergebnisse unterliegen der Farb Näherung.

Eine Anwendung legt den Vordergrund Mischungs Modus mithilfe der [**SetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-setrop2) -Funktion fest und ruft den aktuellen Modus mithilfe der [**GetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-getrop2) -Funktion ab.

Obwohl es einen Hintergrund Mischungs Modus gibt, steuert dieser Modus nicht die Mischung von Farben. Stattdessen wird angegeben, ob eine Hintergrundfarbe beim Zeichnen von formatierten Linien, ausstrichen und Text verwendet wird.

 

 



