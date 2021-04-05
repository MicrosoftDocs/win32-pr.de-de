---
title: Sicherstellen, dass der Windows-Media Player den HtmlView-Inhalt öffnet
description: Sicherstellen, dass der Windows-Media Player den HtmlView-Inhalt öffnet
ms.assetid: 4ec4e027-4f9c-4a86-9f70-b4014971c070
keywords:
- Windows Media Metadatei-Wiedergabelisten, Windows Media Player öffnen von HtmlView-Inhalt
- Wiedergabelisten, Windows Media Player öffnen von HtmlView-Inhalt
- Metadatei-Wiedergabelisten, Windows Media Player öffnen von HtmlView-Inhalt
- Windows Media Metadatei-Wiedergabelisten, Öffnen von HtmlView-Inhalt
- Wiedergabelisten, Öffnen von HtmlView-Inhalt
- Metadatei-Wiedergabelisten, Öffnen von HtmlView-Inhalt
- Öffnen von HtmlView-Inhalt
- Windows Media Player, Öffnen von HtmlView-Inhalt
- Windows Media Player, HtmlView-Inhalt
- HtmlView, Öffnen von Inhalten
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3d3220be44fcc33b3657fb115b0bb57d07d1b928
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710974"
---
# <a name="ensuring-that-windows-media-player-opens-the-htmlview-content"></a>Sicherstellen, dass der Windows-Media Player den HtmlView-Inhalt öffnet

Derzeit sind Windows Media Player 9-Serie und Windows Media Player 10 die einzigen Player, die den *HtmlView* -Parameter in. ASX-Dateien unterstützen. Dies bedeutet, dass Sie Maßnahmen ergreifen sollten, um sicherzustellen, dass der HtmlView-Inhalt in diesen Versionen von Windows Media Player wiedergegeben wird.

Sie müssen zuerst feststellen, ob die Windows Media Player 9-Serie oder Windows Media Player 10 auf dem Computer des Benutzers installiert ist. Das Windows Media Player SDK enthält ein umfassendes Beispiel, das veranschaulicht, wie verschiedene Versionen von Windows-Media Player in verschiedenen Webbrowsern erkannt werden. Obwohl eine vollständige Analyse des Erkennungs Beispiels über den Rahmen dieses Abschnitts hinausgeht, gibt es einige grundlegende Schritte, die Sie durchführen können, um zu bestimmen, welche Version von Windows Media Player der Computer des Benutzers ausgeführt wird.

In der einfachsten Form ist das Erkennen von Windows Media Player das Einbetten des Player-Steuer Elements auf der Webseite, das mit Ihrem HtmlView-Inhalt verknüpft ist, und die anschließende Überprüfung des vom *Player* abgerufenen Werts. **VERSIONINFO** -Eigenschaft. Nachdem Sie sich vergewissert haben, dass der Benutzer Windows Media Player 9-oder Windows Media Player 10 installiert hat, können Sie die [Player. openplayer](player-openplayer.md) -Methode verwenden, um den Inhalt im Vollmodus-Player zu öffnen. Die **openplayer** -Methode stellt sicher, dass Ihre Inhalte anfänglich in der Funktion " **jetzt** wiedergeben" des vollmodusplayers angezeigt werden, nicht in einer Skin, im Mini Player Modus oder in einem anderen Player, der sich selbst als Standardprogramm für Dateien mit der Dateinamenerweiterung ". asx" registriert hat, aber HtmlView nicht unterstützt. Sobald der Inhalt angezeigt wird, verfügt der Benutzer jedoch über die komplette Kontrolle über Windows Media Player, was bedeutet, dass er eine andere Funktion als **jetzt spielen**, in den Skin-Modus wechseln oder sogar den Player beenden kann.

Im folgenden Beispielcode wird eine Webseite für Internet Explorer erstellt. Auf dieser Seite wird eine. ASX-Datei geöffnet, die eine HtmlView-Webseite angibt, die im vollmodusplayer angezeigt wird, wenn Windows Media Player 9 oder höher installiert ist.


