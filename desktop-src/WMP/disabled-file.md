---
title: Deaktivierte Datei
description: Deaktivierte Datei
ms.assetid: 8b3339f6-a5d5-4501-826c-6ce33bfbf0cb
keywords:
- Windows Media Player Mobile Skins, Grafikdateien
- Skins, Art-Dateien
- Dateien für Skins, Art
- Grafikdateien für Skins, Deaktivierte Dateien
- Windows Media Player Mobile Skins, Deaktivierte Dateien
- Skins, Deaktivierte Dateien
- Deaktivierte Dateien in Skins
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7b7d7c052ed0de1a3e231bc204b87a84f1e9e10262acfe43df310d76f76577b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997355"
---
# <a name="disabled-file"></a>Deaktivierte Datei

Die Datei Deaktiviert enthält die Bilder, die angezeigt werden, wenn eine bestimmte Schaltflächenfunktion nicht verwendet werden kann oder ein Schaltflächenzustand deaktiviert ist. Wenn beispielsweise eine leere Wiedergabeliste definiert ist, werden die Schaltflächen **Weiter** und **Prev** angezeigt, und sie sollten mit einem deaktivierten Bild angezeigt werden. Außerdem wird für Umschaltflächen das Bild Deaktiviert verwendet, um anzugeben, dass der Zustand deaktiviert ist.

Die folgende Abbildung ist eine typische Disabled-Datei.

![Deaktivierte Datei](images/cesdkdis.png)

Dadurch werden die Bilder für Schaltflächen vom Typ "Treffer" gespeichert, die deaktiviert sind. Die Bilder ähneln der Hintergrunddatei, aber die Farben sind leichter. Mithilfe des Offsets, der im Abschnitt Bitmaps der Skindefinitionsdatei definiert ist, werden die Schaltflächenbilder mit dem Bild der Hintergrunddatei angezeigt.

Beachten Sie, dass der Hintergrund des Schaltflächenbilds genau mit dem entsprechenden Bereich in der Hintergrunddatei übereinstimmt. Dies ist wichtig, da das gesamte für das deaktivierte Bild definierte Rechteck den übereinstimmenden Bereich in der Hintergrunddatei ersetzt, wenn eine Schaltfläche vom Typ "Treffertyp" nicht verfügbar ist. Halten Sie die Grafik konsistent mit dem Hintergrundbild, um sicherzustellen, dass sich nur die Teile der Schaltfläche ändern, die anders angezeigt werden sollen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Art Files**](art-files-mobile.md)
</dt> </dl>

 

 




