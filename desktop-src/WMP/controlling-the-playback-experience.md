---
title: Steuern des Wiedergabe Erlebnisses
description: Steuern des Wiedergabe Erlebnisses
ms.assetid: f130eee1-10ef-4cbe-b6ac-8ad24e1f0f34
keywords:
- Windows Media Metadatei-Wiedergabelisten, Steuern der Wiedergabe
- Wiedergabelisten, Steuern der Wiedergabe
- Metadatei-Wiedergabelisten, Steuern der Wiedergabe
- Windows Media Metadatei-Wiedergabelisten, Wiedergabe Probleme
- Wiedergabelisten, Wiedergabe Probleme
- Metadatei-Wiedergabelisten, Wiedergabe Probleme
- Steuern der Wiedergabe
- Windows Media Player, Steuern der Wiedergabe
- Windows Media Player, Wiedergabe Probleme
- HtmlView, Wiedergabe Probleme
- HtmlView, Steuern der Wiedergabe
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6877b869be8ca38ef9266aedf9318103d0e547ca
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340633"
---
# <a name="controlling-the-playback-experience"></a>Steuern des Wiedergabe Erlebnisses

In diesem Abschnitt werden einige der Wiedergabe Probleme erläutert, die beim Verwenden der HtmlView-Funktion auftreten können.

## <a name="requiring-the-user-to-view-web-based-content"></a>Der Benutzer muss webbasierten Inhalt anzeigen.

Sie können sich entscheiden, dass Benutzer nur in der Lage sein sollen, Ihre digitalen Medieninhalte zu nutzen, wenn der webbasierte HtmlView-Inhalt ebenfalls angezeigt wird. Sie können Skriptcode in Ihre HtmlView-Webseite einschließen, der die Wiedergabe des digitalen Medien Inhalts beendet, wenn der Benutzer von der Funktion " **jetzt** Wiedergabe" entfernt wird. Zu diesem Zweck können Sie einen Ereignishandler für das **Entlade** Ereignis als Teil des **Body** -Elements angeben, wie der folgende HTML-Code veranschaulicht:


```XML
<BODY onunload = "UnloadMe();">

```



Anschließend können Sie Skriptcode in die Ereignishandlerfunktion einschließen, um die Datei im Player zu schließen. Der folgende Beispielcode bewirkt Folgendes:


```XML
function UnloadMe()
{
   Player.close();
}

```



Wenn der Benutzer **nun** durch Klicken auf eine Schaltfläche zum Öffnen einer anderen Windows Media Player-Funktion wechselt, z. b. der Bibliothek, schließt der Spieler den eingebetteten Browser. Dies bewirkt, dass das **onentlade** -Ereignis stattfindet, wobei das Skript in der Funktion mit dem Namen **unloadme** ausgeführt wird. Die [Player. Close](player-close.md) -Methode beendet die Wiedergabe und entlädt die aktuelle digitale Mediendatei. Um den Inhalt erneut anzuzeigen, muss der Benutzer die ursprüngliche. ASX-Datei erneut öffnen. Diese Technik hält auch die Wiedergabe an, wenn der Benutzer von der HtmlView-Webseite weg navigiert. Beachten Sie, dass diese Technik nicht verhindern kann, dass der Benutzer den Inhalt digitaler Medien anzeigen kann, wenn er zum Skin-Modus wechselt.

Sie erinnern sich, dass der HtmlView-Parameter auf jedes **Entry** -Element in einer. ASX-Datei angewendet werden kann. Sie können diese Funktion nutzen, um sicherzustellen, dass Ihr HtmlView-Inhalt jedes Mal angezeigt wird, wenn eine neue digitale Mediendatei gestartet wird. Ordnen Sie zu diesem Zweck jedem Eintrag in Ihrer. ASX-Wiedergabeliste ein **param** -Element für HtmlView zu. Wenn jeder Eintrag abgespielt wird, wechselt der Spieler in den vollständigen Modus und zeigt den HtmlView-Inhalt an, den Sie in der Wiedergabeliste angegeben haben.

## <a name="url-and-file-script-command-types-are-disabled-by-default"></a>URL-und Datei Skript-Befehls Typen sind standardmäßig deaktiviert.

Windows Media Player 9 oder höher stellt Einstellungen bereit, die es dem Benutzer ermöglichen, anzugeben, ob URL-und Dateityp-Skript Befehle ausgeführt werden können. Beide Skript Befehls Typen werden standardmäßig nicht ausgeführt. Wenn Sie benutzerdefinierte Skript Befehls Typen verwenden, werden Sie unabhängig von der Benutzereinstellung weiterhin ausgeführt. Wenn Sie URL-und Dateityp Skript Befehle verwenden müssen, müssen Sie den Benutzer auffordern, die Einstellungen zu ändern. Um die Einstellungen zu ändern, **Klicken Sie auf Extras**, dann auf **Optionen** und dann auf **Sicherheit**.

## <a name="reopening-an-htmlview-does-not-reload-the-webpage"></a>Beim erneuten Öffnen einer HtmlView wird die Webseite nicht neu geladen.

Wenn der Benutzer eine. ASX-Datei öffnet, die einen HtmlView-Parameter enthält, und dann dieselbe Datei erneut öffnet, aktualisiert Windows Media Player die HtmlView-Webseite nicht. Dies bedeutet auch, dass der Player den eingebetteten Browser nicht an die anfängliche HtmlView-Webseite zurückgibt, wenn Sie Benutzern ermöglicht haben, von ihrer HtmlView-Webseite zu navigieren.

## <a name="hiding-the-content-location"></a>Ausblenden des Inhalts Speicher Orts

Möglicherweise möchten Sie, dass Windows Media Player den Speicherort der digitalen Medieninhalte nicht anzeigt, während eine. ASX-Datei wiedergegeben wird. Normalerweise zeigt Windows Media Player nur Informationen über die Wiedergabeliste selbst an, wenn Inhalte aus dem Internet gestreamt werden. Es gibt jedoch weitere Schritte, die Sie durchführen können, um zu verhindern, dass Benutzer den Speicherort der Inhalte ermitteln. Eine Möglichkeit, um sicherzustellen, dass der Player den Pfad zu ihren Inhalten nicht anzeigt, besteht beispielsweise darin, ihre Inhalte mithilfe von Windows Media Services serverseitigen Wiedergabelisten zu streamen. Auf diese Weise wird, wenn der Benutzer die Eigenschaften für den Inhalt anzeigt, die URL des Servers und nicht die URL Ihres Inhalts angezeigt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Anzeigen von Webseiten in Windows Media Player**](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[**Param-Element**](param-element.md)
</dt> </dl>

 

 




