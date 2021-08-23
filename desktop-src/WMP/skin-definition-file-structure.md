---
title: Struktur der Skindefinitionsdatei
description: Struktur der Skindefinitionsdatei
ms.assetid: 6b9ea288-ec64-473b-b796-ab637517099a
keywords:
- Windows Media Player Skins, Skindefinitionsdateien
- Skins, Skindefinitionsdateien
- Dateien für Skins, Skindefinition
- Skindefinitionsdateien,Struktur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c708e46f93e2d00820015a04b0f467da2deafe59e4dbafb0b9e4f3fb8660271
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995280"
---
# <a name="skin-definition-file-structure"></a>Struktur der Skindefinitionsdatei

Die Skindefinitionsdatei muss einer bestimmten Struktur folgen. Sie beginnen  mit einem THEME-Element, erstellen ein oder mehrere VIEW-Elemente und definieren dann jedes **VIEW-Element** mit den Benutzeroberflächenelementen, die für den Zu verwendenden Ansichtstyp geeignet sind. 

## <a name="theme-elements"></a>THEME-Elemente

Auf der obersten Ebene müssen Sie die Skindefinitionsdatei mit dem **THEME-Element starten** und damit schließen.


```C++
<THEME>
    ...
</THEME>

```



Das **THEME-Element** ist das Stammelement für Ihre Skin. Es kann nur ein **THEME-Element** in einer Skindefinitionsdatei geben, und es muss sich auf der obersten Ebene befingen. **THEME-Elemente** verfügen über spezifische und Umgebungsattribute, obwohl Sie sie in den meisten Jahren nicht verwenden müssen. Weitere Informationen zu diesen Attributen finden Sie in der [Referenz zur Skinprogrammierung.](skin-programming-reference.md)

## <a name="view-elements"></a>VIEW-Elemente

Jedes **THEME** muss mindestens ein **VIEW-Element** haben. Das **VIEW-Element** steuert das bestimmte Bild, das auf dem Bildschirm angezeigt wird. Möglicherweise möchten Sie mehr als eine Ansicht haben, damit Sie hin- und herwechseln können. Sie möchten z. B. eine große Ansicht für die Arbeit mit Wiedergabelisten, eine mittlere Ansicht zum Ansehen von Visualisierungen und eine kleine Ansicht, die in eine Ecke des Bildschirms passt.

Wenn Sie mehrere Ansichten erstellen, sollten Sie sicherstellen, dass  jede Ansicht über einen eindeutigen ID-Attributwert verfügt, der zum Identifizieren der Ansicht verwendet wird. Sie müssen das **backgroundImage-Attribut** definieren, da ihre Ansicht kein Startbild hat. Wenn Sie kein rechteckiges Bild anzeigen möchten, sollten Sie das **clippingColor-Attribut** verwenden, um die Bereiche Ihrer Skin zu definieren, die nicht angezeigt werden, und Sie möchten wahrscheinlich das **titleBar-Attribut** des **VIEW-Elements** festlegen.

Jedes **VIEW-Element** kann auch ein oder mehrere **SUBVIEW-Elemente** enthalten. Ein **SUBVIEW-Element** ähnelt **einem VIEW-Element** und kann für Teile Ihrer Skin verwendet werden, die Sie bewegen, ausblenden oder anzeigen möchten. Ein **SUBVIEW-Element** kann z. B. verwendet werden, um eine gleitende Taskleiste zu erstellen, die aus der Skin lädt, um einen grafischen Equalizer anzuzeigen. **SUBVIEW-Elemente** können an view ausgerichtet **werden** und haben andere besondere Beziehungen zur **VIEW.**

## <a name="initializing-windows-media-player"></a>Initialisieren Windows Media Player

Sie können bestimmte Anfangseigenschaften von Windows Media Player **player-,** **SETTINGS- und** **CONTROLS-Elementen** festlegen. Beispielsweise können Sie das Volume auf eine anfängliche Ebene festlegen oder einen Standardwert für einen Dateinamen angeben.

Der folgende Code zeigt, wie der **URL-Wert** in einer Skin festgelegt wird:


```C++
<PLAYER
  URL = "https://proseware.com/mellow.wma">
</PLAYER>

```



Wenn Sie das **autoStart-Attribut von** SETTINGS auf **False** festlegen möchten, verwenden Sie den folgenden Code:


```C++
<PLAYER>
  <SETTINGS
    autoStart = "False">
  </SETTINGS>
</PLAYER>

```



