---
title: Region Files
description: Region Files
ms.assetid: 20952eb9-4cd1-4d7d-b5cc-f1741977745f
keywords:
- Windows Media Player Mobile Skins,Art-Dateien
- Skins,Art-Dateien
- Dateien für Skins,Art
- Artdateien für Skins,Region-Dateien
- Windows Media Player Mobile Skins, Region-Dateien
- Skins, Region-Dateien
- Region-Dateien in Skins
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48ce26db27ef6ad3373916337c6378886a2846f71f1d8aa0e8d5266aae23eff4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117934087"
---
# <a name="region-files"></a>Region Files

Region-Dateien sind erforderlich, wenn Sie eine beliebige Art von Trefferschaltfläche (2PushHit, PushHit oder ToggleHit) verwenden.

Region-Dateien werden verwendet, um Bereiche zu definieren, die auf eine bestimmte Schaltfläche reagieren, die auch als Treffer bezeichnet wird. Für jede Trefferschaltfläche erhält ein Bereich in der Bitmap Region eine bestimmte Webfarbe (z.B. FF0000, der Wert für \# Volltonrot). Die Farbnummer wird in der Definition der Schaltfläche "Region" angegeben. Wenn der Benutzer die Skin anzeigt, wird das Schaltflächenbild mithilfe der Koordinaten des Bereichs in der Bitmap Region auf den Hintergrund überlagert.

Sie können z. B. einen roten Kreis an einer Position zeichnen, die der Position der Schaltfläche Weiter entspricht, und ihn rot einfärben \# (FF0000). Anschließend können Sie in der Schaltflächendefinition einen RGB-Trefferwert von 255,0,0 zuweisen (das RGB-Äquivalent \# von FF0000). In diesem Fall würde die Schaltfläche Weiter nur auf Tippen (Treffer) innerhalb des roten Kreises reagieren.

Trefferschaltflächen werden verwendet, wenn Sie andere Formen als Rechtecke definieren möchten. Sie müssen weiterhin die Koordinaten für jede Schaltfläche definieren, damit sekundäre Bilder wie Pushed und Disabled korrekt gefunden werden können. In der Praxis ist jede Schaltfläche durch ein Rechteck gebunden, und diese imaginären Begrenzungsrechte dürfen sich nicht überlappen.

> [!Note]  
> Region art files are not needed in Windows Media Player 10 Mobile skins because button types are not supported in Windows Media Player 10 Mobile or later.

 

Die folgende Abbildung ist eine typische Region-Datei.

![Region-Datei](images/cesdkreg.png)

Diese Datei definiert die Teile der Skin für jede Treffertypschaltfläche. Jede Farbe wird anhand ihrer Farbnummer im Abschnitt Schaltflächen der Skindefinitionsdatei identifiziert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Art-Dateien**](art-files-mobile.md)
</dt> </dl>

 

 




