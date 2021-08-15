---
title: Erstellen der primären Art-Datei
description: Erstellen der primären Art-Datei
ms.assetid: 50099050-2ce8-4cbf-82b7-3018f6579bd2
keywords:
- Erstellen von Skins, primäre Grafikdateien
- Windows Media Player Skins, Art-Dateien
- Skins, Art-Dateien
- Dateien für Skins, Art
- Grafikdateien für Skins, primäre Bilder
- Windows Media Player Skins, primäre Bilder
- Skins, primäre Images
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
# <a name="creating-the-primary-art-file"></a>Erstellen der primären Art-Datei

Die primäre Grafikdatei enthält die Grafik, die dem Benutzer Ihrer Skin zuerst angezeigt wird. In diesem Fall erstellen Sie Bilder in verschiedenen Ebenen Ihres Grafikprogramms. Der Grund für die Verwendung von Ebenen ist, dass Sie später bestimmte Ebenen kopieren, um Kartendateien und alternative Grafikdateien zu erstellen.

Um die primäre Grafikdatei zu erstellen, erstellen Sie die folgenden Ebenen in der folgenden Reihenfolge:

Skin-Hintergrundebene

Dies ist die Farbe, die transparent ist, wenn die Skin angezeigt wird. Erstellen Sie zunächst eine Ebene für diese, wählen Sie jedoch die endgültige Farbe dieser Ebene aus, nachdem Sie eine Farbe für die Skincontainerebene ausgewählt haben. Diese Farbe sollte der Ebene des Skincontainers ähneln, aber nicht mit dieser identisch sein, um Antialiasingeffekte auszublenden.

Skincontainerebene

Dies ist das Bild, das den Umriss Ihrer Skin bildet und dem Benutzer angezeigt wird. Es wird auch der Container für die beiden Schaltflächen in diesem Beispiel sein. Stellen Sie sich Ihre Skin als Container für Steuerelemente der Benutzeroberfläche wie Schaltflächen, Schieberegler usw. vor. In diesem Beispiel ist der Container ein gelbes Oval.

Wiedergabe- und Schließen-Schaltflächenebenen

Dies sind die beiden Steuerelemente der Benutzeroberfläche, die in diesem Beispiel verwendet werden. Sie werden in separaten Ebenen ablegt, sodass Sie sie einfach anpassen oder später kopieren können.

Bevor Sie Die Ebenen erstellen, müssen Sie die Datei erstellen, die Ihre Ebenen enthält. Starten Sie Photo, und erstellen Sie eine neue Datei mit einer Höhe von 100 Pixeln und einer Breite von 200 Pixeln. Die Datei, die zum Erstellen der Grafik für dieses Beispiel verwendet wird, heißt tiny.psd und ist im SDK enthalten.

Alle Anweisungen werden in Bezug auf Png gegeben, aber jedes andere Grafikprogramm kann verwendet werden, um Skins zu erstellen, solange Sie in einem der Dateiformate speichern können, die vom Windows Media Player unterstützt werden (BMP, GIF, JPG und PNG). Die Erstellung von Designs ist einfacher, wenn Sie ein Grafikprogramm verwenden, das über Ebenen verfügt, z. B. Adobe Adobe, Jasc Paint Shop Pro oder JedorLayery. Ebenen sind äußerst nützlich, da Bilder für die Bildzuordnung und Anzeige alternativer Bilder ordnungsgemäß ausgerichtet werden müssen.

## <a name="skin-background-layer"></a>Skin Background Layer

Erstellen Sie eine neue Ebene, und nennen Sie sie "Skin background". Dies wird zur Transparenzfarbe, die Sie in der Skindefinitionsdatei definieren. Warten Sie, bis die Farbe für den Skincontainer ausgewählt ist, bevor Sie die Hintergrundebene der Skin mit einer bestimmten Farbe füllen.

## <a name="skin-container-layer"></a>Skin-Containerebene

Erstellen Sie als Nächstes eine neue Ebene, und nennen Sie sie "Skin-Container". Dadurch werden die Ränder Der Skin definiert und ist der Container für die Schaltflächen.

Wählen Sie mithilfe der Webfarbschieberegler eine Vordergrundfarbe für die Form aus. In diesem Beispiel wurde die Farbe \# "DBDD11" ausgewählt.

Erstellen Sie als Nächstes eine ovale Form. Die einfachste Möglichkeit besteht darin, das Eliptical Marquee-Tool zu verwenden und eine ovale Auswahl zu erstellen. Wenn Sie eine ovale Auswahl erstellt haben, die der gewünschten Größe und Form entspricht, füllen Sie die Auswahl mit der Vordergrundfarbe aus, und brechen Sie die Auswahl ab.

Um dies etwas interessanter zu gestalten, wenden Sie schließlich den Ebeneneffekt von Abrägung und Emboss mit den Standardwerten an.

Ihre Skincontainerebene sollte wie in der folgenden Abbildung aussehen.

![Skincontainerebene](images/g01cont.png)

## <a name="background-skin-color"></a>Hintergrundfarbe der Skin

