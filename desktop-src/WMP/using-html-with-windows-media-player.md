---
title: Verwenden von HTML mit Windows-Media Player
description: Verwenden von HTML mit Windows-Media Player
ms.assetid: 321d4396-511b-4f0d-9ee9-8bdddceedc0e
keywords:
- Windows Media Player, HTML
- Windows Media Player-Objektmodell, HTML
- Objektmodell, HTML
- Windows Media Player ActiveX-Steuerelement, HTML für Objektmodell
- ActiveX-Steuerelement, HTML für Objektmodell
- Windows Media Player Mobile ActiveX-Steuerelement, HTML für Objektmodell
- Windows Media Player Mobile, HTML für Objektmodell
- HTML mit Windows-Media Player
- Einbettung von Webseiten, HTML
- Einbettungen, Webseiten
- Skript Befehle
- URL-kippen
- Rich-Media-Streaming
- Browserunterstützung
- Anzeigen von Webseiten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7cd96932573802d0a75f95a437b2c7284b3de44
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856263"
---
# <a name="using-html-with-windows-media-player"></a>Verwenden von HTML mit Windows-Media Player

## <a name="overview"></a>Übersicht

Die Verwendung von HTML mit Windows Media Player ist eine hervorragende Möglichkeit, um Audioinhalte und Videos mit Text und Grafiken zu kombinieren. Sie können das Windows Media Player-Steuerelement in eine Webseite einbetten, wenn Sie Ihre statischen Inhalte ergänzen oder Webanwendungen mit digitalen Medien erstellen möchten. Wenn Sie Ihre digitalen Medien mit HTML ergänzen möchten, können Sie Webseiten im vollständigen Modus des Players anzeigen, indem Sie in den Windows Media Metadatei-Wiedergabelisten auf Sie verweisen.

Wenn Sie benutzerdefinierte Programme schreiben, die das Windows Media Player-Steuerelement im Remote Modus einbetten, können Sie auch die Webseiten steuern, die in den verschiedenen Bereichen des vollständigen Modus des Players angezeigt werden, wenn die Benutzer das Steuerelement Abdocken. Auf diese Weise können Sie die Kontinuität zwischen angedockten und nicht angedockten Zuständen beibehalten.

## <a name="web-embedding"></a>Webeinbettung

Sie können das Windows Media Player-Steuerelement als Teil einer Webseite verwenden, die Sie erstellen. Informationen finden Sie [unter Einbetten des Windows Media Player-Steuer Elements in eine Webseite](embedding-the-windows-media-player-control-in-a-web-page.md).

## <a name="script-commands-and-url-flipping"></a>Skript Befehle und URL-Flipping

Skript Befehle sind Text/Wert-Paare, die Sie in Ihre digitalen Mediendateien oder Streams einbetten können. Sie können benutzerdefinierte Skript Befehle ausschließlich zum Lösen von Skriptcode verwenden, während Windows Media Player anderen Skript Befehlen automatisch verarbeiten lässt.

Wenn Sie über mehrere Webseiten verfügen, die eine digitale Medienpräsentation begleiten, können URL-Skript Befehle die Seite automatisch in einem Frame ändern, während das Windows Media Player-Steuerelement weiterhin digitale Medien in einem anderen Frame wieder gibt. Dies wird als URL-Flipping bezeichnet und ist eine hervorragende Möglichkeit zum Erstellen einer Multimedia-Folien Anzeige. Mit anderen automatisch behandelten Skript Befehlen können Sie die Wiedergabe in eine andere Mediendatei oder einen anderen Stream umschalten, Beschriftungs Text anzeigen oder Ereignisse wie AD-Einfügungen Auslöschungen, die in einer Windows Media Metadatei-Wiedergabeliste definiert sind.

Weitere Informationen zum Überspringen von URLs finden Sie unter [Erstellen von Web-Based Präsentationen](creating-web-based-presentations.md).

## <a name="rich-media-streaming"></a>Rich-Media-Streaming

Das URL-kippen funktioniert am besten mit einfachen Seiten, die schnell geladen werden. Bei komplexeren Seiten werden mehrere Komponenten einzeln übertragen, was das Synchronisieren der Seiten Anzeige mit digitalen Medien erschwert. Zum zulassen komplexer Rich-Media-Präsentationen können Webseiten einem Mediendaten Strom hinzugefügt und auf die gleiche Weise wie Audioinformationen und Videos an den Player übermittelt werden. Auf diese Weise können Sie die Komponenten Ihrer Präsentation viel einfacher synchronisieren, insbesondere über Verbindungen mit geringer Geschwindigkeit.

Weitere Informationen zum Streaming von Rich-Media-Medien finden Sie unter [Erstellen von Web-Based Präsentationen](creating-web-based-presentations.md).

## <a name="browser-support"></a>Browserunterstützung

Sie können das Windows Media Player-Steuerelement in Microsoft Internet Explorer, Firefox und Netscape Navigator einbetten, obwohl der Prozess für jeden Prozess etwas unterschiedlich ist. Sie können auch Webseiten erstellen, die für alle drei Browser entworfen wurden.

Mit Internet Explorer und Firefox Betten Sie das Steuerelement mithilfe des HTML-Objekt Elements ein. Der Navigator erfordert jedoch einen anderen Ansatz, da ActiveX-Steuerelemente nicht direkt unterstützt werden. Mit Navigator verwenden Sie das Applet-Element, um ein spezielles Java-Applet in die Seite einzubetten. Dieses Applet verarbeitet die Kommunikation mit dem Player-ActiveX-Steuerelement.

Weitere Informationen zur Unterstützung von Firefox finden [Sie unter Verwenden des Windows Media Player-Steuer Elements mit Firefox](using-the-windows-media-player-control-with-firefox.md).

Weitere Informationen zur Unterstützung von Netscape Navigator finden [Sie unter Verwenden von Windows Media Player mit Netscape 7,1](using-windows-media-player-with-netscape-7-1.md).

## <a name="displaying-web-pages-in-the-full-mode-of-the-player"></a>Anzeigen von Webseiten im vollständigen Modus des Players

Sie können die Funktionalität von Windows Media Player erweitern oder eine benutzerdefinierte Ansicht der Informationen bereitstellen, die Ihre digitalen Medien enthalten, indem Sie Webseiten im vollständigen Modus des Players anzeigen. Dies ist die HtmlView-Funktion von Windows Media-Metafiles. Metadatendateien ermöglichen Ihnen eine hervorragende Kontrolle über den Wiedergabelisten Inhalt, sodass Sie nahtlos zwischen Clips wechseln, Ankündigungen einfügen und weiterhin Bilder in Windows Media Player anzeigen können. Wenn Sie Webseiten im vollständigen Modus des Players anzeigen möchten, verwenden Sie das param-Element, um Ihren Wiedergabelisten Einträgen oder vollständigen Wiedergabelisten URL-Verweise hinzuzufügen.

Weitere Informationen zur Verwendung von Webseiten in Metadateien finden Sie unter [Anzeigen von Webseiten in Windows Media Player](displaying-web-pages-in-windows-media-player.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen zum Player-Objektmodell**](about-the-player-object-model.md)
</dt> </dl>

 

 




