---
title: Hinzufügen eines eingebetteten Windows Media Player-Steuer Elements
description: Hinzufügen eines eingebetteten Windows Media Player-Steuer Elements
ms.assetid: e002bf2a-c51a-448a-80a0-a35d6f32e9c0
keywords:
- Windows Media Metadatei-Wiedergabelisten, Hinzufügen von eingebetteten Fenstern Media Player Steuerelementen
- Wiedergabelisten, Hinzufügen von eingebetteten Windows Media Player-Steuerelementen
- Metadatei-Wiedergabelisten, Hinzufügen von eingebetteten Fenstern Media Player Steuerelementen
- Windows Media Metadatei-Wiedergabelisten, eingebettete Windows Media Player-Steuerelemente
- Wiedergabelisten, eingebettete Windows Media Player-Steuerelemente
- Metadatei-Wiedergabelisten, eingebettete Fenster Media Player
- Hinzufügen von eingebetteten Fenstern Media Player Steuerelementen
- eingebettete Windows Media Player-Steuerelemente
- Windows Media Player, Hinzufügen von eingebetteten Steuerelementen
- Windows Media Player, eingebettete Steuerelemente
- HtmlView, Hinzufügen von eingebetteten Windows-Media Player Steuerelementen
- HtmlView, eingebettete Windows Media Player-Steuerelemente
- HtmlView, Windows Media Player-Objektmodell
- HtmlView, Player-Objektmodell
- Windows Media Player-Objektmodell, Informationen zu
- Objektmodell, Informationen
- Player-Objekt
- Windows Media, Player-Objektmodell
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1dea3b11f59bff2edbcef99f1acda5fd0cfcff46
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388511"
---
# <a name="adding-an-embedded-windows-media-player-control"></a>Hinzufügen eines eingebetteten Windows Media Player-Steuer Elements

Es gibt zwei Gründe, warum Sie in Erwägung gezogen werden, eine eingebettete Instanz von Windows Media Player ihrer HtmlView-Präsentation hinzuzufügen. Wenn Sie Videoinhalte anzeigen möchten, müssen Sie zunächst das Windows Media Player ActiveX-Steuerelement verwenden. Zweitens: Wenn Sie die Funktionen des Windows Media Player-Objektmodells von der HtmlView-Webseite aus nutzen möchten, müssen Sie hierfür eine Instanz des Player-Steuer Elements verwenden.

## <a name="using-the-player-control-to-display-video-in-htmlview-content"></a>Verwenden des Player-Steuer Elements zum Anzeigen von Videos im HtmlView-Inhalt

In der Regel zeigt Windows Media Player Video mit dem Bereich Video und Visualisierung der Funktion **jetzt Wiedergabe** an. Da HtmlView diesen Bereich verwendet, um Ihre Webseite anzuzeigen, müssen Sie einen zusätzlichen Videoanzeige Bereich angeben, wenn der Player Video abspielen soll. Dies ist einfach, wenn Sie das Windows Media Player ActiveX-Steuerelement verwenden.

Um das Player-Steuerelement zum Anzeigen von Videos zu verwenden, Betten Sie das Steuerelement mithilfe des **Objekttags** in die HtmlView-Webseite ein. Dabei handelt es sich um dasselbe Verfahren, das Sie verwenden, um das Player-Steuerelement in eine beliebige Webseite einzubetten, auf der Sie Videos anzeigen möchten. Der folgende Beispielcode zeigt die grundlegende Syntax zum Einbetten des Player-Steuer Elements in Internet Explorer:


```XML
<OBJECT id = "Player" 
    CLASSID = "CLSID:6BF52A52-394A-11d3-B153-00C04F79FAA6"> 
        <PARAM Name = "autoStart"  Value = "true">
        <PARAM Name = "uiMode" Value = "none">
</OBJECT>

```



Der *Autostart* -Parameter stellt sicher, dass der Inhalt automatisch wiedergegeben wird, wenn eine neue URL angegeben wird. Der Wert, den Sie für *uiMode* angeben, ist für Sie festgelegt, aber Sie möchten bei der Erstellung von Inhalten für HtmlView-Präsentationen normalerweise "None" angeben. Wenn Sie das Windows Media Player-Steuerelement einbetten, um Videos auf diese Weise anzuzeigen, kann der Benutzer die Wiedergabe mit den Steuerelementen des vollmodusplayers steuern, sodass keine zusätzlichen Transport Steuerelemente auf der Webseite bereitgestellt werden müssen. Sie können den Speicherplatz, den Sie normalerweise für Transport Steuerelemente zuweisen würden, verwenden, um mehr Text, Grafiken oder Links zu anderen Inhalten anzuzeigen.

Geben Sie keinen *URL* -Parameter an, wenn Sie das Windows Media Player-Steuerelement in eine Webseite einbetten, die in einer HtmlView-Präsentation angezeigt werden soll. Geben Sie stattdessen die digitalen Mediendateien in der. ASX-Datei an, die den Inhalt öffnet.

Da Sie den Videoanzeige Bereich auf der HtmlView-Webseite bereitstellen, können Sie entscheiden, wo das Video positioniert werden soll und wie groß der Anzeigebereich sein soll. Beispielsweise können Sie das **Player** -Objekt in einem HTML **div** -Element enthalten und dann die Position für das **div** -Element angeben, um die Videoanzeige auf der Webseite zu positionieren. Sie können die Dimensionen der Videoanzeige ändern, indem Sie Werte für die Attribute height und Width des **Object** -Elements angeben. Sie können diese Werte auch mithilfe von Skriptcode angeben.

## <a name="using-the-player-object-model"></a>Verwenden des Player-Objektmodells

Das Windows Media Player-Objektmodell macht Eigenschaften, Methoden und Ereignisse verfügbar, die Sie in ihren HtmlView-Webseiten verwenden können. Wenn Sie das Windows Media Player ActiveX-Steuerelement in die HtmlView-Webseite einbetten, haben Sie automatisch Zugriff auf das Player-Objektmodell.

Wenn Sie das Windows Media Player-Steuerelement in die HtmlView-Webseite einbetten, verwenden Sie das Player-Objektmodell nicht, um die zu Wiedergabe Ende digitale Mediendatei anzugeben. Wenn Sie z. b. Skriptcode verwenden, um einen Wert für die **URL** -Eigenschaft des eingebetteten Steuer Elements anzugeben, wird die HtmlView-Webseite aus der Funktion " **jetzt** wiedergeben" entladen, wenn die digitale Mediendatei wiedergegeben wird. Um dies zu verhindern, öffnen Sie immer die. ASX-Dateien, die HtmlView-Parameter enthalten, wenn Sie das Skript verwenden müssen, um Inhalte digitaler Medien von ihrer HtmlView-Webseite zu öffnen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Anzeigen von Webseiten in Windows Media Player**](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[**Player. uiMode**](player-uimode.md)
</dt> <dt>

[**Player. URL**](player-url.md)
</dt> <dt>

[**Einstellungen. Autostart**](settings-autostart.md)
</dt> </dl>

 

 




