---
title: Vorteile der Verwendung von HtmlView
description: Vorteile der Verwendung von HtmlView
ms.assetid: bbec9471-87f1-4c41-a322-f11e9e1dec37
keywords:
- Windows Media Metadatei-Wiedergabelisten, HtmlView-Vorteile
- Wiedergabelisten, HtmlView-Vorteile
- Metadatei-Wiedergabelisten, HtmlView-Vorteile
- Windows Media Metadatei-Wiedergabelisten, Vorteile von HtmlView
- Wiedergabelisten, Vorteile von HtmlView
- Metadatei-Wiedergabelisten, Vorteile von HtmlView
- Vorteile von HtmlView
- Windows Media Player, Vorteile von HtmlView
- Windows Media Player, HtmlView-Vorteile
- HtmlView, Vorteile
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f5e5409db969f5e9a8e0df18738f4995490b1d83
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388527"
---
# <a name="advantages-of-using-htmlview"></a>Vorteile der Verwendung von HtmlView

Mit der HtmlView-Funktion können Sie auf einfache Weise eine integrierte webbasierte Benutzer Funktionalität erstellen, mit der digitale Medieninhalte wiedergegeben werden, indem das vertraute Erscheinungsbild des Internets verwendet wird. Wenn Sie webbasierten Inhalt mit digitalen Medieninhalten in der Windows Media Player-Benutzeroberfläche (UI) kombinieren, kann das Ergebnis eine größere Auswirkung auf den Benutzer haben, als wenn die Elemente separat angezeigt werden. Der Inhalt digitaler Medien wird durch interessante Verwandte Informationen erweitert, während die Webseite Links zu ähnlichen Inhalten bereitstellen kann, sodass neue Geschäftschancen geschaffen werden.

## <a name="htmlview-provides-a-better-user-experience"></a>HtmlView bietet eine bessere Benutzer Leistung.

Benutzer haben Zugriff auf die Informationen, die mit digitalen Medieninhalten angeboten werden können, aber Sie möchten nicht mit einer scheinbar unendlichen Reihe von Popup Ankündigungen umgehen. Die Verwendung von Popup Browserfenstern zum Anzeigen von Werbung im Web ist so üblich, dass jetzt Software vorhanden ist, die das Öffnen dieser Fenster verhindert. Diese Software kann den unerwünschten Nebeneffekt haben, dass legitime Webseiten nicht angezeigt werden. manchmal wird eine gesamte digitale Medienpräsentation unterdrückt.

Wenn Sie die HtmlView-Funktion verwenden, müssen Benutzer sich nicht mehr mit Popup Fenstern beschäftigen. Anstatt ein separates Browserfenster zum Bereitstellen zusätzlicher Informationen für den Benutzer zu öffnen, können Sie benutzerdefinierten webbasierten Inhalt in der Windows Media Player-Benutzeroberfläche anzeigen, **während der Player** die Audioinhalte oder Videoinhalte des Benutzers wieder gibt. Benutzer können die Wiedergabe mithilfe der Windows Media Player-Steuerelemente steuern. Da Ihre Inhalte im vollmodusplayer abgespielt werden, hindert die Software, die zum Verhindern von Popup-Werbeeinblendungen konzipiert ist, den Inhalt nicht mehr.

## <a name="htmlview-content-is-easy-to-create"></a>HtmlView-Inhalte können einfach erstellt werden.

Wie der Funktionsname schon sagt, erstellen Sie mithilfe der HtmlView-Funktion mithilfe von Hypertext Markup Language (HTML) webbasierten Inhalt. Wenn Sie bereits Inhalte für das Web erstellen, bedeutet dies, dass Sie keine neue Programmiersprache erlernen müssen, um mit der HtmlView-Funktion problemlos umfangreiche Inhalte zu erstellen. Wenn Sie bereits Webseiten mit einem eingebetteten Windows Media Player ActiveX-Steuerelement haben, können Sie diese Seiten in der Benutzeroberfläche des Players anzeigen lassen, indem Sie einfach auf diese Webseiten aus einer Windows Media-Metadatendatei (. ASX) mithilfe eines speziellen Parameters zeigen.

In Windows Media Player wird eine eingebettete Instanz von Microsoft Internet Explorer verwendet, um HtmlView-Inhalte anzuzeigen. Dies bedeutet, dass Sie beim Erstellen Ihrer Webseiten nicht verschiedene Internet Browser, mehrere Skript Modelle oder andere Skriptsprachen in Erwägung gezogen müssen. Selbst wenn der Benutzer Internet Explorer nicht als seinen Standardbrowser verwendet, wird die Webseite weiterhin ordnungsgemäß im Player angezeigt.

Es ist möglich, dass sich ein anderes Programm als Windows Media Player sich selbst als Standardprogramm zum Öffnen von. ASX-Dateien registrieren kann. Das Objektmodell Windows Media Player 9 oder höher enthält eine neue Methode, **openplayer**, die es Ihnen ermöglicht, eine Uniform Resource Locator (URL) für den Inhalt anzugeben, den Sie wiedergeben möchten. Wenn Sie die **openplayer** -Methode verwenden, wird Windows Media Player immer im vollständigen Modus geöffnet, um den angegebenen Inhalt wiederzugeben. Mit dieser Methode können Sie sicherstellen, dass der HtmlView-Inhalt in Windows Media Player und nicht in einer anderen Anwendung angezeigt wird, die die. ASX-Dateityp Zuordnung übernommen hat.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Anzeigen von Webseiten in Windows Media Player**](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[**Player. openplayer**](player-openplayer.md)
</dt> </dl>

 

 




