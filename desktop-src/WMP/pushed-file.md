---
title: Datei mit Push übertragen
description: Datei mit Push übertragen
ms.assetid: bea803d2-1237-4983-9673-afdcddc32748
keywords:
- Windows Media Player Mobile Skins, Grafikdateien
- Skins, Art-Dateien
- Dateien für Skins, Art
- Grafikdateien für Skins, Pushdateien
- Windows Media Player Mobile Skins, Pushdateien
- Skins, Pushdateien
- Per Push übertragene Dateien in Skins
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0526cad560abfbee3a7ec6cbaa0c355a51d93c2080d7c1ef933f7caaf867ba2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118570675"
---
# <a name="pushed-file"></a>Datei mit Push übertragen

Die Datei pushed enthält die Bilder, die angezeigt werden, wenn der Benutzer auf eine Schaltfläche tippt. Sie können auch die normalen und gepushten Bilder für den Pausenzustand der PlayPause-Schaltfläche einschließen.

Die folgende Abbildung ist eine typische Pushdatei.

![Pushdatei](images/cesdkpus.png)

Dadurch werden die Bilder gespeichert, die angezeigt werden, wenn auf die Schaltflächen des Treffertyps getippt wird. In dieser Datei sind auch die normalen und per Push übertragenen Bilder für das angehaltene Bild der PlayPause-Schaltfläche gespeichert. Mit Ausnahme der sekundären PlayPause-Bilder auf der rechten Seite werden die anderen Schaltflächenbilder mit dem Hintergrundbild angezeigt, wobei der offset verwendet wird, der im Abschnitt Bitmaps der Skindefinitionsdatei definiert ist.

Beachten Sie, dass der Hintergrund des Schaltflächenbilds genau mit dem entsprechenden Bereich in der Hintergrunddatei übereinstimmt. Dies ist wichtig, denn wenn der Benutzer auf eine Schaltfläche vom Typ "Treffer" tippt, ersetzt das gesamte Rechteck, das für das gepushte Bild definiert ist, den entsprechenden Bereich in der Hintergrunddatei. Halten Sie die Grafik konsistent mit dem Hintergrundbild, um sicherzustellen, dass sich nur die Teile der Schaltfläche ändern, die anders angezeigt werden sollen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Art Files**](art-files-mobile.md)
</dt> </dl>

 

 




