---
title: Struktur der Skin-Definitionsdatei
description: Struktur der Skin-Definitionsdatei
ms.assetid: 6b9ea288-ec64-473b-b796-ab637517099a
keywords:
- Windows Media Player Skins, Skin-Definitions Dateien
- Skins, Skin-Definitions Dateien
- Dateien für Skins, Skin-Definition
- Skin-Definitions Dateien, Struktur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a64226fb918bcbf93c95ece52075e2c8e7ed13e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037229"
---
# <a name="skin-definition-file-structure"></a>Struktur der Skin-Definitionsdatei

Die Skin-Definitionsdatei muss einer bestimmten Struktur folgen. Sie beginnen **mit einem Design** Element, erstellen ein oder mehrere **Ansichts** Elemente und definieren dann jedes **Ansichts** Element mit den Benutzeroberflächen Elementen, die für den gewünschten Ansichtstyp geeignet sind.

## <a name="theme-elements"></a>Designelemente

Auf der obersten Ebene müssen Sie die Skin-Definitionsdatei **mit dem Design** -Element starten und damit schließen.


```C++
<THEME>
    ...
</THEME>

```



Das **Theme** -Element ist das Stamm Element für Ihre Skin. In einer Skin-Definitionsdatei kann nur ein **Designelement vorhanden** sein, und es muss sich auf der obersten Ebene befinden. Design **Elemente verfügen** über bestimmte Attribute und Ambient-Attribute, die in den meisten Fällen aber nicht verwendet werden müssen. Weitere Informationen zu diesen Attributen finden Sie in der [Skin-Programmier Referenz](skin-programming-reference.md).

## <a name="view-elements"></a>Elemente anzeigen

Jedes **Design** muss mindestens ein **Ansichts** Element aufweisen. Das **Ansichts** Element steuert das jeweilige Bild, das auf dem Bildschirm angezeigt wird. Möglicherweise möchten Sie mehr als eine Ansicht haben, damit Sie hin-und herwechseln können. Angenommen, Sie möchten eine große Ansicht zum Arbeiten mit Wiedergabelisten, eine mittlere Ansicht zum Überwachen von Visualisierungen und eine kleine Ansicht, die in eine Ecke des Bildschirms passt.

Wenn Sie mehrere Ansichten erstellen, sollten Sie sicherstellen, dass jede Ansicht über einen eindeutigen **ID** -Attribut Wert verfügt, der zum Identifizieren der Sicht verwendet wird. Sie müssen das **BackgroundImage** -Attribut definieren, oder die Ansicht enthält kein Startbild. Wenn Sie kein rechteckiges Bild anzeigen möchten, verwenden Sie wahrscheinlich das **clippingcolor** -Attribut, um die Bereiche Ihrer Skin zu definieren, die nicht angezeigt werden, und Sie möchten wahrscheinlich das **TitleBar** -Attribut des **View** -Elements festlegen.

Jedes **Ansichts** Element kann auch über ein oder mehrere **untergeordnete** Elemente verfügen. Ein **unter Ansichts** Element ähnelt einer **Ansicht** und kann für Teile der Skin verwendet werden, die Sie bewegen, ausblenden oder anzeigen möchten. Beispielsweise kann ein **subview** -Element verwendet werden, um eine Schiebe Leiste zu erstellen, die aus ihrer Skin herausspringt, um einen Grafik-Equalizer anzuzeigen. **Subview** -Elemente können an der **Ansicht** ausgerichtet werden und andere besondere Beziehungen zur **Ansicht** aufweisen.

## <a name="initializing-windows-media-player"></a>Windows-Media Player werden initialisiert.

Sie können bestimmte anfängliche Eigenschaften von Windows Media Player mit den Elementen **Player**, **Settings** und **Controls** festlegen. Beispielsweise können Sie das Volume auf eine anfängliche Ebene festlegen oder einen Standardwert für einen Dateinamen festlegen.

Der folgende Code zeigt, wie der **URL** -Wert in einer Skin festgelegt wird:


```C++
<PLAYER
  URL = "https://proseware.com/mellow.wma">
</PLAYER>

```



Wenn Sie das **Autostart** -Attribut der **Einstellungen** auf false festlegen möchten, verwenden Sie den folgenden Code:


```C++
<PLAYER>
  <SETTINGS
    autoStart = "False">
  </SETTINGS>
</PLAYER>

```



Beachten Sie, dass das **Settings** -Element im **Player** -Element geschachtelt ist.