```XML
<HTML>
<BODY>

<!-- This code embeds the Player object in invisible mode. -->
<OBJECT id = "Player" 
    CLASSID = "CLSID:6BF52A52-394A-11d3-B153-00C04F79FAA6" height = 0 width = 0> 
        <PARAM Name = "AutoStart"  Value = "True">
        <PARAM Name = "uiMode" Value = "invisible">
</OBJECT>

<!-- Create a button to open the content. -->
<INPUT Type = "Button"  ID = "btnPlay"  Value = "Play ASX"  onClick = "PlayASX();"/>

<SCRIPT Language = "JScript">

// This function tests the Player version. If it is Windows Media 
// Player 9 Series or later, the script opens the .asx file in the full-mode 
// Player. Otherwise, the script makes the embedded control visible to 
// the user and opens the .asx file in the webpage. 

function PlayASX()
{
    if(parseInt(Player.versionInfo) >= 9)
        {
            // Open the full-mode Player to show HTMLView.
            Player.openPlayer("https://www.proseware.com/MyHTMLView.asx");
        }
        else
        {
            // Open the .asx file in the embedded Player.
            Player.uiMode = "full";
            Player.height = 200;
            Player.width = 200;
            Player.URL = "https://www.proseware.com/MyHTMLView.asx";
        }
}
</SCRIPT>

</BODY>
</HTML>

```



Der Code im vorherigen Beispiel bettet das Windows Media Player-Steuerelement ein, bei dem die **uiMode** -Eigenschaft auf "unsichtbar" festgelegt ist und die Attribute height und Width auf NULL festgelegt sind. Der Grund hierfür ist, dass die Benutzeroberfläche des Player-Steuer Elements von der Webseite anfänglich nicht angezeigt werden muss – Sie benötigt lediglich Zugriff auf das Player-Objektmodell. Die Seite zeigt auch eine Eingabe Schaltfläche an, mit der der Benutzer die. ASX-Datei wiedergeben kann.

Wenn der Benutzer auf die Schaltfläche "wiedergeben" klickt, wird die Microsoft JScript-Funktion playasx ausgeführt. Diese Funktion ruft zuerst den Wert für die Eigenschaft "Player **VERSIONINFO** " ab und verwendet dabei die Methode "JScript **Paramet** ", um den numerischen Wert der abgerufenen Zeichenfolge zu überprüfen. Wenn der numerische Wert größer oder gleich 9 ist (d. h., dass der Benutzer Windows Media Player 9-Reihe installiert hat), ruft der Skriptcode die **openplayer** -Methode auf und übergibt dabei die URL der. ASX-Datei, die den HtmlView-Parameter enthält. Diese Methode öffnet die. ASX-Datei mithilfe von Windows Media Player im vollständigen Modus, gibt den digitalen Medieninhalt in der. ASX-Wiedergabeliste wieder und zeigt den webbasierten HtmlView-Inhalt im Feature " **jetzt** wiedergeben" an.

Wenn der numerische Wert der Versions Zeichenfolge nicht größer oder gleich 9 ist (d. h., dass der Benutzer nicht über eine Windows Media Player 9-Serie oder höher auf seinem Computer installiert ist), der Skriptcode ändert den **uiMode** -Wert des Player-Steuer Elements in "Full", legt eine neue Breite und Höhe für das Steuerelement fest und öffnet dann die. ASX-Datei im eingebetteten Player, indem ein Wert für die **URL** -Eigenschaft angegeben wird. In diesem Fall wird der Inhalt digitaler Medien auf der Webseite abgespielt, aber alle in der. ASX-Datei angegebenen HtmlView-Werte werden ignoriert.

Die Art und Weise, wie Inhalte wiedergegeben werden, wenn der Benutzer keine Windows Media Player 9-Serie oder Windows Media Player 10 installiert hat. Im vorangehenden Beispiel wird gezeigt, wie angegeben wird, dass der Inhalt auf der Webseite statt im vollmodusplayer abgespielt wird, wobei jeder HtmlView-Inhalt im Prozess ignoriert wird. Es gibt noch andere Ansätze, die Sie ergreifen können. Beispielsweise können Sie den Benutzer auffordern, eine neuere Version von Windows Media Player zu installieren, sodass diese Version des Players für die Wiedergabe digitaler Medieninhalte erforderlich ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Anzeigen von Webseiten in Windows Media Player**](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[**Player. uiMode**](player-uimode.md)
</dt> <dt>

[**Player. URL**](player-url.md)
</dt> </dl>

 

 




