---
title: Steuern der Wiedergabeerfahrung
description: Steuern der Wiedergabeerfahrung
ms.assetid: f130eee1-10ef-4cbe-b6ac-8ad24e1f0f34
keywords:
- Windows Medienmetadatei-Wiedergabelisten, Steuern der Wiedergabe
- Wiedergabelisten, Steuern der Wiedergabe
- Metafile-Wiedergabelisten,Steuern der Wiedergabe
- Windows Wiedergabelisten für Medienmetadateien, Wiedergabeprobleme
- Wiedergabelisten, Wiedergabeprobleme
- Metafile-Wiedergabelisten, Wiedergabeprobleme
- Steuern der Wiedergabe
- Windows Media Player,Steuern der Wiedergabe
- Windows Media Player, Wiedergabeprobleme
- HTMLView, Wiedergabeprobleme
- HTMLView,Steuern der Wiedergabe
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: efca4d299edc40cfb94820fbb1aae7115329c0f3fcbd2859db0bbbc56d7a0d4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118341887"
---
# <a name="controlling-the-playback-experience"></a>Steuern der Wiedergabeerfahrung

In diesem Abschnitt werden einige der Wiedergabeprobleme erläutert, die bei verwendung des HTMLView-Features auftreten können.

## <a name="requiring-the-user-to-view-web-based-content"></a>Benutzer müssen webbasierte Inhalte anzeigen

Möglicherweise möchten Sie, dass Benutzer Ihre digitalen Medieninhalte nur nutzen können, wenn auch die webbasierten HTMLView-Inhalte angezeigt werden. Sie können Skriptcode in Ihre HTMLView-Webseite einschließen, die die Wiedergabe der digitalen Medieninhalte beendet, wenn der Benutzer von der Funktion **Jetzt wiedergeben** abschaltet. Hierzu können Sie einen Ereignishandler für das **Entladeereignis** als Teil des **BODY-Elements** angeben, wie der folgende HTML-Code veranschaulicht:


```XML
<BODY onunload = "UnloadMe();">

```



Anschließend können Sie Skriptcode in Ihre Ereignishandlerfunktion einschließen, um die Datei im Player zu schließen. Der folgende Beispielcode führt dies aus:


```XML
function UnloadMe()
{
   Player.close();
}

```



Wenn der Benutzer von **Jetzt wiedergeben** abschaltet, indem er auf eine Schaltfläche klickt, um ein weiteres Windows Media Player Feature zu öffnen, z. B. die Bibliothek, schließt der Player den eingebetteten Browser. Dadurch tritt das **Onunload-Ereignis auf,** und das Skript wird in der Funktion **unloadMe** ausgeführt. Die [Player.close-Methode](player-close.md) beendet die Wiedergabe und entlädt die aktuelle digitale Mediendatei. Um den Inhalt erneut anzuzeigen, muss der Benutzer die ursprüngliche ASX-Datei erneut öffnen. Diese Technik beendet auch die Wiedergabe, wenn der Benutzer von der HTMLView-Webseite weg navigiert. Beachten Sie, dass diese Technik nicht verhindern kann, dass der Benutzer die digitalen Medieninhalte anzeigt, wenn er in den Skinmodus wechselt.

Sie werden sich erinnern, dass der HTMLView-Parameter auf jedes **ENTRY-Element** in einer ASX-Datei angewendet werden kann. Sie können dieses Feature nutzen, um sicherzustellen, dass Ihr HTMLView-Inhalt bei jedem Start einer neuen digitalen Mediendatei angezeigt wird. Ordnen Sie hierzu jedem Eintrag in ihrer ASX-Wiedergabeliste ein **PARAM-Element** für HTMLView zu. Wenn jeder Eintrag wiedergegeben wird, kehrt der Player in den vollständigen Modus zurück und zeigt den HTMLView-Inhalt an, den Sie in der Wiedergabeliste angegeben haben.

## <a name="url-and-file-script-command-types-are-disabled-by-default"></a>Url- und FILE-Skriptbefehlstypen sind standardmäßig deaktiviert.

Windows Media Player 9-Serie oder höher stellt Einstellungen bereit, mit denen der Benutzer angeben kann, ob SKRIPTbefehle vom Typ "URL" und "FILE" ausgeführt werden können. Standardmäßig werden diese beiden Skriptbefehlstypen nicht ausgeführt. Wenn Sie benutzerdefinierte Skriptbefehlstypen verwenden, werden sie unabhängig von der Benutzereinstellung weiterhin ausgeführt. Wenn Sie Skriptbefehle vom Typ URL und FILE verwenden müssen, müssen Sie den Benutzer auffordern, die Einstellungen zu ändern. Um die Einstellungen zu ändern, klicken Sie auf **Extras**, dann **auf Optionen** und dann **auf Sicherheit.**

## <a name="reopening-an-htmlview-does-not-reload-the-webpage"></a>Beim erneuten Öffnen einer HTMLView wird die Webseite nicht erneut geladen.

Wenn der Benutzer eine ASX-Datei öffnet, die einen HTMLView-Parameter enthält, und anschließend dieselbe Datei erneut öffnet, aktualisiert Windows Media Player die HTMLView-Webseite nicht. Dies bedeutet auch, dass der Player den eingebetteten Browser nicht zur ursprünglichen HTMLView-Webseite zurückgibt, wenn Sie Benutzern erlaubt haben, von Ihrer HTMLView-Webseite zu navigieren.

## <a name="hiding-the-content-location"></a>Ausblenden des Inhaltsspeicherorts

Möglicherweise möchten Sie nicht, dass Windows Media Player den Speicherort Ihrer digitalen Medieninhalte anzeigt, während eine ASX-Datei wiedergegeben wird. In der Regel zeigt Windows Media Player beim Streamen von Inhalten aus dem Internet nur Informationen über die Wiedergabeliste selbst an. Es gibt jedoch weitere Schritte, die Sie ergreifen können, um zu verhindern, dass Benutzer den Speicherort Ihrer Inhalte bestimmen. Eine Möglichkeit, sicherzustellen, dass der Player den Pfad zu Ihren Inhalten nicht anzeigt, besteht beispielsweise darin, Ihre Inhalte mit Windows Media-Dienste serverseitigen Wiedergabelisten zu streamen. Auf diese Weise sieht der Benutzer, wenn er die Eigenschaften für den Inhalt anzeigt, die URL des Servers und nicht die URL Ihres Inhalts.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Anzeigen von Webseiten in Windows Media Player**](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[**PARAM-Element**](param-element.md)
</dt> </dl>

 

 




