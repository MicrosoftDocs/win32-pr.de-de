---
title: Super Dateien
description: Super Dateien
ms.assetid: a5005d1a-4b87-482d-914e-3184a2c93267
keywords:
- Windows Media Player Mobile Skins, Art Dateien
- Skins, Art Dateien
- Dateien für Skins, Art
- kunstdateien für Skins, Super files-Dateien
- Windows Media Player Mobile Skins, Super files-Dateien
- Skins, Super files
- Super Dateien in Skins
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ece533f81f8866eb0f9848d7296cc23bcd37f453
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338614"
---
# <a name="super-files"></a>Super Dateien

Super Dateien werden zum Speichern der deaktivierten Images für trackbars verwendet. Da das TrackBar-Haupt Bild in der Hintergrund Datei angezeigt wird und der Benutzer auf das Thumb-Bild und nicht auf das TrackBar-Bild tippt, wird nur das deaktivierte Bild für trackbars benötigt. Sie wird in der Datei gespeichert, die von Super im Abschnitt Bitmaps der Skin-Definitionsdatei definiert ist. Eine Super-Datei kann auch die über drückten und deaktivierten Bilder für andere Schaltflächen wie stumm speichern. Dies ist nicht erforderlich, um eine Schaltfläche vom Typ "Treffer" zu sein.

> [!Note]  
> Super kunstdateien werden in Skins für Windows Media Player 10 Mobile oder höher nicht verwendet, da sich die deaktivierten Images für Such trackbars in der seekthumb-Datei befinden.

 

Das folgende Bild ist eine typische Super-Datei.

![Super-Datei](images/cesdksup.png)

Dadurch werden die deaktivierten Bilder für die trackbars und die stumm Schaltfläche gespeichert. Diese Bilder sind im Abschnitt Bitmaps definiert.

Der Hintergrundbereich des deaktivierten TrackBar-Bilds stimmt exakt mit dem entsprechenden Bereich in der Hintergrund Datei überein. Dies ist wichtig, da das gesamte Rechteck, das für das deaktivierte TrackBar-Bild definiert ist, den entsprechenden Bereich in der Hintergrund Datei ersetzt. Dadurch wird sichergestellt, dass das deaktivierte TrackBar-Bild nahtlos in das Hintergrundbild integriert ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Kunstdateien**](art-files-mobile.md)
</dt> </dl>

 

 




