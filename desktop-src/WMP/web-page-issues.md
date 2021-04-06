---
title: Webseiten Probleme
description: Webseiten Probleme
ms.assetid: fd97540e-21e9-443e-99ec-ed29f4a2570a
keywords:
- Windows Media Metadatei-Wiedergabelisten, Webseiten
- Wiedergabelisten, Webseiten
- Metadatei-Wiedergabelisten, Webseiten
- Windows Media Metadatei-Wiedergabelisten, Anpassen von HtmlView
- Wiedergabelisten, Anpassen von HtmlView
- Metadatei-Wiedergabelisten, Anpassen von HtmlView
- Windows Media Metadatei-Wiedergabelisten, HtmlView-Anpassung
- Wiedergabelisten, HtmlView-Anpassung
- Metadatei-Wiedergabelisten, HtmlView-Anpassung
- Anpassen von HtmlView
- Windows Media Player, Webseiten
- Windows Media Player, Anpassen von HtmlView
- Windows Media Player, HtmlView-Anpassung
- HtmlView, anpassen
- HtmlView, Webseiten
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 882d8993ba3690cf8c4a068f9861ccf39cd1a95c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713403"
---
# <a name="web-page-issues"></a>Webseiten Probleme

Beim Erstellen einer Webseite, die in der Funktion "Windows-Media Player **jetzt spielen** " angezeigt wird, müssen Sie einige Punkte beachten. In diesem Abschnitt werden einige der Probleme erläutert, die beim Erstellen des webbasierten Inhalts auftreten können.

## <a name="customizing-htmlview"></a>Anpassen von HtmlView

Ihre HtmlView-Webseite kann so einfach oder komplex sein, wie Sie möchten. Sie können alle Elemente einschließen, die Sie normalerweise in Ihrem webbasierten Inhalt verwenden. Wenn Sie das Windows Media Player-Steuerelement einbetten, können Sie eine der vom Steuerelement bereitgestellten Benutzeroberflächen anzeigen, eine eigene Benutzeroberfläche mithilfe von HTML-und Skriptcode erstellen oder überhaupt keine Benutzeroberfläche bereitstellen (was bedeutet, dass der Benutzer die Transport Steuerelemente des Vollmodus-Players verwenden kann).

Die empfohlene Größe für Webseiten, die mithilfe der HtmlView-Funktion angezeigt werden, beträgt 575 x 345 Pixel. Der Benutzer hat jedoch die Möglichkeit, die Größe des Windows-Media Player zu ändern und die Bildschirmauflösung auszuwählen. Wenn die HtmlView-Webseite größer ist als die Größe, die von der Funktion " **jetzt** wiedergeben" untergebracht wird, zeigt der Player horizontale und vertikale Schiebe leisten an, mit denen der Benutzer die gesamte Seite anzeigen kann. Testen Sie den HtmlView-Inhalt mithilfe verschiedener Bildschirmauflösungen und Player Größen, um die beste Größe für Ihre Webseite zu ermitteln.

Windows Media Player bietet keine Methode, mit der Sie eine Größe für den vollmodusplayer angeben können.

## <a name="web-page-navigation"></a>Webseiten Navigation

Windows Media Player bietet keine Navigations Symbolleiste für Webseiten, die im Feature " **jetzt** wiedergeben" angezeigt werden. Dies bedeutet, dass Sie über die gesamte Kontrolle verfügen, ob Benutzer von ihrer HtmlView-Webseite Weg navigieren können. Wenn Sie es Benutzern ermöglichen möchten, zu anderen Webseiten zu navigieren, müssen Sie Elemente in Ihren HTML-Code einschließen, um diese Funktionalität bereitzustellen.

## <a name="retrieving-the-parent-window"></a>Abrufen des übergeordneten Fensters

Wenn Ihr vorhandener Skriptcode **Window. Parent** verwendet, um das übergeordnete Fenster Objekt abzurufen, funktioniert dieser Code auf der HtmlView-Webseite nicht. Wenn Sie HtmlView verwenden, ist kein übergeordnetes Fenster Objekt vorhanden. Diese Skriptfunktion ist daher nicht verfügbar.

## <a name="about-the-embedded-browser"></a>Informationen zum eingebetteten Browser

Da Windows Media Player eine eingebettete Instanz von Internet Explorer zum Anzeigen von HtmlView-Inhalten verwendet, gelten die Benutzereinstellungen und-Richtlinien für Internet Explorer für alle Webseiten, die im Player angezeigt werden. Wenn der Benutzer z. b. Internet Explorer so konfiguriert hat, dass Webseiten nicht auf den Computer heruntergeladen werden, wird die HtmlView-Webseite ebenfalls verhindert.

Webseiten, die mithilfe der HtmlView-Funktion geöffnet wurden, werden immer in Internet Explorer **Internet** Security Zone ausgeführt.

