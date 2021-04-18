---
title: Erstellen der primären Grafikdatei
description: Erstellen der primären Grafikdatei
ms.assetid: 50099050-2ce8-4cbf-82b7-3018f6579bd2
keywords:
- Erstellen von Skins, Primary Art-Dateien
- Windows Media Player Skins, Grafikdateien
- Skins, Art Dateien
- Dateien für Skins, Art
- kunstdateien für Skins, primäre Bilder
- Windows Media Player Skins, primäre Images
- Skins, primäre Bilder
- primäre Images in Skins
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9ceb92a5a87c1fc03ec7336a7ca5dd7814e4a1c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104562369"
---
# <a name="creating-the-primary-art-file"></a>Erstellen der primären Grafikdatei

Die primäre Grafikdatei enthält die Kunst, die der Benutzer Ihrer Skin zuerst sieht. In diesem Fall erstellen Sie Images auf unterschiedlichen Ebenen Ihres Kunstprogramms. Der Grund für die Verwendung von Ebenen ist, dass Sie bestimmte Ebenen später kopieren, um Kartendateien und Alternative kunstdateien zu erstellen.

Zum Erstellen der primären Grafikdatei erstellen Sie die folgenden Ebenen in der folgenden Reihenfolge:

Skin-Hintergrund Ebene

Dies ist die Farbe, die transparent ist, wenn die Skin angezeigt wird. Erstellen Sie zuerst eine Ebene, aber wählen Sie die endgültige Farbe dieser Ebene aus, nachdem Sie eine Farbe für die Skin-Container Ebene ausgewählt haben. Diese Farbe sollte ähnlich wie die Skin-Container Schicht sein, um Antialiasing-Effekte auszublenden.

Skin-Container Ebene

Dies ist das Bild, das die Gliederung ihrer Skin bildet und die dem Benutzer angezeigt wird. Es ist auch der Container für die beiden Schaltflächen in diesem Beispiel. Stellen Sie sich Ihre Skin als Container für Steuerelemente der Benutzeroberfläche wie Schaltflächen, Schieberegler usw. vor. In diesem Beispiel ist der Container ein gelbes Oval.

Schaltflächen Ebenen wiedergeben und schließen

Dies sind die beiden Steuerelemente der Benutzeroberfläche, die in diesem Beispiel verwendet werden. Sie werden Sie in separaten Ebenen platzieren, damit Sie Sie problemlos anpassen oder später kopieren können.

Bevor Sie die Ebenen erstellen, müssen Sie die Datei erstellen, die die Ebenen enthält. Starten Sie Photoshop, und erstellen Sie eine neue Datei, die 100 Pixel hoch und 200 Pixel breit ist. Die Datei, die zum Erstellen der Kunst für dieses Beispiel verwendet wird, wird als tiny.psd bezeichnet und ist im SDK enthalten.

Alle Anweisungen werden in Form von Photoshop angegeben, aber jedes andere Kunstprogramm kann zum Erstellen von Skins verwendet werden, solange Sie in einem der Dateiformate speichern können, die von der Windows-Media Player unterstützt werden (BMP, GIF, JPG und PNG). Sie werden die Skin-Erstellung vereinfachen, wenn Sie ein Kunstprogramm verwenden, das über Ebenen wie Adobe Photoshop, Jasc Paint Shop Pro oder jedor-viskosity verfügt. Ebenen sind äußerst nützlich, da Bilder ordnungsgemäß für die Bild Zuordnung und die Anzeige alternativer Bilder ausgerichtet werden müssen.

## <a name="skin-background-layer"></a>Skin-Hintergrund Ebene

Erstellen Sie eine neue Ebene, und nennen Sie Sie "Skin Background". Dies wird zu der Transparenz Farbe, die Sie in der Skin-Definitionsdatei definieren. Warten Sie, bis die Farbe für den Skin-Container ausgewählt ist, bevor Sie die Hintergrund Ebene der Skin mit einer bestimmten Farbe auffüllen.

## <a name="skin-container-layer"></a>Skin-Container Ebene

Erstellen Sie als nächstes eine neue Ebene, und nennen Sie Sie "Skin Container". Dadurch werden die Kanten ihrer Skin definiert, und es handelt sich um den Container für die Schaltflächen.

Wählen Sie mithilfe der Webfarb Schieberegler eine Vordergrundfarbe für die Form aus. In diesem Beispiel wurde die Farbe " \# DBDD11" ausgewählt.

Erstellen Sie als nächstes eine Oval-Form. Die einfachste Möglichkeit besteht darin, das Eliptical-Marquee-Tool zu verwenden und eine Oval-Auswahl zu erstellen. Wenn Sie eine Oval-Auswahl erstellt haben, die die gewünschte Größe und Form hat, füllen Sie die Auswahl mit der Vordergrundfarbe aus, und brechen Sie die Auswahl ab.

Um dieses Aussehen etwas interessanter zu gestalten, wenden Sie den Ebeneneffekt von "Bevel" und "emboss" auf die Standardwerte an.

Ihre Skin-Container Schicht sollte wie in der folgenden Abbildung aussehen.

