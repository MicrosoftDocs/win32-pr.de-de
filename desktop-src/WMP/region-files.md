---
title: Regions Dateien
description: Regions Dateien
ms.assetid: 20952eb9-4cd1-4d7d-b5cc-f1741977745f
keywords:
- Windows Media Player Mobile Skins, Art Dateien
- Skins, Art Dateien
- Dateien für Skins, Art
- kunstdateien für Skins, Regions Dateien
- Windows Media Player Mobile Skins, Regions Dateien
- Skins, Regions Dateien
- Regions Dateien in Skins
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48d258afeab029df7218d3616b8aecdb62c72806
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311112"
---
# <a name="region-files"></a>Regions Dateien

Regions Dateien sind erforderlich, wenn Sie eine beliebige Art von Treffer Schaltfläche verwenden (2pushhit, pushhit oder degglehit).

Regions Dateien werden verwendet, um Bereiche zu definieren, die auf eine Tap (auch als Treffer bezeichnet) auf einer bestimmten Schaltfläche reagieren. Für jede Treffer Schaltfläche erhält ein Bereich in der Bereichs Bitmap eine bestimmte Webfarbe (z. b. \# FF0000, bei der es sich um den Wert für ein voll tonrot handelt). Die Farbnummer wird in der Definition der Bereichs Schaltfläche angegeben. Wenn der Benutzer die Skin anzeigt, wird das Schaltflächen Bild mithilfe der Koordinaten des Bereichs in der Bereichs Bitmap auf dem Hintergrund dargestellt.

Sie können z. b. einen roten Kreis an einem Speicherort zeichnen, der dem Speicherort der Schaltfläche "weiter" entspricht, und die Farbe "rot" ( \# FF0000). Anschließend können Sie in der Schaltflächen Definition den Wert "Treffer RGB" von 255, 0, 0 (der RGB-Entsprechung von \# FF0000) zuweisen. In diesem Fall würde die Schaltfläche "weiter" nur auf Abzweigungen (Treffer) innerhalb des roten Kreises reagieren.

Wenn Sie andere Formen als Rechtecke definieren möchten, werden Treffer Schaltflächen verwendet. Sie müssen immer noch die Koordinaten für jede Schaltfläche definieren, damit sekundäre Images wie z. b. gepusht und deaktiviert sind. In der Praxis wird jede Schaltfläche durch ein Rechteck gebunden, und diese imaginären Begrenzungs Rechtecke dürfen sich nicht überlappen.

> [!Note]  
> Regions kunstdateien werden in Windows Media Player 10 Mobile-Skins nicht benötigt, da Schaltflächen Typen in Windows Media Player 10 Mobile oder höher nicht unterstützt werden.

 

Das folgende Bild ist eine typische Regions Datei.

![Regions Datei](images/cesdkreg.png)

Diese Datei definiert die Teile der Skin für jede Schaltfläche des Treffer Typs. Jede Farbe wird anhand ihrer Farbzahl im Schaltflächen Abschnitt der Skin-Definitionsdatei identifiziert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Kunstdateien**](art-files-mobile.md)
</dt> </dl>

 

 




