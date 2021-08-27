---
title: Superdateien
description: Superdateien
ms.assetid: a5005d1a-4b87-482d-914e-3184a2c93267
keywords:
- Windows Media Player Mobile Skins, Grafikdateien
- Skins, Art-Dateien
- Dateien für Skins, Art
- Grafikdateien für Skins, Superdateien
- Windows Media Player Mobile Skins, Superdateien
- Skins, Superdateien
- Superdateien in Skins
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcbd6734e0491b5fc0e6552db14b3c0ab4489e466e7851ef4b474e84d2d85183
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122864"
---
# <a name="super-files"></a>Superdateien

Superdateien werden verwendet, um die deaktivierten Images für Trackbars zu speichern. Da das Hauptbild der Trackleiste in der Hintergrunddatei angezeigt wird und der Benutzer auf das Bild mit dem Daumen tippt und nicht auf das Trackleistenbild, wird nur das Bild Deaktiviert für Trackleisten benötigt. Sie wird in der von Super definierten Datei im Abschnitt Bitmaps der Skindefinitionsdatei gespeichert. Eine Super-Datei kann auch die Bilder Pushed und Disabled für andere Schaltflächen speichern, z. B. Mute, was nicht als Schaltfläche vom Typ "Treffer" erforderlich ist.

> [!Note]  
> SuperArt-Dateien werden nicht in Skins für Windows Media Player 10 Mobile oder höher verwendet, da sich die deaktivierten Bilder für Suchspurleisten in der Seekthumb-Datei befinden.

 

Die folgende Abbildung ist eine typische Superdatei.

![Superdatei](images/cesdksup.png)

Dadurch werden die deaktivierten Bilder für die Trackleisten und die Stummschaltungsschaltfläche gespeichert. Diese Bilder werden entsprechend der Definition im Abschnitt Bitmaps versetzt.

Der Hintergrundbereich des deaktivierten Trackbarbilds stimmt genau mit dem entsprechenden Bereich in der Hintergrunddatei überein. Dies ist wichtig, da das gesamte Rechteck, das für das deaktivierte Trackbarbild definiert ist, den entsprechenden Bereich in der Hintergrunddatei ersetzt. Dadurch wird sichergestellt, dass das deaktivierte Trackbarbild nahtlos in das Hintergrundbild integriert wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Art Files**](art-files-mobile.md)
</dt> </dl>

 

 