Mit diesen Elementen können die folgenden Attribute und Ereignisse zur Entwurfszeit angegeben werden:

**Player-Element Attribute**

-   **url**
-   **Pufferung**
-   **Ereignis Wechsel**
-   **Currentplaylistchange**
-   **Fehler**
-   **Markerhit**
-   **Mediachange**
-   **Mediacollectionchange**
-   **Modeänderung**
-   **Mpendstatechange**
-   **Mlaylistchange**
-   **Mlaystatechange**
-   **"Musitionchange"**
-   **Mcriptcommand**
-   **Mtatuschange**

**SETTINGS-Element Attribute**

-   **Autostart**
-   **Schwebe**
-   **Basis**
-   **defaultframe**
-   **enableerrordialogfelder**
-   **invokeurls**
-   **verstum**
-   **playcount**
-   **zinss**
-   **volume**

## <a name="controls-element-attributes"></a>Steuert Element Attribute

-   **currentmarker**
-   **CurrentPosition**

## <a name="other-user-interface-elements"></a>Andere Elemente der Benutzeroberfläche

Nachdem Sie das **Design und die** **Ansichts** Elemente definiert haben, müssen Sie die **Ansicht** mit bestimmten Benutzeroberflächen Elementen auffüllen. Sie müssen nicht alle verfügbaren Elemente in einer Skin verwenden, sondern nur die Elemente, die Sie benötigen.

Wenn ein Element vom Benutzer angezeigt werden kann, wird es als Steuerelement bezeichnet. Die folgenden Steuerelemente sind für Skins verfügbar:

-   Schaltflächen
-   Schieberegler, benutzerdefinierte Schieberegler und Status leisten
-   Textfelder
-   Video Fenster
-   Visualisierungs Fenster
-   Wiedergabelisten Fenster
-   Unter Ansichts Fenster

Darüber hinaus können mehrere-Elemente verwendet werden, um Windows-Media Player Aktionen weiter zu definieren, Sie erfordern jedoch visuelle Elemente wie Schaltflächen oder Schieberegler:

-   Video Einstellungen
-   Ausgleichs Einstellungen
-   Visualisierungs Einstellungen

## <a name="buttons"></a>Schaltflächen

Schaltflächen sind der beliebteste Teil eines Skin. Sie können Schaltflächen verwenden, um Aktionen wie z. b. abspielen, beenden, beenden, minimieren und wechseln zu einer anderen Ansicht zu initiieren. Windows Media Player stellt dem Skin-Ersteller zwei Arten von Schaltflächen Elementen bereit: das **Button** -Element und das **ButtonGroup** -Element. Außerdem gibt es mehrere vordefinierte Typen von Schaltflächen.

-   **Button-Element.** Das **Button** -Element wird für einzelne Schaltflächen verwendet. Wenn Sie das **Button** -Element verwenden, müssen Sie für jede Schaltfläche ein Bild angeben und die genaue Position definieren, an der die Schaltfläche relativ zum Hintergrundbild angezeigt werden soll. Einer der Vorteile des **Schalt** Flächen Elements besteht darin, dass Sie das Schaltflächen Bild dynamisch ändern können.
-   **ButtonGroup-Element.** Das **ButtonGroup** -Element wird für Gruppen von Schaltflächen verwendet. Tatsächlich müssen Sie jedes **ButtonGroup** -Element mit einem Paar **ButtonGroup** -Tags einschließen. Die Verwendung von Schaltflächen Gruppen ist einfacher als die Verwendung einzelner Schaltflächen, da Sie nicht den genauen Speicherort für die einzelnen Schaltflächen angeben müssen. Stattdessen geben Sie eine separate ImageMap an, mit der die Aktionen definiert werden, die durchgeführt werden, wenn der Mauszeiger auf einen Bereich im Hintergrund bewegt oder klickt. Die Verwendung von Image Maps ist einfach, da Sie die für den Hintergrund erstellte Grafik in eine Zuordnungs Ebene in Ihrem Grafikbearbeitungsprogramm kopieren können. Die Verwendung des Programms zur Grafikbearbeitung ist schneller und präziser, als zu versuchen, genau zu definieren, wo eine einzelne Schaltfläche auf dem Hintergrund platziert werden soll.
-   **Vordefinierte Schaltflächen.** Es gibt mehrere vordefinierte Schaltflächen. Beispielsweise können Sie eine playelement-Schaltfläche verwenden, um digitale Mediendateien wiederzugeben, und ein stopelement, um die Wiedergabe zu beenden. Weitere Informationen finden Sie unter Button [Group](buttongroup-element.md) -Element und [Button-Element](button-element.md) in der Skin-Programmier Referenz. Mithilfe von [ImageButton](imagebutton.md) können Bilder angezeigt werden, die sich in Reaktion auf bestimmte Ereignisse ändern können.

