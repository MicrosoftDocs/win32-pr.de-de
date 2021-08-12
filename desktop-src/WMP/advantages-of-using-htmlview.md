---
title: Vorteile der Verwendung von HTMLView
description: Vorteile der Verwendung von HTMLView
ms.assetid: bbec9471-87f1-4c41-a322-f11e9e1dec37
keywords:
- Windows Wiedergabelisten von Medienmetadateien, HTMLView-Vorteile
- Playlists,HTMLView-Vorteile
- Metafile-Wiedergabelisten, HTMLView-Vorteile
- Windows Wiedergabelisten von Medienmetadateien,Vorteile von HTMLView
- Wiedergabelisten,Vorteile von HTMLView
- Metafile-Wiedergabelisten,Vorteile von HTMLView
- Vorteile von HTMLView
- Windows Media Player,Vorteile von HTMLView
- Windows Media Player,HTMLView-Vorteile
- HTMLView,Vorteile
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a6019ec83466be9f4eca649d870422dce640fddc3ff011c46c6f918a1a09faa2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118583267"
---
# <a name="advantages-of-using-htmlview"></a>Vorteile der Verwendung von HTMLView

Das HTMLView-Feature erleichtert das Erstellen einer integrierten webbasierten Benutzeroberfläche, die digitale Medieninhalte mithilfe des vertrauten Aussehens des Webs wiederspiegelt. Wenn Sie webbasierte Inhalte mit digitalen Medieninhalten auf der Windows Media Player-Benutzeroberfläche kombinieren, kann das Ergebnis einen größeren Einfluss auf den Benutzer haben, als wenn die Elemente separat angezeigt werden. Die digitalen Medieninhalte werden durch interessante verwandte Informationen erweitert, während die Webseite Links zu ähnlichen Inhalten bereitstellen kann, wodurch neue Geschäftsmöglichkeiten eröffnet werden.

## <a name="htmlview-provides-a-better-user-experience"></a>HTMLView bietet eine bessere Benutzererfahrung

Benutzer möchten auf die Informationen zugreifen, die mit digitalen Medieninhalten angeboten werden können, aber sie möchten nicht mit einer scheinbar endlosen Reihe von Popup-Ankündigungen umgehen. Die Verwendung von Popupbrowserfenstern zum Anzeigen von Werbung im Web ist so üblich geworden, dass es jetzt Software gibt, die verhindert, dass diese Fenster geöffnet werden. Diese Software kann den unerwünschten Nebeneffekt haben, dass legitime Webseiten nicht angezeigt werden, und manchmal wird eine gesamte digitale Medienpräsentation unterdrückt.

Wenn Sie das HTMLView-Feature verwenden, müssen Benutzer sich nicht mehr mit Popupfenstern befassen. Anstatt ein separates Browserfenster öffnen zu müssen, um dem Benutzer zusätzliche Informationen zur  Verfügung zu stellen, können Sie benutzerdefinierte, webbasierte Inhalte in der Funktion Jetzt wiedererlangen der Windows Media Player-Benutzeroberfläche anzeigen, während der Player die audio- oder videoinhalte wieder gibt, die der Benutzer möchte. Benutzer können die Wiedergabe mithilfe der Windows Media Player steuern. Da Ihre Inhalte im Vollmodus-Player abspielt, verhindert Software, die Popupanzeigen verhindern soll, dass Benutzer die Inhalte nicht verwenden.

## <a name="htmlview-content-is-easy-to-create"></a>HTMLView-Inhalt ist einfach zu erstellen

Wie der Featurename schon sagt, erstellen Sie webbasierte Inhalte, die mithilfe des HTMLView-Features angezeigt werden, Hypertext Markup Language (HTML). Wenn Sie bereits Inhalte für das Web erstellen, bedeutet dies, dass Sie keine neue Programmiersprache erlernen müssen, um mit dem HTMLView-Feature problemlos umfangreiche Inhalte zu erstellen. Wenn Sie bereits über Webseiten mit einem eingebetteten Windows Media Player ActiveX-Steuerelement verfügen, können Sie diese Seiten auf der Player-Benutzeroberfläche anzeigen lassen, indem Sie einfach über eine Windows Media-Metadatei (ASX-Datei) mithilfe eines speziellen Parameters auf diese Webseiten verweisen.

Windows Media Player verwendet eine eingebettete Instanz von Microsoft Internet Explorer, um HTMLView-Inhalte anzuzeigen. Dies bedeutet, dass Sie beim Erstellen Ihrer Webseiten keine verschiedenen Internetbrowser, mehrere Skriptmodelle oder verschiedene Skriptsprachen berücksichtigen müssen. Auch wenn der Benutzer nicht Internet Explorer als Standardbrowser verwendet, wird Ihre Webseite weiterhin ordnungsgemäß im Player angezeigt.

Es ist möglich, dass ein anderes Programm als Windows Media Player sich selbst als Standardprogramm zum Öffnen von ASX-Dateien registriert. Das Windows Media Player-Objektmodell der 9er-Serie oder höher enthält die neue Methode **openPlayer,** mit der Sie eine Uniform Resource Locator (URL) für den Inhalt angeben können, den Sie wieder geben möchten. Wenn Sie die **openPlayer-Methode** verwenden, Windows Media Player immer im vollständigen Modus geöffnet, um den angegebenen Inhalt wieder anzugeben. Mit dieser Methode können Sie sicherstellen, dass Ihr HTMLView-Inhalt in Windows Media Player angezeigt wird, anstatt in einer anderen Anwendung, die die ASX-Dateityp-Zuordnung übernommen hat.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Anzeigen von Webseiten in Windows Media Player**](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[**Player.openPlayer**](player-openplayer.md)
</dt> </dl>

 

 