Beachten Sie, **dass das SETTINGS-Element** im **PLAYER-Element geschachtelt** ist.

Mithilfe dieser Elemente können zur Entwurfszeit die folgenden Attribute und Ereignisse angegeben werden:

**PLAYER-Elementattribute**

-   **url**
-   **Pufferung**
-   **Currentitemchange**
-   **Currentplaylistchange**
-   **Fehler**
-   **Markerhit**
-   **Mediachange**
-   **Mediacollectionchange**
-   **Modechange**
-   **Mpenstatechange**
-   **Mlaylistchange**
-   **Mlaystatechange**
-   **Mositionchange**
-   **Mcriptcommand**
-   **Mtatuschange**

**SETTINGS-Elementattribute**

-   **autoStart**
-   **Gleichgewicht**
-   **baseURL**
-   **defaultFrame**
-   **enableErrorDialogs**
-   **invokeURLs**
-   **Stumm**
-   **playCount**
-   **Rate**
-   **volume**

## <a name="controls-element-attributes"></a>CONTROLS-Elementattribute

-   **currentMarker**
-   **currentPosition**

## <a name="other-user-interface-elements"></a>Andere Benutzeroberfläche-Elemente

Nachdem Sie ihre **THEME-** und **VIEW-Elemente** definiert haben, müssen Sie **view** mit bestimmten Benutzeroberflächenelementen auffüllen. Sie müssen nicht alle verfügbaren Elemente in einer Skin verwenden, sondern nur die elemente, die Sie benötigen.

Wenn ein Element für den Benutzer angezeigt werden kann, wird es als Steuerelement bezeichnet. Die folgenden Steuerelemente sind für Skins verfügbar:

-   Schaltflächen
-   Schieberegler, benutzerdefinierte Schieberegler und Statusleisten
-   Textfelder
-   Videofenster
-   Visualisierungsfenster
-   Wiedergabelistenfenster
-   Unteransichtsfenster

Darüber hinaus können mehrere Elemente verwendet werden, um Windows Media Player zu definieren, aber sie erfordern visuelle Elemente wie Schaltflächen oder Schieberegler:

-   Videoeinstellungen
-   Equalizer-Einstellungen
-   Visualisierungseinstellungen

## <a name="buttons"></a>Schaltflächen

Schaltflächen sind der beliebtesten Teil einer Skin. Sie können Schaltflächen verwenden, um Aktionen wie Wiedergabe, Beenden, Beenden, Minimieren und Wechseln zu einer anderen Ansicht auszulösen. Windows Media Player bietet dem Skin-Ersteller zwei Arten von Schaltflächenelementen: das **BUTTON-Element** und das **BUTTONGROUP-Element.** Darüber hinaus gibt es mehrere vordefinierte Typen von Schaltflächen.

-   **BUTTON-Element.** Das **BUTTON-Element** wird für einzelne Schaltflächen verwendet. Wenn Sie das **BUTTON-Element** verwenden, müssen Sie für jede Schaltfläche ein Bild festlegen und die genaue Position definieren, an der die Schaltfläche relativ zum Hintergrundbild angezeigt werden soll. Einer der Vorteile des **BUTTON-Elements** ist, dass Sie das Schaltflächenbild dynamisch ändern können.
-   **BUTTONGROUP-Element.** Das **BUTTONGROUP-Element** wird für Gruppen von Schaltflächen verwendet. Tatsächlich müssen Sie jedes **BUTTONGROUP-Element** mit einem Paar von **BUTTONGROUP-Tags** umschließen. Die Verwendung von Schaltflächengruppen ist einfacher als die Verwendung einzelner Schaltflächen, da Sie nicht die genaue Position für jede Schaltfläche angeben müssen. Stattdessen geben Sie eine separate Bildkarte an, die die Aktionen definiert, die ausgeführt werden, wenn der Mauszeiger auf einen Bereich im Hintergrund zeigt oder darauf klickt. Die Verwendung von Bildzuordnungen ist einfach, da Sie die für Ihren Hintergrund erstellte Grafik auf eine Zuordnungsebene in Ihrem Grafikbearbeitungsprogramm kopieren können. Die Verwendung des Grafikbearbeitungsprogramms ist schneller und präziser als der Versuch, genau zu definieren, wo eine einzelne Schaltfläche im Hintergrund platziert werden soll.
-   **Vordefinierte Schaltflächen.** Es gibt mehrere vordefinierte Schaltflächen. Beispielsweise können Sie eine PLAYELEMENT-Schaltfläche verwenden, um digitale Mediendateien wiedergeben, und ein STOPELEMENT, um die Wiedergabe zu beenden. Weitere [Informationen finden Sie unter BUTTONGROUP-Element](buttongroup-element.md) und [BUTTON-Element](button-element.md) in der Referenz zur Skinprogrammierung. [IMAGEBUTTON kann](imagebutton.md) verwendet werden, um Bilder anzuzeigen, die sich als Reaktion auf bestimmte Ereignisse ändern können.

