---
title: Erstellen der primären Artdatei
description: Erstellen der primären Artdatei
ms.assetid: 50099050-2ce8-4cbf-82b7-3018f6579bd2
keywords:
- Erstellen von Skins,primäre Artdateien
- Windows Media Player skins,art files
- Skins,Art-Dateien
- Dateien für Skins,Art
- Artdateien für Skins,primäre Bilder
- Windows Media Player Skins,primäre Bilder
- Skins, primäre Bilder
- Primäre Bilder in Skins
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b21483e9b39692ad9eee7eb2cd7958f2fa70ddb7c2926877b84f3f537156bd55
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118341542"
---
# <a name="creating-the-primary-art-file"></a>Erstellen der primären Artdatei

Die primäre Artdatei enthält die Art, die dem Benutzer Ihrer Skin zuerst angezeigt wird. In diesem Fall erstellen Sie Bilder in verschiedenen Ebenen Ihres Artprogramms. Der Grund für die Verwendung von Ebenen ist, dass Sie später bestimmte Ebenen kopieren, um Kartendateien und alternative Artdateien zu erstellen.

Um die primäre Artdatei zu erstellen, erstellen Sie die folgenden Ebenen in der folgenden Reihenfolge:

Hintergrundebene "Skin"

Dies ist die Farbe, die transparent ist, wenn die Skin angezeigt wird. Erstellen Sie zuerst eine Ebene für diese, wählen Sie jedoch die endgültige Farbe dieser Ebene aus, nachdem Sie eine Farbe für die Skincontainerebene ausgewählt haben. Diese Farbe sollte der Skincontainerebene ähneln, aber nicht der gleichen sein, um Alle Antialiasingeffekte auszublenden.

Skincontainerebene

Dies ist das Bild, das den Umriss Ihrer Skin bildet und dem Benutzer angezeigt wird. Es wird auch der Container für die beiden Schaltflächen in diesem Beispiel sein. Stellen Sie sich Ihre Skin als Container für Steuerelemente der Benutzeroberfläche wie Schaltflächen, Schieberegler und so weiter vor. In diesem Beispiel ist der Container ein gelbes Oval.

Wiedergabe- und Schließen-Schaltflächenebenen

Dies sind die beiden Steuerelemente der Benutzeroberfläche, die in diesem Beispiel verwendet werden. Sie werden sie in separate Ebenen setzen, damit Sie sie problemlos anpassen oder später kopieren können.

Bevor Sie Ihre Ebenen erstellen, müssen Sie die Datei erstellen, die Ihre Ebenen enthalten soll. Starten Sie Ups, und erstellen Sie eine neue Datei, die 100 Pixel hoch und 200 Pixel breit ist. Die Datei, die zum Erstellen der Art für dieses Beispiel verwendet wird, wird als tiny.psd und ist im SDK enthalten.

Alle Anweisungen werden in Bezug auf Png angegeben, aber jedes andere Grafikprogramm kann zum Erstellen von Skins verwendet werden, solange Sie in einem der von Windows Media Player unterstützten Dateiformate (BMP, GIF, JPG und PNG) speichern können. Die Erstellung von Skins ist einfacher, wenn Sie ein Bildprogramm mit Ebenen verwenden, z. B. Adobe Adobe, Jasc Paint Shop Pro oder Jedor Bzw. Jedor Bzw. Jedor. Ebenen sind äußerst nützlich, da Bilder für die Bildzuordnung und die Anzeige alternativer Bilder ordnungsgemäß ausgerichtet werden müssen.

## <a name="skin-background-layer"></a>Skin-Hintergrundebene

Erstellen Sie eine neue Ebene, und nennen Sie sie "Skin background". Dies wird die Transparenzfarbe, die Sie in der Skindefinitionsdatei definieren. Warten Sie, bis die Farbe für den Skincontainer ausgewählt ist, bevor Sie die Skinhintergrundebene mit einer bestimmten Farbe füllen.

## <a name="skin-container-layer"></a>Skincontainerebene

Erstellen Sie als Nächstes eine neue Ebene, und nennen Sie sie "Skin container". Dies definiert die Ränder Ihrer Skin und ist der Container für die Schaltflächen.

Wählen Sie mithilfe der Webfarbschieberegler eine Vordergrundfarbe für die Form aus. In diesem Beispiel wurde die Farbe \# "DBDD11" ausgewählt.

Erstellen Sie als Nächstes eine ovale Form. Die einfachste Möglichkeit besteht in der Verwendung des Tools Eliptical Marquee und der Erstellung einer ovalen Auswahl. Wenn Sie eine ovale Auswahl erstellt haben, die der von Ihnen ausgewählten Größe und Form ist, füllen Sie die Auswahl mit der Vordergrundfarbe aus, und brechen Sie die Auswahl ab.

Um dieses Aussehen noch interessanter zu machen, wenden Sie den Ebeneneffekt von Abschräge und Emboss mit den Standardwerten an.

Ihre Skincontainerebene sollte wie in der folgenden Abbildung aussehen.

![Skincontainerebene](images/g01cont.png)