## <a name="sliders"></a>Schieberegler

Schieberegler sind nützlich für die Arbeit mit Informationen, die sich im Laufe der Zeit ändern. Beispielsweise können Sie einen Schieberegler verwenden, um die Menge der Musik anzugeben, die bereits für eine bestimmte Mediendatei wiedergegeben wurde. Schieberegler können horizontal oder vertikal, linear oder Zirkel oder eine beliebige Form sein, die Sie sich vorstellen können. Schieberegler sind in drei Varianten enthalten: Schieberegler, Status leisten und benutzerdefinierte Schieberegler.

-   **Rutscher.** Sie können das **Slider** -Element für volumensteuerelemente verwenden oder den Benutzer auf einen anderen Teil des Medien Inhalts verschieben.
-   **Status leisten.** Status anzeigen ähneln Schiebereglern. Status Indikatoren sind für die grafische Darstellung des Prozentsatzes eines bestimmten Prozesses konzipiert, der abgeschlossen wurde, jedoch nicht für einen Prozess, mit dem der Benutzer interagieren soll. Beispielsweise können Sie eine Statusanzeige verwenden, um den Puffer Status anzugeben.
-   **Benutzerdefinierte Schieberegler.** Es wird eine benutzerdefinierte Schieberegler-Funktionalität bereitgestellt, sodass Sie Steuerelemente wie z. b.-Knoten erstellen oder ungewöhnliche Steuerelement Mechanismen Wenn Sie z. b. ein Volume-Steuerelement erstellen möchten, das Ihre Skin umschließt, können Sie es mit einem benutzerdefinierten Schieberegler verwenden. Zum Einrichten des benutzerdefinierten Schiebereglers müssen Sie eine Imagemap erstellen, die Graustufenbilder enthält, um die Speicherorte der Werte auf dem Schieberegler zu definieren. Dies ist relativ einfach mit einem Grafikbearbeitungsprogramm, das Ebenen unterstützt.

## <a name="text"></a>Text

Sie können das **Text** -Element verwenden, um Text auf Ihrer Skin anzuzeigen, z. b. Titel Titel.

## <a name="video"></a>Video

Sie können Videos in der Skin anzeigen. Mit dem **Video** -Element können Sie die Größe und Position des Videofensters festlegen.

Sie können es dem Benutzer auch ermöglichen, die Videoeinstellungen mit dem **Video Settings** -Element zu ändern. Beispielsweise können Sie Steuerelemente erstellen, um die Helligkeit des Videos anzupassen.

Wenn Sie kein Video Element angeben und der Inhalt Video enthält, kehrt Windows Media Player in den vollständigen Modus zurück, und ihre Skin wird nicht angezeigt.

## <a name="equalizer-settings"></a>Ausgleichs Einstellungen

Sie können das Filtern für bestimmte audiohäufigkeits Bänder mit dem Element **equalizersettings** festlegen. Sie können den Bass steigern, das Treble optimieren und ihre Sounds so einrichten, dass Sie Ihren Ohren oder dem Wohnraum entsprechen.

## <a name="visualizations"></a>Visualisierungen

Visualisierungen können in der Skin angezeigt werden. Visualisierungen sind visuelle Effekte, die sich im Laufe der Zeit ändern, wenn Audiodaten über Windows Media Player abgespielt werden. Das **Effects** -Element bestimmt, wo die Visualisierungen abgespielt werden, welche Größe das Fenster darstellen wird und welche Visualisierungen wiedergegeben werden.

## <a name="playlists"></a>Wiedergabelisten

Sie können das **Wiedergabe** Listen-Element verwenden, um dem Benutzer zu ermöglichen, ein Element aus einer bestimmten Wiedergabeliste auszuwählen.

## <a name="subviews"></a>Unter Ansichten

Mit dem **subview** -Element können Sie sekundäre Sätze von Schnittstellen Steuerelementen anzeigen, z. b. eine Wiedergabeliste oder ein Video Steuerelement.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Skin-Dateien**](skin-files.md)
</dt> </dl>

 

 




