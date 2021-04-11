---
title: Rahmen für Windows-Media Player (veraltet)
description: Rahmen für Windows-Media Player (veraltet)
ms.assetid: defa461b-ffa5-4fee-bed4-aba3e733b8c4
keywords:
- Windows-Media Player, Rahmen
- Windows Media Player Skins, Rahmen
- Skins, Rahmen
- Rahmen im Vergleich zu Skins
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a48ff3ec17230002e9c6b4a1eb17e3024375a58
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309983"
---
# <a name="borders-for-windows-media-player-deprecated"></a>Rahmen für Windows-Media Player (veraltet)

Diese Seite dokumentiert eine Funktion, die in zukünftigen Versionen von Windows Media Player und dem Windows Media Player SDK möglicherweise nicht verfügbar ist.

Ein Rahmen ähnelt einem Skin, aber anstatt die Benutzeroberfläche für den Compact-Modus von Windows Media Player zu ersetzen, wird ein Rahmen in den Bereich "jetzt wiedergegeben" der Windows-Media Player im Vollmodus eingebettet.

Mithilfe eines Windows Media-Download Pakets können Sie Inhalte mit einem Rahmen einschließen, um Multimedia-Anwendungen zu nutzen.

Ein Beispiel für ein Windows-Medien Download Paket, das einen Rahmen und eingebetteten Inhalt enthält, ist im Verzeichnis "Samples" dieses SDK enthalten.

## <a name="creating-a-border"></a>Erstellen eines Rahmens

Ein Rahmen wird auf die gleiche Weise wie ein Skin erstellt. Der einzige Unterschied besteht darin, dass die Skin in den Bereich für die wieder **Gabe** eingebettet ist. Dies bedeutet, dass die Skin-Größe nicht berechnet werden kann und dass alle Skin-Elemente relativ sein müssen. Wenn der Benutzer die Größe des Windows-Media Player ändert, sind Teile des Rahmens möglicherweise abgeschnitten und werden nicht angezeigt.

## <a name="loading-a-border"></a>Laden eines Rahmens

Ein Rahmen wird geladen, wenn eine Windows Media-Metadatendatei geladen wird, die das **Skin** -Element verwendet. Das **href** -Attribut des **Skin** -Elements muss auf ein Skin verweisen. Ein typisches **Skin** -Element würde wie folgt aussehen:


```C++
<SKIN HREF="myborder.wmz">

```



Weitere Informationen finden Sie unter [Skin-Element (veraltet)](skin-element--deprecated.md).

## <a name="including-content-with-a-border"></a>Einschließen von Inhalten mit einem Rahmen

Sie können Inhalte mit einem Rahmen mithilfe einer Windows Media-Download Datei (mit der Dateinamenerweiterung ". WMD") einschließen. Führen Sie die folgenden Schritte aus:

1.  Erstellen Sie den Rahmen. Achten Sie darauf, dass Sie diese so erstellen, dass die Größe des Rahmens durch die Größe der Größe nicht ruiniert wird. Fügen Sie z. b. keine Hintergrund Datei ein. machen Sie den Hintergrund transparent, damit eine Visualisierung dahinter ausgeführt werden kann.
2.  Komprimieren Sie den Inhalt der Skin (Kunst, JScript-Dateien und Skin-Definitionsdatei) in eine Datei mit der Dateinamenerweiterung. WMZ.
3.  Erstellen Sie eine Windows Media-Metadatendatei (mit der Dateinamenerweiterung ". asx"), die auf die komprimierte Rahmen Datei (mit der Dateinamenerweiterung ". WMZ") verweist. Die Metadatei kann Wiedergabelisten Informationen mit Metadaten für Kunst und URLs für bestimmten Inhalt enthalten.
4.  Assemblieren Sie den Inhalt der digitalen Medien.
5.  Komprimieren Sie den Rahmen, die Metadatendatei und den Inhalt in einer Datei, und versehen Sie Sie mit der Dateinamenerweiterung ". WMD".

## <a name="using-a-border"></a>Verwenden eines Rahmens

Nachdem Sie die Windows Media-Download Datei erstellt haben, muss der Benutzer lediglich darauf doppelklicken. Die Datei wird auf den Computer des Benutzers heruntergeladen. Die Dateien im Paket werden entpackt, die Wiedergabeliste wird den Wiedergabelisten hinzugefügt, der Rahmen wird im Fenster " **jetzt** wiedergegeben" des Windows-Media Player für den vollständigen Modus angezeigt, und das erste Element in der neuen Wiedergabeliste wird wiedergegeben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen zu Skins**](about-skins.md)
</dt> <dt>

[**Beispiele**](samples.md)
</dt> <dt>

[**Windows Media-Download Pakete (veraltet)**](windows-media-download-packages--deprecated.md)
</dt> </dl>

 

 




