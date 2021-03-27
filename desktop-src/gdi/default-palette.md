---
description: Die Standardpalette ist ein Array von Farbwerten, mit denen die Farben identifiziert werden, die standardmäßig mit einem Gerätekontext verwendet werden können.
ms.assetid: 7972d5da-2b73-4cd7-a2ee-fca3a571f611
title: Standard Palette
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c100eeb144ab4f6483281b33739578642880a91f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863668"
---
# <a name="default-palette"></a>Standard Palette

Die *Standardpalette* ist ein Array von Farbwerten, mit denen die Farben identifiziert werden, die standardmäßig mit einem Gerätekontext verwendet werden können. Das System ordnet die Standardpalette einem Kontext zu, wenn eine Anwendung einen Kontext für ein Gerät erstellt, das Farbpaletten unterstützt. Die Standardpalette stellt sicher, dass Farben zur Verwendung durch eine Anwendung ohne weitere Aktionen verfügbar sind.

Die Standardpalette hat normalerweise 20 Einträge (Farben), aber die genaue Anzahl von Einträgen kann von Gerät zu Gerät abweichen. Diese Zahl ist gleich dem numcolors-Wert, der von der [**gettovicecaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) -Funktion zurückgegeben wird. Eine Anwendung kann die Farbwerte für Farben in der Standardpalette abrufen, indem Sie ausgefülltes Stifte aufzählt, die gleiche Technik, die zum Ermitteln der Farben auf nicht palettengeräten verwendet wird. Die Farben in der Standardpalette hängen vom Gerät ab. Geräte anzeigen beispielsweise werden häufig die 16 Standardfarben der VGA-Anzeige und 4 weitere von Windows definierte Farben verwendet. Druckgeräte können andere Standardfarben verwenden.

Bei Verwendung der Standardpalette verwenden Anwendungen Farbwerte, um Stift-und Textfarben anzugeben. Wenn die angeforderte Farbe nicht in der Palette liegt, gleicht das System die Farbe, indem es die nächstgelegene Farbe in der Palette verwendet. Wenn eine Anwendung eine voll Tonfarbe anfordert, die sich nicht in der Palette befindet, simuliert das System die Farbe, indem die Farben in der Palette ausgeblendet werden.

Um Näherungen und Dithering zu vermeiden, können Anwendungen auch Stift-, Pinsel-und Textfarben angeben, indem Sie Farb palettenindizes anstelle von Farbwerten verwenden. Ein Farb Palettenindex ist ein ganzzahliger Wert, der einen bestimmten Paletteneintrag identifiziert. Anwendungen können Farb palettenindizes anstelle von Farbwerten verwenden, müssen jedoch das " [**paletteindex**](/windows/desktop/api/Wingdi/nf-wingdi-paletteindex) "-Makro verwenden, um die Indizes zu erstellen.

Farbpalette-Indizes sind nur für Geräte nützlich, die Farbpaletten unterstützen. Um diese Geräte Abhängigkeit zu vermeiden, sollten Anwendungen, die denselben Code verwenden, um sowohl Paletten-als auch nicht palettengeräte zu zeichnen, die Farb Werte für Stift, Pinsel und Text verwenden. Diese Werte sind identisch mit Farbwerten, es sei denn, Sie erstellen voll tonpinsel. (Bei palettengeräten unterliegt eine durch einen palettenrelativer Farbwert angegebene Vollbild-Farbe Farb Näherung anstelle von Dithering.) Anwendungen müssen das [**palettergb**](/windows/desktop/api/Wingdi/nf-wingdi-palettergb) -Makro verwenden, um palettenrelative Farbwerte zu erstellen.

Das System lässt nicht zu, dass eine Anwendung die Einträge in der Standardpalette ändert. Um andere Farben als die in der Standardpalette zu verwenden, muss eine Anwendung eine eigene logische Palette erstellen und die Palette in den Gerätekontext auswählen.

 

 



