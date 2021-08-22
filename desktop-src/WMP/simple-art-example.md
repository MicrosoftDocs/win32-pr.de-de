---
title: Simple Art Example
description: Simple Art Example
ms.assetid: e17c29c3-3bc6-43f5-83e1-94005218417f
keywords:
- Windows Media Player skins,art files
- Skins,Art-Dateien
- Dateien für Skins,Art
- Artdateien für Skins,Beispiele
- Windows Media Player Skins,Beispiele
- Skins,Beispiele
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bbd50cb4ad0dbd76babd99439a885f9e77557d04e18f2698bb970effa23d6b7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119615948"
---
# <a name="simple-art-example"></a>Simple Art Example

Drei Art-Dateien sind erforderlich, um eine einfache Skin mit zwei Schaltflächen zu erstellen. Ein primäres Bild und ein Zuordnungsbild sind erforderlich, und ein alternatives Bild gibt dem Benutzer einen visuellen Hinweis darauf, dass auf eine Schaltfläche geklickt werden kann.

Diese Artdateien wurden in einem Artprogramm erstellt, das Ebenen verwendet. Durch die Verwendung von Ebenen können Sie einfacher sicherstellen, dass Ihre primären, Zuordnungs- und alternativen Images alle die gleiche Größe haben und sich aneinander befinden.

Die ausführlichen Anweisungen zum Erstellen der Technik finden Sie im [Handbuch zur Erstellung von Skins.](skin-creation-guide.md)

## <a name="primary-image"></a>Primäres Bild

Das primäre Bild ist ein einfaches gelbes Oval mit zwei Schaltflächen, einem orangefarbenen zum Starten Windows Media Player und einer violetten Schaltfläche, um es anzuhalten. Der Hintergrund ist etwas dunkler gelb als das Oval. Diese Abbildung ist in der folgenden Abbildung dargestellt.

![Primäres Image](images/absam01b.png)

Das primäre Bild wurde aus den folgenden Bildern in einer separaten Ebene geerbt. Zuerst wurde ein Oval mit einer Ebenenschräge und einem Emboss-Effekt erstellt. Diese Abbildung ist in der folgenden Abbildung dargestellt.

![ovales Bild](images/absam01s.png)

Anschließend wurden die beiden Schaltflächen erstellt, auch mit Ebenenschräge- und Prägeeffekten. Dies ist in der folgenden Abbildung dargestellt.

![Zwei Schaltflächen](images/absam01p.png)

Als Nächstes wurde der Bildhintergrund erstellt. Es wurde ein etwas dunkleres Gelb ausgewählt, damit kein Antialiasing zwischen dem Oval und dem Hintergrund bemerkt wird. Der Farbwert ist \# DANNC00. Diese Abbildung ist in der folgenden Abbildung dargestellt.

![Hintergrundbild](images/absam01y.png)

Die Ebenen, die diese Bilder enthalten, wurden sichtbar gemacht und als Kopie im Bitmapformat gespeichert, wodurch das primäre Bild erstellt wurde. Das primäre zusammengesetzte Bild wird vom **backgroundImage-Attribut** des **VIEW-Elements** verwendet.

## <a name="mapping-image"></a>Abbildung der Zuordnung

Ein Zuordnungsbild ist erforderlich, um anzugeben, wann und wo auf eine Skin geklickt wird. Es wurde ein Zuordnungsbild mit einem roten und einem grünen Bereich erstellt. Diese Abbildung ist in der folgenden Abbildung dargestellt.

![Zuordnungsbild](images/absam01m.png)

Der grüne Bereich wird verwendet, um den Bereich auf der Skin zu identifizieren, der Windows Media Player und der rote Bereich verwendet wird, um ihn anzuhalten. Das Zuordnungsbild hat die gleiche Größe wie das primäre Image.

