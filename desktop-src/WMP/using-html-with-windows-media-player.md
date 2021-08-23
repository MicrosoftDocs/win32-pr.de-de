---
title: Verwenden von HTML mit Windows Media Player
description: Verwenden von HTML mit Windows Media Player
ms.assetid: 321d4396-511b-4f0d-9ee9-8bdddceedc0e
keywords:
- Windows Media Player,HTML
- Windows Media Player-Objektmodell,HTML
- Objektmodell, HTML
- Windows Media Player ActiveX,HTML für Objektmodell
- ActiveX,HTML für objektmodell
- Windows Media Player Mobiles ActiveX-Steuerelement,HTML für Objektmodell
- Windows Media Player Mobil,HTML für Objektmodell
- HTML mit Windows Media Player
- Einbetten von Webseiten, HTML
- Einbetten, Webseiten
- Skriptbefehle
- URL-Flipping
- Rich Media Streaming
- Browserunterstützung
- Anzeigen von Webseiten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d72185dec8ae9a2119d8c3218478e7ebb5a2df4d7740b25c9f4ecc016aa392e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119465920"
---
# <a name="using-html-with-windows-media-player"></a>Verwenden von HTML mit Windows Media Player

## <a name="overview"></a>Übersicht

Die Verwendung von HTML Windows Media Player ist eine hervorragende Möglichkeit, Audio- und Videoinhalte mit Text und Grafiken zu kombinieren. Sie können das Windows Media Player-Steuerelement in eine Webseite einbetten, wenn Sie Ihre statischen Inhalte ergänzen oder Webanwendungen mit digitalen Medien erstellen möchten. Wenn Sie Ihre digitalen Medien durch HTML ergänzen möchten, können Sie webseiten hingegen im vollständigen Modus des Players anzeigen, indem Sie auf diese Windows Medienmetadatei-Wiedergabelisten verweisen.

Wenn Sie benutzerdefinierte Programme schreiben, die das Windows Media Player-Steuerelement in den Remotemodus einbetten, können Sie auch die Webseiten steuern, die in den verschiedenen Bereichen des vollständigen Modus des Players angezeigt werden, wenn Ihre Benutzer das Steuerelement abdocken. Auf diese Weise können Sie die Kontinuität zwischen den angedockten und den nicht angedockten Zuzuständen beibehalten.

## <a name="web-embedding"></a>Web Embedding

Sie können das Windows Media Player-Steuerelement als Teil einer Webseite verwenden, die Sie erstellen. Weitere [Informationen finden Sie unter Einbetten des Windows Media Player-Steuerelements in eine Webseite.](embedding-the-windows-media-player-control-in-a-web-page.md)

## <a name="script-commands-and-url-flipping"></a>Skriptbefehle und URL-Flipping

Skriptbefehle sind Text-Wert-Paare, die Sie in Ihre digitalen Mediendateien oder Streams einbetten können. Sie können benutzerdefinierte Skriptbefehle ausschließlich verwenden, um Skriptcode auszulösen, während Windows Media Player Skriptbefehle automatisch verarbeiten können.

Wenn Sie über mehrere Webseiten verfügen, die eine Digitale Medienpräsentation begleiten, können URL-Skriptbefehle die Seite automatisch in einem Frame ändern, während das Windows Media Player-Steuerelement weiterhin digitale Medien in einem anderen Frame wieder gibt. Dies wird als URL-Flipping bezeichnet und ist eine hervorragende Möglichkeit, eine Multimediapräsentation zu erstellen. Mit anderen automatisch verarbeiteten Skriptbefehlen können Sie die Wiedergabe in eine andere Mediendatei oder einen anderen Stream ändern, Beschriftungstext anzeigen oder Ereignisse wie Werbeeinfügungen auslösen, die in einer Wiedergabeliste Windows Media-Metadatei definiert sind.

Weitere Informationen zum Kippen von URLs finden Sie unter [Creating Web-Based Presentations](creating-web-based-presentations.md).

## <a name="rich-media-streaming"></a>Rich Media Streaming

URL-Flipping funktioniert am besten mit einfachen Seiten, die schnell geladen werden. Bei komplexeren Seiten werden mehrere Komponenten einzeln übertragen, was die Synchronisierung der Seitenanzeige mit digitalen Medien erschwert. Um komplexe Rich Media-Präsentationen zu ermöglichen, können Webseiten einem Medienstream hinzugefügt und auf die gleiche Weise wie Audio- und Videoinhalte an den Player übermittelt werden. Auf diese Weise können Sie die Komponenten Ihrer Präsentation viel einfacher synchronisieren, insbesondere über Verbindungen mit niedriger Geschwindigkeit.

Weitere Informationen zum Rich Media-Streaming finden Sie unter [Creating Web-Based Presentations](creating-web-based-presentations.md).

## <a name="browser-support"></a>Browserunterstützung

Sie können das steuerelement Windows Media Player in Microsoft Internet Explorer, Firefox und Netscape Navigator einbetten, obwohl der Prozess für jeden etwas anders ist. Sie können auch Webseiten erstellen, die für die Arbeit mit allen drei Browsern konzipiert sind.

Mit Internet Explorer und Firefox betten Sie das Steuerelement mithilfe des HTML OBJECT-Elements ein. Der Navigator erfordert jedoch einen anderen Ansatz, da er ActiveX unterstützt. Mit Navigator verwenden Sie das APPLET-Element, um ein spezielles Java-Applet in die Seite einbetten. Dieses Applet verarbeitet die Kommunikation mit dem Player-ActiveX Steuerelement.

Weitere Informationen zur Firefox-Unterstützung finden Sie unter [Verwenden des Windows Media Player-Steuerelements mit Firefox](using-the-windows-media-player-control-with-firefox.md).

Weitere Informationen zur Unterstützung Netscape Navigator finden Sie unter Using Windows Media Player with Netscape 7.1 (Verwenden von Windows Media Player [mit Netscape 7.1).](using-windows-media-player-with-netscape-7-1.md)

## <a name="displaying-web-pages-in-the-full-mode-of-the-player"></a>Anzeigen von Webseiten im vollständigen Modus des Players

Sie können die Funktionalität von Windows Media Player erweitern oder eine benutzerdefinierte Ansicht der Informationen bereitstellen, die mit Ihren digitalen Medien begleitet wird, indem Sie Webseiten im vollständigen Modus des Players anzeigen. Dies ist das HTMLView-Feature Windows Medienmetadateien. Metadateien bieten Ihnen eine hervorragende Kontrolle über Wiedergabelisteninhalte, sodass Sie nahtlos zwischen Clips überwechseln, Ankündigungen einfügen und stille Bilder in Windows Media Player. Um Webseiten im vollständigen Modus des Players anzuzeigen, verwenden Sie das PARAM-Element, um IHREN Wiedergabelisteneinträgen oder ganzen Wiedergabelisten URL-Verweise hinzuzufügen.

Weitere Informationen zur Verwendung von Webseiten in Metadateien finden Sie unter [Anzeigen von Webseiten in Windows Media Player.](displaying-web-pages-in-windows-media-player.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen zum Player-Objektmodell**](about-the-player-object-model.md)
</dt> </dl>

 

 




