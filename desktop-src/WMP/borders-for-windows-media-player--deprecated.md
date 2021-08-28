---
title: Rahmen für Windows Media Player (veraltet)
description: Rahmen für Windows Media Player (veraltet)
ms.assetid: defa461b-ffa5-4fee-bed4-aba3e733b8c4
keywords:
- Windows Media Player, Rahmen
- Windows Media Player Skins, Rahmen
- Skins, Rahmen
- Rahmen im Vergleich zu Skins
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c32e16fa6e334c5c47f24feadc777b82cee1a12477211bc4e613d22e8fdc4521
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123850"
---
# <a name="borders-for-windows-media-player-deprecated"></a>Rahmen für Windows Media Player (veraltet)

Auf dieser Seite wird ein Feature dokumentiert, das in zukünftigen Versionen von Windows Media Player und dem Windows Media Player SDK möglicherweise nicht verfügbar ist.

Ein Rahmen ähnelt einer Skin, aber anstatt die Benutzeroberfläche für den kompakten Modus von Windows Media Player zu ersetzen, wird ein Rahmen im Bereich Jetzt wiedergeben des vollständigen Modus Windows Media Player eingebettet.

Mithilfe eines Windows Media Download-Pakets können Sie Inhalte mit einem Rahmen einschließen und so den Weg zu Multimediaanwendungen ebnen.

Ein Beispiel Windows Mediendownloadpakets, das einen Rahmen und eingebetteten Inhalt enthält, ist im Beispielverzeichnis dieses SDK enthalten.

## <a name="creating-a-border"></a>Erstellen eines Rahmens

Ein Rahmen wird auf die gleiche Weise wie eine Skin erstellt. Der einzige Unterschied besteht darin, dass die Skin in den Bereich **Jetzt wiedergegeben** eingebettet ist. Dies bedeutet, dass die Skingröße nicht berechnet werden kann und dass alle Skinelemente relativ sein müssen. Wenn die Größe des Benutzers Windows Media Player geändert wird, können Teile des Rahmens abgeschnitten und nicht sichtbar sein.

## <a name="loading-a-border"></a>Laden eines Rahmens

Ein Rahmen wird geladen, wenn eine Windows Media-Metadatei geladen wird, die das **SKIN-Element** verwendet. Das **HREF-Attribut** des **SKIN-Elements** muss auf eine Skin verweisen. Ein typisches **SKIN-Element** würde wie folgt aussehen:


```C++
<SKIN HREF="myborder.wmz">

```



Weitere Informationen finden Sie unter [SKIN-Element (veraltet)](skin-element--deprecated.md).

## <a name="including-content-with-a-border"></a>Einschließen von Inhalten mit einem Rahmen

Sie können Inhalte mit einem Rahmen einschließen, indem Sie eine Windows Mediendownloaddatei (mit der Dateinamenerweiterung WMD) verwenden. Folgen Sie diesen Schritten:

1.  Erstellen Sie den Rahmen. Achten Sie darauf, sie so zu erstellen, dass die Größenänderung die Zusammensetzung des Rahmens nicht überrollt. Schließen Sie z. B. keine Hintergrunddatei ein. Machen Sie den Hintergrund transparent, sodass eine Visualisierung dahinter ausgeführt werden kann.
2.  Komprimieren Sie den Skininhalt (Art, JScript dateien und Skindefinitionsdatei) in eine Datei mit der Dateinamenerweiterung .wmz.
3.  Erstellen Sie eine Windows Media-Metadatei (mit der Dateinamenerweiterung ASX), die auf die komprimierte Rahmendatei verweist (mit der Dateinamenerweiterung .wmz). Die Metadatei kann Wiedergabelisteninformationen mit Metadaten für Art und URLs für bestimmte Inhalte enthalten.
4.  Stellen Sie die Inhalte digitaler Medien zusammen.
5.  Komprimieren Sie Rahmen, Metadatei und Inhalt in einer Datei, und geben Sie ihr eine WMD-Dateinamenerweiterung.

## <a name="using-a-border"></a>Verwenden eines Rahmens

Nachdem Sie die Windows Mediendownloaddatei erstellt haben, muss der Benutzer nur noch darauf doppelklicken. Die Datei wird auf den Computer des Benutzers heruntergeladen. Die Dateien im Paket werden entpackt, die Wiedergabeliste wird den Wiedergabelisten hinzugefügt, der Rahmen wird im Bereich **Jetzt wiedergegeben** des vollständigen Modus Windows Media Player angezeigt, und das erste Element in der neuen Wiedergabeliste beginnt mit der Wiedergabe.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen zu Skins**](about-skins.md)
</dt> <dt>

[**Beispiele**](samples.md)
</dt> <dt>

[**Windows Mediendownloadpakete (veraltet)**](windows-media-download-packages--deprecated.md)
</dt> </dl>

 

 