## <a name="background-skin-color"></a>Hintergrund-Skinfarbe

Nachdem Sie nun eine Vordergrundfarbe für Ihre Skincontainerform ausgewählt haben, können Sie eine ähnliche Farbe für Ihre Skinhintergrundebene auswählen. Sie möchten nicht genau dieselbe Farbe, oder Ihr Skincontainer ist auch transparent. Achten Sie darauf, dass Sie diese Farbe nicht an einer anderen Stelle in Ihrer Skin verwenden, auch nicht auf Fotos, da das Desktopbild an jedem Ort, an dem diese Farbe angezeigt wird, stattdessen angezeigt wird.

Sie möchten eine Farbe in der Nähe der Skincontainerfarbe, um Antialiasingeffekte zu vermeiden. Wenn Sie z. B. einen schwarzen Hintergrund haben, werden möglicherweise einige Schwarze am Rand Ihrer Skin gezeigt. Wenn Sie eine Farbe auswählen, die der Farbe des Skincontainers nahe kommt, werden alle im Antialiasingprozess angezeigten verirrten Pixel unbemerkt angezeigt.

Antialiasing ist der Prozess der Glättung der Kanten von geschwungenen oder gekrümmten Formen. Antialiasing erstellt neue Farben für Pixel entlang der Ränder einer Form, die eine Mischung aus Vordergrundfarbe und Hintergrundfarbe sind. Einige dieser Zwischenfarben können dazu führen, dass Pixel übersehen werden, wenn die Hintergrundfarbe transparent gemacht wird.

Ihre Hintergrundebene sollte wie in der folgenden Abbildung aussehen.

![Hintergrund-Skinebene](images/g01backg.png)

## <a name="play-and-close-button-layers"></a>Wiedergabe- und Schließen-Schaltflächenebenen

Erstellen Sie eine neue Ebene, und nennen Sie sie "Schaltfläche schließen". Erstellen Sie mit dem Auswahltool Eliptical Marquee erneut einen Kreis, und positionieren Sie ihn auf der linken Seite des Gesamtbilds. Aktivieren Sie die Sichtbarkeit der Skincontainerdatei, um die Auswahl zu platzieren.

Wenn Sie mit der Platzierung zufrieden sind, füllen Sie die Auswahl mit einer beliebigen Farbe aus (mit Ausnahme der Farbe des Skincontainers oder des Skinhintergrunds). In diesem Beispiel wurde eine violette Farbe ausgewählt. Sie müssen sich die Anzahl der Farben nicht merken. Brechen Sie dann die Auswahl ab, und wenden Sie einen weiteren Standardeffekt der Abschräge- und Emboss-Schicht an. Wenn Sie Nichtebeneneffekte auf Ihre Schaltfläche anwenden möchten, erstellen Sie eine Kopie des Originals für die spätere Verwendung in der Zuordnung.

Die Schaltfläche Schließen sollte wie in der folgenden Abbildung aussehen.

![Schließ-Schaltfläche](images/g01qbut.png)

Erstellen Sie eine neue Ebene, und nennen Sie sie "Wiedergabeschaltfläche". Verwenden Sie die gleichen Techniken wie für die Schaltfläche Schließen, aber geben Sie ihr eine andere Farbe. In diesem Fall wurde eine rosafarbene Schaltflächenfarbe ausgewählt, aber jede Farbe kann verwendet werden, solange sie nicht die gleiche Farbe wie der Skincontainer (da sie sich in den Container einblenden würde) oder die Hintergrundfarbe der Skin (da sie transparent wird).

Die Wiedergabeschaltfläche sollte wie in der folgenden Abbildung aussehen.

![Wiedergabeschaltfläche](images/g01pbut.png)

## <a name="combine-layers-and-save"></a>Kombinieren von Ebenen und Speichern

Sie können nun die primäre Artdatei erstellen. Blenden Sie alle Ebenen aus, und zeigen Sie dann nur die folgenden Ebenen in dieser Reihenfolge an (von oben nach unten):

Wiedergabeschaltfläche

Schaltfläche „Schließen“

Skincontainer

Skinhintergrund

Speichern Sie in einer neuen Datei, indem Sie im Menü Datei den Befehl Kopie speichern verwenden. Wählen Sie die BMP-Option im Abschnitt Speichern unter des Dialogfelds Kopie speichern aus, und geben Sie einen Dateinamen ein, auf den Sie später in der Skindefinitionsdatei verweisen. Im Idealfall sollten Sie diese im gleichen Verzeichnis wie Ihre Skindefinitionsdatei speichern. Sie können diesen Aufruf beispielsweise background.bmp. Wählen Sie die Standardeinstellungen aus, und speichern Sie die Datei.

Ihre primäre Artdatei sollte wie dies aussehen:

![Primäre Artdatei](images/g01prime.png)

Sie verwenden diesen Dateinamen als Wert für das **backgroundImage-Attribut** des **VIEW-Elements** in Ihrer Skindefinitionsdatei.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Erstellen Ihres ersten Skins**](building-your-first-skin.md)
</dt> </dl>

 

 




