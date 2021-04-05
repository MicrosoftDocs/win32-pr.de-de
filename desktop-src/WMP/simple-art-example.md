---
title: Beispiel für einfache Kunst
description: Beispiel für einfache Kunst
ms.assetid: e17c29c3-3bc6-43f5-83e1-94005218417f
keywords:
- Windows Media Player Skins, Grafikdateien
- Skins, Art Dateien
- Dateien für Skins, Art
- kunstdateien für Skins, Beispiele
- Windows Media Player Skins, Beispiele
- Skins, Beispiele
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cab7b25dc33da70a627f8b0e126d6797b1bcdd9f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710008"
---
# <a name="simple-art-example"></a>Beispiel für einfache Kunst

Drei kunstdateien sind erforderlich, um eine einfache Skin mit zwei Schaltflächen zu erstellen. Ein primäres Image und ein Mapping-Image sind erforderlich, und ein alternatives Bild bietet dem Benutzer einen visuellen Hinweis darauf, dass eine Schaltfläche klickbar ist.

Diese kunstdateien wurden in einem Kunstprogramm erstellt, das Ebenen verwendet. Durch die Verwendung von Ebenen ist es einfacher, sicherzustellen, dass das primäre, das Mapping-und das alternative Image die gleiche Größe haben und einander zueinander stehen.

Ausführliche Anweisungen zum Erstellen der Kunst finden Sie im [Handbuch zur Erstellung von Skin](skin-creation-guide.md).

## <a name="primary-image"></a>Primäres Bild

Das primäre Abbild ist ein einfaches gelbes Oval mit zwei Schaltflächen, ein rosa zum Starten von Windows Media Player und eine violette Schaltfläche, um es anzuhalten. Der Hintergrund ist etwas dunkler gelb als das Oval. Dieses Bild wird in der folgenden Abbildung dargestellt.

![primäres Image](images/absam01b.png)

Das primäre Abbild stammt aus den folgenden Images, jeweils in einer separaten Ebene. Zuerst wurde eine Oval mit einer ebenenschrägung und einem Prägung-Effekt erstellt. Dieses Bild wird in der folgenden Abbildung dargestellt.

![Oval-Image](images/absam01s.png)

Anschließend wurden die beiden Schaltflächen erstellt, auch mit der ebenenschrägung und den Prägung-Effekten. Dies ist in der folgenden Abbildung dargestellt.

![zwei Schaltflächen](images/absam01p.png)

Im nächsten Schritt wurde der Bild Hintergrund erstellt. Es wurde ein etwas dunkleres gelbes ausgewählt, sodass alle Antialiasing zwischen dem Oval und dem Hintergrund nicht bemerkt werden. Der Farbwert ist \# CCCC00. Dieses Bild wird in der folgenden Abbildung dargestellt.

![Hintergrundbild](images/absam01y.png)

Die Ebenen, in denen diese Bilder enthalten waren, wurden sichtbar gemacht und als Kopie im Bitmapformat gespeichert, wodurch das primäre Image erstellt wurde. Das primäre zusammengesetzte Image wird vom **BackgroundImage** -Attribut des **Ansichts** Elements verwendet.

## <a name="mapping-image"></a>Bild Zuordnung

Ein Mapping-Bild wird benötigt, um anzugeben, wann und wo ein Skin geklickt wird. Ein Mapping-Bild wurde mit einem roten Bereich und einem grünen Bereich erstellt. Dieses Bild wird in der folgenden Abbildung dargestellt.

![Bild Zuordnung](images/absam01m.png)

Der grüne Bereich wird verwendet, um den Bereich auf der Skin zu identifizieren, der die Windows-Media Player startet, und der Rote Bereich wird verwendet, um ihn zu verhindern. Das Mapping-Image entspricht der Größe des primären Bilds.

Das Zuordnungsbild wurde erstellt, indem die Schaltflächen Ebene in eine neue Ebene kopiert und die Abschrägung und der Prägung-Effekt deaktiviert wurde. Flatimages werden für die Zuordnung benötigt, da Windows-Media Player in jedem Bereich nach einzelnen Farbwerten suchen werden. Sie kann nur nach einer von Ihnen definierten Farbe suchen, z. b \# . rot (FF0000). Wenn das Image eine Abschrägung oder eine andere Auswirkung hat, ist nicht alles genau das rote, das Sie benötigen.