Nachdem Sie nun eine Vordergrundfarbe für Ihre Skincontainerform ausgewählt haben, können Sie eine ähnliche Farbe für Ihre Skinhintergrundebene auswählen. Sie möchten nicht genau dieselbe Farbe, oder Ihr Skincontainer ist ebenfalls transparent. Stellen Sie sicher, dass Sie diese farbe nicht an anderer Stelle in Ihrer Skin verwenden, auch nicht auf Fotos, da das Desktopbild stattdessen überall dort angezeigt wird, wo diese Farbe angezeigt wird.

Sie möchten eine Farbe in der Nähe der Farbe des Skincontainers, um Antialiasingeffekte zu vermeiden. Wenn Sie z. B. einen schwarzen Hintergrund haben, werden möglicherweise einige Teile von Schwarz um den Rand Ihrer Skin angezeigt. Wenn Sie eine Farbe in der Nähe der Farbe des Skincontainers auswählen, werden alle im Antialiasingprozess angezeigten verstrichenen Pixel unbemerkt.

Antialiasing ist der Prozess der Glättung der Ränder von schrägen oder gekrümmten Formen. Antialiasing erstellt neue Farben für Pixel entlang der Ränder einer Form, die eine Mischung aus Vordergrundfarbe und Hintergrundfarbe sind. Einige dieser Zwischenfarben können dazu führen, dass Pixel übersehen werden, wenn die Hintergrundfarbe transparent gemacht wird.

Ihre Skinhintergrundebene sollte wie in der folgenden Abbildung aussehen.

![Hintergrundskinebene](images/g01backg.png)

## <a name="play-and-close-button-layers"></a>Wiedergabe- und Schließen-Schaltflächenebenen

Erstellen Sie eine neue Ebene, und nennen Sie sie "Schaltfläche schließen". Erstellen Sie mit dem Auswahltool Eliptical Marquee erneut einen Kreis, und positionieren Sie ihn auf der linken Seite des Gesamtbilds. Aktivieren Sie die Sichtbarkeit der Skincontainerdatei, um die Auswahl zu platzieren.

Wenn Sie mit der Platzierung zufrieden sind, füllen Sie die Auswahl mit einer beliebigen Farbe aus (mit Ausnahme der Farbe des Skincontainers oder des Skinhintergrunds). In diesem Beispiel wurde eine violette Farbe ausgewählt. Sie müssen sich die Nummer der Farbe nicht merken. Brechen Sie dann die Auswahl ab, und wenden Sie einen weiteren Standardeffekt für Abrägungs- und Bettungsebenen an. Wenn Sie Nichtebeneneffekte auf Ihre Schaltfläche anwenden möchten, erstellen Sie eine Kopie des Originals zur späteren Verwendung in der Zuordnung.

Die Schaltfläche Schließen sollte wie in der folgenden Abbildung aussehen.

![Schließ-Schaltfläche](images/g01qbut.png)

Erstellen Sie eine neue Ebene, und nennen Sie sie "Wiedergabeschaltfläche". Verwenden Sie die gleichen Techniken wie für die Schaltfläche Schließen, geben Sie ihr jedoch eine andere Farbe. In diesem Fall wurde eine farbefarbene schaltflächenfarbene Farbe ausgewählt, aber jede Farbe kann verwendet werden, solange sie nicht die gleiche Farbe wie der Skincontainer (da sie sich in den Container einfügen würde) oder die Farbe des Skinhintergrunds (da sie transparent wird) ist.

Ihre Wiedergabeschaltfläche sollte wie in der folgenden Abbildung aussehen.

![Wiedergabeschaltfläche](images/g01pbut.png)

## <a name="combine-layers-and-save"></a>Kombinieren von Ebenen und Speichern

Sie können nun die primäre Grafikdatei erstellen. Blenden Sie alle Ebenen aus, und zeigen Sie dann nur die folgenden Ebenen in dieser Reihenfolge an (von oben nach unten):

Wiedergabeschaltfläche

Schaltfläche „Schließen“

Skincontainer

Skin-Hintergrund

Speichern Sie mithilfe des Befehls Kopie speichern im Menü Datei in einer neuen Datei. Wählen Sie im Abschnitt Speichern unter des Dialogfelds Kopie speichern die Option BMP aus, und geben Sie einen Dateinamen ein, auf den Sie später in der Skindefinitionsdatei verweisen. Im Idealfall sollten Sie dies im selben Verzeichnis speichern wie ihre Skindefinitionsdatei. Beispielsweise könnten Sie diese background.bmp aufrufen. Wählen Sie die Standardeinstellungen aus, und speichern Sie die Datei.

Ihre primäre Grafikdatei sollte wie folgt aussehen:

![Primäre Grafikdatei](images/g01prime.png)

Sie verwenden diesen Dateinamen als Wert für das **backgroundImage-Attribut** des **VIEW-Elements** in Ihrer Skindefinitionsdatei.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Erstellen Ihrer ersten Skin**](building-your-first-skin.md)
</dt> </dl>

 

 