![Skin-Container Ebene](images/g01cont.png)

## <a name="background-skin-color"></a>Farbe für Hintergrundfarbe

Nachdem Sie nun eine Vordergrundfarbe für Ihre Skin-Container-Form ausgewählt haben, können Sie eine ähnliche Farbe für die Hintergrund Ebene der Skin auswählen. Sie möchten nicht genau dieselbe Farbe, oder der Skin-Container ist auch transparent. Stellen Sie sicher, dass Sie diese genaue Farbe nicht an einer anderen Stelle in der Skin verwenden, sogar in Fotos, denn immer, wenn diese Farbe angezeigt wird, wird stattdessen das Desktop Bild angezeigt.

Sie möchten eine Farbe in der Nähe der Skin-Container Farbe, um Antialiasing-Effekte zu vermeiden. Wenn Sie z. b. einen schwarzen Hintergrund haben, werden möglicherweise einige Teile von schwarz um den Rand der Skin angezeigt. Wenn Sie eine Farbe in der Nähe der Farbe des Skin-Containers auswählen, werden alle im Anti-Aliasing-Prozess aufzurufenden ungebundenen Pixel nicht angezeigt.

Antialiasing ist der Prozess der Glättung der Kanten von schrägen oder gekrümmten Formen. Antialiasing erstellt neue Farben für Pixel entlang der Kanten einer Form, die eine Mischung aus der Vordergrundfarbe und der Hintergrundfarbe sind. Einige dieser zwischen Farben können dazu führen, dass Pixel übersehen werden, wenn die Hintergrundfarbe transparent gemacht wird.

Die Hintergrund Ebene der Skin sollte wie in der folgenden Abbildung aussehen.

![Hintergrund-Skin-Ebene](images/g01backg.png)

## <a name="play-and-close-button-layers"></a>Schaltflächen Ebenen wiedergeben und schließen

Erstellen Sie eine neue Ebene, und benennen Sie Sie mit "Schaltfläche" Schließen ". Wenn Sie das Eliptical-Marquee-Auswahl Tool erneut verwenden, erstellen Sie einen Kreis und positionieren ihn auf der linken Seite des Gesamt Bilds. Aktivieren Sie die Sichtbarkeit der Skin-Containerdatei, um die Auswahl zu platzieren.

Wenn Sie mit der Platzierung zufrieden sind, füllen Sie die Auswahl mit einer beliebigen Farbe aus (außer der Farbe des Skin-Containers oder des Skin-Hintergrunds). In diesem Beispiel wurde eine lila Farbe ausgewählt. Sie müssen sich nicht die Anzahl der Farben merken. Brechen Sie dann die Auswahl ab, und wenden Sie eine weitere Standard Abschrägung und einen emboss-Ebenen Wenn Sie auf die Schaltfläche keine Ebeneneffekte anwenden möchten, erstellen Sie eine Kopie des Originals zur späteren Verwendung in der Zuordnung.

Die Schaltfläche schließen sollte wie in der folgenden Abbildung aussehen.

![Schließ-Schaltfläche](images/g01qbut.png)

Erstellen Sie eine neue Ebene, und benennen Sie Sie "Wiedergabe Schaltfläche". Verwenden Sie die gleichen Verfahren wie für die Schaltfläche "Schließen", aber weisen Sie eine andere Farbe zu. In diesem Fall wurde eine rosa Schaltflächen Farbe ausgewählt, aber jede Farbe kann verwendet werden, solange Sie nicht die gleiche Farbe wie der Skin-Container hat (da Sie in den Container integriert würde) oder die Hintergrundfarbe der Skin (da Sie transparent werden würde).

Die Wiedergabe Schaltfläche sollte wie in der folgenden Abbildung aussehen.

![Wiedergabe Schaltfläche](images/g01pbut.png)

## <a name="combine-layers-and-save"></a>Kombinieren von Ebenen und speichern

Nun können Sie die primäre Grafikdatei erstellen. Alle Ebenen ausblenden und dann nur die folgenden Ebenen anzeigen (von oben nach unten):

Wiedergabeschaltfläche

Schaltfläche „Schließen“

Skin-Container

Skin-Hintergrund

Speichern Sie die Datei in einer neuen Datei, indem Sie im Menü Datei den Befehl Kopie speichern verwenden. Wählen Sie im Bereich speichern als des Dialog Felds Kopie speichern die Option BMP aus, und geben Sie einen Dateinamen ein, auf den Sie später in der Skin-Definitionsdatei verweisen werden. Im Idealfall sollten Sie diese im gleichen Verzeichnis speichern wie Ihre Skin-Definitionsdatei. Beispielsweise können Sie diese background.bmp nennen. Wählen Sie die Standardeinstellungen aus, und speichern Sie die Datei.

Ihre primäre Grafikdatei sollte wie folgt aussehen:

![primäre Grafikdatei](images/g01prime.png)

Sie verwenden diesen Dateinamen als Wert für das **BackgroundImage** -Attribut des **View** -Elements in der Skin-Definitionsdatei.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Aufbauen Ihrer ersten Skin**](building-your-first-skin.md)
</dt> </dl>

 

 




