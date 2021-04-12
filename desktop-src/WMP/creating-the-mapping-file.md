---
title: Erstellen der Mapping-Datei
description: Erstellen der Mapping-Datei
ms.assetid: d882cd5b-1404-4dfd-8b51-a61e1505fae1
keywords:
- Erstellen von Skins, Mapping von Dateien
- Windows Media Player Skins, Grafikdateien
- Skins, Art Dateien
- Dateien für Skins, Art
- kunstdateien für Skins, Mapping von Bildern
- Windows Media Player Skins, Mapping von Bildern
- Skins, Mapping von Bildern
- Zuordnung von Bildern in Skins
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e49b71682f48ecdba098f76a9e27f656b27d5fe8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104387987"
---
# <a name="creating-the-mapping-file"></a>Erstellen der Mapping-Datei

Nachdem Sie die Bestandteile ihrer primären Grafikdatei erstellt haben, ist es relativ einfach, eine Mapping-Datei zu erstellen. Sie erstellen die neue Mapping-Datei, indem Sie die Kunst aus den beiden Schaltflächen Ebenen kombinieren, die Sie bereits erstellt haben.

1.  Sie müssen die beiden Schaltflächen, die Sie für die primäre Grafikdatei erstellt haben, in eine neue Ebene kopieren. Führen Sie die folgenden Schritte aus: Kopieren Sie die Schaltflächen Ebene schließen, entfernen Sie alle Ebeneneffekte, und benennen Sie Sie mit "Karte schließen" um. Die Kunst sollte flach und ohne Becks aussehen.
2.  Verwenden Sie die Farbauswahl, um eine Vordergrundfarbe der reinen roten Farbe zu erstellen. Stellen Sie sicher, dass der Wert für die Farbnummer " \# FF0000" lautet. Verwenden Sie dann das Füllwerkzeug Tool, um die Innenseite des Kreises der Kartenebene zu schließen.
3.  Kopieren Sie die Wiedergabe Schaltfläche, entfernen Sie alle Ebeneneffekte, und benennen Sie Sie "Wiedergabe Map" um. Auch hier sollte die Kunst flach aussehen. Sie sollten keine Auswirkungen auf die Zuordnungs Ebene haben, da Sie nur Bereiche der Bitmap definieren, die von Windows Media Player verwendet werden, um zu bestimmen, wo die Maus eine Aktion ausführt und was Sie damit tun möchten.
4.  Verwenden Sie die Farbauswahl, um die Vordergrundfarbe rein grün zu erstellen. Stellen Sie sicher, dass der Wert für die Farbnummer " \# 00FF00" lautet. Verwenden Sie dann das Füllwerkzeug Tool, um das Innere des Kreises der Wiedergabe Kartenebene auszufüllen.

Sie sind jetzt bereit, die DateiDatei für die Zuordnung zu erstellen. Blenden Sie alle Ebenen aus, und zeigen Sie in dieser Reihenfolge (von oben nach unten) nur die folgenden Ebenen an:

Wiedergabe Karte

Karte schließen

Speichern Sie die Datei in einer neuen Datei, indem Sie im Menü Datei den Befehl Kopie speichern verwenden. Wählen Sie im Bereich speichern als des Dialog Felds Kopie speichern die Option BMP aus, und geben Sie einen Dateinamen ein, auf den Sie später in der Skin-Definitionsdatei verweisen werden. Im Idealfall sollte Sie sich im gleichen Verzeichnis befinden wie Ihre Skin-Definitionsdatei. Beispielsweise können Sie diese Datei map.bmp abrufen. Wählen Sie die Standardeinstellungen aus, und speichern Sie die Datei.

Die Mapping-Datei sollte wie in der folgenden Abbildung aussehen.

![mapping file](images/g01map.png)

Wie Sie vielleicht vermuten, wird der grüne Bereich verwendet, um zu bestimmen, wann Windows Media Player gestartet werden soll, und der Rote Bereich ist, ihn zu beenden. Es können zwei Farben verwendet werden, sofern Sie die Farbnummern beim Einrichten der Skin-Definitionsdatei verwenden. Stellen Sie sicher, dass die Farben in der Karte reine Farben für die Region sind, die Sie verwenden möchten, und über unterschiedliche Kanten verfügen. Eine reine Farbe wäre eine, bei der jedes einzelne Pixel im Bereich denselben Farbwert hat. Durch die Verwendung eines Effekts kann der Rand weich oder verzerrt werden, wodurch die Farben einiger Pixel etwas verändert werden. Die Mapping-Datei wird nur von der Maus angezeigt, nicht von einem Menschen, Sie sollten Sie daher nicht schmücken und alle Ebeneneffekte entfernen, die Sie möglicherweise aus anderen Ebenen übernommen haben.

Wenn Sie die Datei speichern, wird der Dateiname, den Sie auswählen, später als Wert für das **mappingImage** -Attribut des **ButtonGroup** -Elements in der Skin-Definitionsdatei verwendet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Aufbauen Ihrer ersten Skin**](building-your-first-skin.md)
</dt> </dl>

 

 