## <a name="sliders"></a>Schieberegler

Schieberegler sind nützlich für die Arbeit mit Informationen, die sich im Laufe der Zeit ändern. Beispielsweise können Sie einen Schieberegler verwenden, um die Menge an Musik anzugeben, die bereits für eine bestimmte Mediendatei abgespielt wurde. Schieberegler können horizontal oder vertikal, linear oder kreisförmige Schieberegler oder eine beliebige Form sein, an die Sie sich denken können. Schieberegler gibt es in drei Varianten: Schieberegler, Statusleisten und benutzerdefinierte Schieberegler.

-   **Schieberegler.** Sie können das **SLIDER-Element** für Volumesteuerelemente verwenden oder dem Benutzer ermöglichen, zu einem anderen Teil des Medieninhalts zu wechseln.
-   **Statusleisten.** Statusleisten ähneln Schiebereglern. Statusanzeigen sind für die grafische Anzeige des Prozentsatzes eines bestimmten Prozesses, der abgeschlossen wurde, konzipiert, jedoch nicht für einen Prozess, mit dem der Benutzer interagieren möchte. Beispielsweise können Sie eine Statusleiste verwenden, um den Pufferungsfortschritt anzugeben.
-   **Benutzerdefinierte Schieberegler.** Benutzerdefinierte Schiebereglerfunktionen werden bereitgestellt, damit Sie Steuerelemente wie Regler erstellen oder ungewöhnliche Steuerungsmechanismen erstellen können. Wenn Sie z. B. ein Volumesteuer steuerelement erstellen möchten, das Ihre Skin umhingt, können Sie dies mit einem benutzerdefinierten Schieberegler tun. Zum Einrichten des benutzerdefinierten Schiebereglers müssen Sie eine Bildkarte erstellen, die Graustufenbilder enthält, um die Positionen der Werte auf dem Schieberegler zu definieren. Dies ist relativ einfach mit einem Grafikbearbeitungsprogramm zu tun, das Ebenen unterstützt.

## <a name="text"></a>Text

Sie können das **TEXT-Element verwenden,** um Text auf Ihrer Skin anzuzeigen, z. B. Titel von Musiktiteln.

## <a name="video"></a>Video

Sie können Videos in Ihrer Skin anzeigen. Mit **dem VIDEO-Element** können Sie die Größe und Position des Videofensters festlegen.

Sie können dem Benutzer auch erlauben, die Videoeinstellungen mit dem **VIDEOSETTINGS-Element zu** ändern. Beispielsweise können Sie Steuerelemente erstellen, um die Helligkeit des Videos anzupassen.

Wenn Sie kein Videoelement geben und der Inhalt Video enthält, wird Windows Media Player in den Vollmodus zurück, und Ihre Skin wird nicht angezeigt.

## <a name="equalizer-settings"></a>Equalizer-Einstellungen

Sie können die Filterung für bestimmte Audiofrequenzbänder mithilfe des **EQUALIZERSETTINGS-Elements** festlegen. Sie können die Töne ankurbeln, den Treble optimieren und Ihre Sounds so einrichten, dass sie Ihren Tönen oder Ihrem Zimmer passen.

## <a name="visualizations"></a>Visualisierungen

Sie können Visualisierungen in Ihrer Skin anzeigen. Visualisierungen sind visuelle Effekte, die sich im Laufe der Zeit ändern, wenn Audiodaten über Windows Media Player. Das **EFFECTS-Element** bestimmt, wo die Visualisierungen abgespielt werden, welche Fenstergröße und welche Visualisierungen abgespielt werden.

## <a name="playlists"></a>Wiedergabelisten

Sie können das **PLAYLIST-Element verwenden,** damit der Benutzer ein Element aus einer bestimmten Wiedergabeliste auswählen kann.

## <a name="subviews"></a>Unteransichten

Sie können das **SUBVIEW-Element verwenden,** um sekundäre Sätze von Schnittstellensteuerelementen anzuzeigen, z. B. wiedergabelisten- oder videosteuerelemente.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Skindateien**](skin-files.md)
</dt> </dl>

 

 




