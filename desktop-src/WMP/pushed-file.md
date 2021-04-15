---
title: Datei mit pushübertragung
description: Datei mit pushübertragung
ms.assetid: bea803d2-1237-4983-9673-afdcddc32748
keywords:
- Windows Media Player Mobile Skins, Art Dateien
- Skins, Art Dateien
- Dateien für Skins, Art
- kunstdateien für Skins, übersetzte Dateien
- Windows Media Player Mobile Skins, übersetzte Dateien
- Skins, übersetzte Dateien
- Dateien in Skins per pushübertragung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 071a6a4fd00eee7040d2fadb8fb80db343dc0ac6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388392"
---
# <a name="pushed-file"></a>Datei mit pushübertragung

Die gepushte Datei enthält die Bilder, die angezeigt werden, wenn der Benutzer auf eine Schaltfläche tippt. Sie können auch das normale und gepushte Bild für den anhaltezustand der Schaltfläche PLAYPAUSE einschließen.

Das folgende Bild ist eine typische gepushte Datei.

![Datei mit pushübertragung](images/cesdkpus.png)

Dies speichert die Bilder, die angezeigt werden, wenn die Schaltflächen für den Treffer-Typ getippt werden. Auch in dieser Datei gespeichert ist das normale und übersetzte Bild für das angehaltene Bild der Schaltfläche PLAYPAUSE. Mit Ausnahme der sekundären PLAYPAUSE-Images auf der rechten Seite werden die anderen Schaltflächen Bilder mit dem Hintergrundbild angezeigt. dabei wird der Offset verwendet, der im Abschnitt Bitmaps der Skin-Definitionsdatei definiert ist.

Beachten Sie, dass der Hintergrund des Schaltflächen Bilds genau mit dem entsprechenden Bereich in der Hintergrund Datei übereinstimmt. Dies ist wichtig, denn wenn der Benutzer auf eine Schaltfläche vom Typ "Treffer" tippt, ersetzt das gesamte Rechteck, das für das übersetzte Bild definiert ist, den entsprechenden Bereich in der Hintergrund Datei. Halten Sie die Grafik mit dem Hintergrundbild konsistent, um sicherzustellen, dass sich nur die Teile der Schaltfläche, die unterschiedlich angezeigt werden sollen, tatsächlich ändern.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Kunstdateien**](art-files-mobile.md)
</dt> </dl>

 

 




