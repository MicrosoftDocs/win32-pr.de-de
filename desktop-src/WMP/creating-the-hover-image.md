---
title: Erstellen des Hoverbilds
description: Erstellen des Hoverbilds
ms.assetid: 169a99ba-96a0-4487-aa1c-07c83c0bc237
keywords:
- Erstellen von Skins, Zeigen auf Bilder
- Windows Media Player skins,art files
- Skins,Art-Dateien
- Dateien für Skins,Art
- Artdateien für Skins,Hoverbilder
- Windows Media Player skins,hover images
- Skins,Hoverbilder
- Zeigen auf Bilder in Skins
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88eff91123a28dae94425d7ea6e7591462545a2d7da0372b088eeec6bd67ed60
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119902280"
---
# <a name="creating-the-hover-image"></a>Erstellen des Hoverbilds

Das primäre Bild dieser Skin sind zwei Schaltflächen, die auf einem Oval stehen. Um dem Benutzer einen Hinweis zu geben, was zu tun ist, können Sie Bilder mit dem Hover hinzufügen. Dies sind alternative Bilder, die angezeigt werden, wenn der Benutzer mit der Maus auf eine Schaltfläche zeigt. Die Hoverschaltflächen enthalten auch die Wiedergabe- und Stopp-VCR-Steuerelementsymbole, damit Benutzer genau wissen, was sie tun können. Mithilfe von Bildern mit Hover können Sie komplexe, selbstdokumentierende, erklärende Skins erstellen.

Um das Bild mit dem Hover zu erstellen, müssen Sie die beiden Schaltflächen, die Sie für die primäre Grafikdatei erstellt haben, auf neue Ebenen kopieren und weitere Ebenen für den Text hinzufügen. Führen Sie die folgenden Schritte durch:

1.  Kopieren Sie die Schaltflächenebene Schließen, und benennen Sie sie in "Hover schließen" um.
2.  Verwenden Sie Farbwähler , um eine Vordergrundfarbe eines hellgelben \# (CCFF33) zu erstellen. Dies wurde ausgewählt, um den Kontrast zu den Schaltflächenfarben zu erzeugen. Verwenden Sie dann das Paint Buckettool, um das Innere des Kreises in der Hoverebene Schließen zu füllen.
3.  Kopieren Sie die Wiedergabeschaltfläche, und benennen Sie sie in "Wiedergabe mit dem Hover" um.
4.  Verwenden Sie Paint Buckettool, um das Innere des Kreises in der Wiedergabe-Hoverebene mit der gleichen Farbe wie der Schließen-Hoverkreis zu füllen.
5.  Erstellen Sie eine neue Ebene, und nennen Sie sie "Close square". Verwenden Sie die Farbwähler, um eine Vordergrundfarbe von Dunkelblau zu erstellen. Verwenden Sie das Stifttool, um ein Quadrat zu zeichnen, es in eine Auswahl zu verwandeln, es zu füllen und den Pfad zu löschen. Bewegen Sie das Quadrat mithilfe des Move-Tools, und zentriert es über die Schaltfläche Hover schließen.
6.  Erstellen Sie eine neue Ebene, und nennen Sie sie "Play triangle". Verwenden Sie das Stifttool, um das Dreieck für "Play" mit den gleichen Techniken zu erstellen, die Sie beim Erstellen der quadratischen Ebene Schließen verwendet haben. Zentriert sie über der Wiedergabeschaltfläche mit dem Hover.

Sie können nun die Hoverartdatei erstellen. Blenden Sie alle Ebenen aus, und zeigen Sie dann nur die folgenden Ebenen in dieser Reihenfolge an (von oben nach unten):

Wiedergabedreieck

Schließen des Quadrats

Wiedergabe mit dem Hover

Schließen mit dem Hover

Speichern Sie in einer neuen Datei, indem Sie im Menü Datei den Befehl Kopie speichern verwenden. Wählen Sie die Option BMP im Abschnitt Speichern unter des Dialogfelds Kopie speichern aus, und geben Sie einen Dateinamen ein, auf den Sie später in der Skindefinitionsdatei verweisen. Im Idealfall sollten Sie diese im gleichen Verzeichnis wie Ihre Skindefinitionsdatei speichern. Sie können diesen Aufruf beispielsweise hover.bmp. Wählen Sie die Standardeinstellungen aus, und speichern Sie die Datei.

Ihre Hoverartdatei sollte wie in der folgenden Abbildung aussehen.

![Bild mit dem Hover](images/absam01h.png)

Die gelbe Hoverschaltfläche wird statt der normalen Schaltfläche angezeigt. Wenn Sie auf die rechte Schaltfläche in Ihrer Skin zeigen, wird die gelbe Schaltfläche mit der Bezeichnung "Play" angezeigt, und wenn Sie auf die linke Schaltfläche zeigen, wird dem Benutzer "Schließen" angezeigt. Die beiden Bilder mit dem Mauszeiger werden nie gleichzeitig angezeigt, da die Maus nicht gleichzeitig auf beide Schaltflächen zeigen kann. Sie müssen das Hovern aktivieren und über eine Hoverartdatei verfügen, die den Bereichen der Zuordnungsdateien zu Bereichen der Hoverdatei entspricht.

Wenn Sie Ihre Datei speichern, wird der von Ihnen verwendete Dateiname später als Wert für das **hoverImage-Attribut** des **BUTTONGROUP-Elements** in Ihrer Skindefinitionsdatei verwendet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Erstellen Ihres ersten Skins**](building-your-first-skin.md)
</dt> </dl>

 

 