Das Zuordnungsbild wurde erstellt, indem die Schaltflächenebene auf eine neue Ebene kopiert und der Abschräge- und Prägeeffekt deaktiviert wurde. Flache Bilder werden für die Zuordnung benötigt, Windows Media Player in jedem Bereich nach einzelnen Farbwerten sucht. Er kann nur nach einer von Ihnen festgelegten Farbe suchen, z. B. rot ( \# FF0000). Wenn Ihr Bild eine Abschräschung oder einen anderen Effekt hat, ist nicht alles genau rot, das Sie benötigen.

Um die Kartenschaltflächen zu einer leicht zu merkenden Farbe zu machen, wurden die Bilder mit reinem Rot und reinem Grün gefüllt, aber es kann eine beliebige Farbe verwendet werden. Sie müssen sich die Farbnummern in Ihrer Karte merken, damit sie in die XML-Skindefinitionsdatei eingegeben werden können. In diesem Fall ist Rot \# FF0000 und grün \# 00FF00.

Wenn dann nur die neue Ebene sichtbar ist, wurde das Bild als Kopie in eine BMP-Datei gespeichert. Sie wird vom **mappingImage-Attribut** des **BUTTONGROUP-Elements** aufgerufen.

## <a name="alternate-image"></a>Alternatives Image

Alternative Bilder sind nicht erforderlich, aber sehr nützlich, um dem Benutzer visuelle Hinweise zu geben. In diesem Fall wird ein Bild mit dem Hover empfohlen, damit der Benutzer weiß, auf welche Bereiche geklickt werden kann.

Ein alternatives Bild wurde mit zwei gelben Schaltflächen erstellt. Dies ist in der folgenden Abbildung dargestellt.

![Bild mit dem Hover](images/absam01h.png)

Das alternative Bild wurde erstellt, indem die ursprüngliche Schaltflächenebene auf eine neue Ebene kopiert und dann die Füllfarbe in Gelb geändert wurde. Der Abschräge- und Prägeeffekt wurde beibehalten. Anschließend wurde eine neue Ebene erstellt und Bilder hinzugefügt: Der Pfeil zeigt "play" und das Quadrat "stop" an. Wenn dann nur die neue gelbe Schaltfläche und die Typebenen sichtbar sind, wurde das Bild als Kopie in eine Bitmapdatei gespeichert.

Wenn der Mauszeiger mit dem Mauszeiger auf einen durch das Zuordnungsbild definierten Bereich zeigt, wird das Bild mit dem Mauszeiger angezeigt, und der Leser wird darauf aufmerksam, dass er beim Klicken auf diese Stelle auf diese Stelle spielen oder Windows Media Player.

## <a name="final-image"></a>Endgültiges Bild

Hier ist das endgültige Bild der Skin.

![endgültige Abbildung](images/absam01f.png)

Und dies ist das Bild, das Sie sehen, wenn Sie auf die rosa Schaltfläche auf der rechten Seite bewegen.

![Mit dem Hover auf die rechte Schaltfläche](images/absam01r.png)

## <a name="xml-code-for-the-art-example"></a>XML-Code für das Beispiel der Technik

Die Details zum Schreiben von XML-Code finden Sie im [Handbuch](skin-creation-guide.md)zur Erstellung von Skins. Um jedoch zu zeigen, wie wenig Code zum Erstellen einer funktionierenden Skin erforderlich ist, finden Sie hier den Code für die Grafik in diesem Beispiel.

Vordefinierte Schaltflächen werden für die Wiedergabe- und Stoppfunktionen verwendet. Sie müssen eine Datei oder Wiedergabeliste aus dem Medienanker Windows laden. Wenn Windows Media Player in den Skinmodus wechselt, wird in der unteren rechten Ecke des Bildschirms ein kleines Feld angezeigt. Dieses Feld wird als "Anker" bezeichnet. Wenn Sie auf den Anker klicken, erhalten Sie die erforderliche Mindestfunktionalität, falls eine Skin keine Möglichkeit bietet, zum vollständigen Modus der Windows Media Player. Der Benutzer kann im Vollmodus über das Menü Ansicht oder im Skinmodus auf den Anker klicken, um zwischen den Modi zu wechseln. 


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

[**Art-Dateien**](art-files.md)
</dt> </dl>

 

 