Damit die zuordnungsschaltflächen leicht zu merken sind, wurden die Bilder mit reiner roter und reiner grüner Farbe gefüllt, aber es kann eine beliebige Farbe verwendet werden. Sie müssen sich die Farbnummern in der Zuordnung merken, damit Sie in der XML-Datei mit den Skin-Definitionen eingegeben werden können. In diesem Fall ist rot \# FF0000 und grün ist \# 00FF00.

Wenn nur die neue Ebene sichtbar ist, wurde das Image als Kopie in eine BMP-Datei gespeichert. Sie wird vom **mappingImage** -Attribut des **ButtonGroup** -Elements aufgerufen.

## <a name="alternate-image"></a>Alternatives Bild

Alternative Bilder sind nicht erforderlich, aber Sie sind sehr nützlich, um dem Benutzer visuelle Hinweise zu übergeben. In diesem Fall wird ein Hover-Bild empfohlen, damit der Benutzer weiß, auf welche Bereiche geklickt werden kann.

Ein alternatives Bild wurde mit zwei gelben Schaltflächen erstellt. Dies ist in der folgenden Abbildung dargestellt.

![Bild mit Hover](images/absam01h.png)

Das alternative Bild wurde erstellt, indem die ursprüngliche Schaltflächen Ebene in eine neue Ebene kopiert und anschließend die Füllfarbe in Gelb geändert wurde. Der Effekt der einschrägung und der Prägung wurde beibehalten. Anschließend wurde eine neue Ebene erstellt, und es wurden Bilder hinzugefügt: der Pfeil gibt "Play" an, und das Quadrat zeigt "Ende" an. Wenn nur die neue gelbe Schaltfläche und die typebenen sichtbar sind, wurde das Bild als Kopie in eine Bitmapdatei gespeichert.

Das Ergebnis ist, dass wenn mit dem Mauszeiger auf einen durch das Zuordnungsbild definierten Bereich gezeigt wird, das Hover-Bild angezeigt wird, um den Reader zu warnen, dass Sie die Windows-Media Player wiedergeben oder beenden können, wenn Sie auf diese Stelle klicken.

## <a name="final-image"></a>Endgültiges Image

Hier ist das endgültige Bild der Skin.

![Endgültiges Image](images/absam01f.png)

Das Bild wird angezeigt, wenn Sie auf der rechten Seite auf die rosa Schaltfläche zeigen.

![zeigen Sie auf die Rechte Schaltfläche](images/absam01r.png)

## <a name="xml-code-for-the-art-example"></a>XML-Code für das Beispiel "Kunst"

Die Details zum Schreiben von XML-Code finden Sie im [Handbuch zur Erstellung von Skin](skin-creation-guide.md), aber um zu veranschaulichen, wie wenig Code zum Erstellen einer funktionierenden Skin benötigt wird, finden Sie hier den Code für die-Grafik in diesem Beispiel.

Für die Funktionen zum wiedergeben und Abbrechen werden vordefinierte Schaltflächen verwendet. Sie müssen eine Datei oder eine Wiedergabeliste aus dem Windows Media-Anker laden. Wenn Windows Media Player in den Skin-Modus wechselt, wird ein kleines Feld in der unteren rechten Ecke des Bildschirms angezeigt. Dieses Feld wird als "Anker" bezeichnet. Wenn Sie auf den Anker klicken, erhalten Sie die erforderliche Mindestfunktionalität, falls ein Skin keine Möglichkeit bietet, zum vollständigen Modus von Windows Media Player zurückzukehren. Der Benutzer kann mithilfe des Menüs **Ansicht** im vollständigen Modus oder durch Klicken auf den Anker im Skin-Modus zwischen den Modi wechseln.


```C++
<THEME>
    <VIEW
        clippingColor = "#CCCC00"
        backgroundImage = "background.bmp"
        titleBar = "false">
         
        <BUTTONGROUP
            mappingImage = "map.bmp"
            hoverImage = "hover.bmp">
                
        <PLAYELEMENT
            mappingColor = "#00FF00"/>

        <STOPELEMENT
            mappingColor = "#FF0000"/>
                
        </BUTTONGROUP>
    </VIEW>
</THEME>

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Kunstdateien**](art-files.md)
</dt> </dl>

 

 