Im eingebetteten Webbrowser-Steuerelement werden die gleichen Regeln zum Zwischenspeichern von Webseiten als eigenständige Version von Internet Explorer verwendet. Beim Erstellen Ihrer Inhalte empfiehlt es sich, Active Server Pages (ASP) zu verwenden, um sicherzustellen, dass der Inhalt jedes Mal vom Webserver übermittelt wird, wenn Windows Media Player auf die HtmlView-Webseite zugreift. Die Verwendung von ASP-Seiten kann so einfach sein wie das Umbenennen der Webseite zur Verwendung der Dateinamenerweiterung ". asp".

## <a name="about-local-web-content"></a>Informationen zu lokalem Webinhalt

Mit der HtmlView-Funktion können Sie keine Webseiten öffnen, die auf dem Computer des Benutzers gespeichert sind.

## <a name="prompting-the-user"></a>Auffordern des Benutzers

Sie können " **Window. prompt** " verwenden, um den Benutzer zur Eingabe von Informationen aufzufordern. **Window. Alert** und **Window. Confirm** sind jedoch bei der Verwendung von HtmlView nicht verfügbar.

## <a name="timing-issues"></a>Zeit Steuerungsprobleme

Bei der Verwendung eines eingebetteten Windows Media Player-Steuer Elements auf der HtmlView-Webseite können Zeit Steuerungsprobleme auftreten. In HtmlView teilt ein eingebettetes Player-Steuerelement seine Wiedergabe-Engine mit dem eigenständigen Windows-Media Player. Es ist möglich, dass der eigenständige Player geöffnet wird und mit der Wiedergabe des ersten Wiedergabelisten Eintrags beginnt, bevor die Webseite (und damit das Player-Steuerelement) geladen wird. Dies bedeutet Folgendes: Wenn Sie die Ereignisse **OpenStateChange** oder **PlayStateChange** behandeln, empfängt der Skriptcode keine Ereignis Benachrichtigungen für diese Ereignisse, bis das Player-Steuerelement und die zugehörigen Objekte geladen sind.

Sie können Schritte im Code ausführen, um die Wiedergabe zu verzögern, bis das Windows Media Player-Steuerelement instanziiert wird. Eine Möglichkeit hierfür besteht darin, den ersten Eintrag in der Metadatei-Wiedergabeliste auf eine Bilddatei zu verweisen und die Dauer der Datei auf eine Zeitspanne festzulegen, die dem Player-Steuerelement das Laden ermöglicht. Der folgende Beispielcode veranschaulicht diese Option:


```XML
<ASX version="3.0">
   <PARAM name="HTMLView" value="https://www.proseware.com/htmlview1.htm"/>

<ENTRY>
   <REF href="https://www.proseware.com/blank.jpg"/>
   <DURATION  VALUE = "1:00"/>
</ENTRY>

<ENTRY>
   <REF href="rtsp://www.proseware.com/content1.wma"/>
</ENTRY>

</ASX>

```



Wenn die vorherige Wiedergabeliste geöffnet wird, wartet Windows Media Player auf den ersten Eintrag in der Wiedergabeliste bis zu einer Minute, während der Spieler die HtmlView-Webseite lädt.

Schreiben Sie als nächstes in der HtmlView-Webseite Skriptcode, um das **OnLoad** -Ereignis für das **Body** -Element zu verarbeiten. In der Ereignishandlerfunktion wird die Player **Controls. Next** -Methode aufgerufen, um die Wiedergabe des zweiten Eintrags in der Wiedergabeliste zu starten.


```XML
<HTML>
<!-- Define the event handler function. -->
<BODY  onload = "OnLoad();">

<OBJECT id = "Player" 
    CLASSID = "CLSID:6BF52A52-394A-11d3-B153-00C04F79FAA6"> 
        <PARAM Name = "autoStart"  Value = "true">
        <PARAM Name = "uiMode" Value = "none">

</OBJECT>

<!-- Handle the BODY onload event. -->
<SCRIPT>
function OnLoad()
{
   // Advance to the second entry in the playlist.
   Player.controls.next();
}
</SCRIPT>

</BODY>
</HTML>

```



Wenn die Webseite im vorherigen Beispiel den Lade Zeitpunkt abgeschlossen hat, wechselt Windows Media Player sofort zum zweiten Eintrag in der Wiedergabeliste. Dadurch wird die für das erste Element in der Wiedergabeliste angegebene Dauer überschrieben. Dies bedeutet, dass der Benutzer nicht vollständig eine Minute warten muss, bevor der gewünschte Inhalt angezeigt wird. Er muss nur warten, bis die Webseite geladen wurde. Da das Player-Steuerelement zu diesem Zeitpunkt vollständig instanziiert wird, können die Ereignisse **OpenStateChange** und **PlayStateChange** auf die übliche Weise behandelt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Anzeigen von Webseiten in Windows Media Player**](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[**Player. PlayStateChange-Ereignis**](player-player-playstatechange.md)
</dt> <dt>

[**Player. OpenStateChange-Ereignis**](player-player-openstatechange.md)
</dt> </dl>

 

 




