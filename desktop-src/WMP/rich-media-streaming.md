---
title: Rich-Media-Streaming
description: Rich-Media-Streaming
ms.assetid: 3a48ee9a-5bf8-4cd0-9eed-07ec6da0f578
keywords:
- Windows Media Player, webbasierte Präsentationen
- Windows Media Player-Objektmodell, webbasierte Präsentationen
- Objektmodell, webbasierte Präsentationen
- Windows Media Player Mobile, webbasierte Präsentationen
- Windows Media Player ActiveX-Steuerelement, webbasierte Präsentationen
- Windows Media Player Mobile ActiveX-Steuerelement, webbasierte Präsentationen
- ActiveX-Steuerelement, webbasierte Präsentationen
- Windows Media Player, Rich-Media-Streaming
- Windows Media Player-Objektmodell, Rich-Media-Streaming
- Objektmodell, Rich-Media-Streaming
- Windows Media Player Mobile, Rich-Media-Streaming
- Windows Media Player ActiveX-Steuerelement, Rich-Media-Streaming
- Windows Media Player Mobile ActiveX-Steuerelement, Rich-Media-Streaming
- ActiveX-Steuerelement, Rich-Media-Streaming
- Webbasierte Präsentationen, Rich-Media-Streaming
- Erstellen von webbasierten Präsentationen, Rich-Media-Streaming
- Rich-Media-Streaming
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54b454ef62f5f5aaaf424598d55d85c03684538c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712714"
---
# <a name="rich-media-streaming"></a>Rich-Media-Streaming

Komplexe Webseiten enthalten viele verschiedene Komponenten, die normalerweise separat übertragen werden. Bei einer langsamen Verbindung werden solche Seiten jeweils nacheinander angezeigt, und es kann einige Minuten dauern, bis Sie vollständig angezeigt werden. Dadurch wird möglicherweise verhindert, dass Webseiten mit digitalen Medien synchronisiert werden. Die Lösung für dieses Problem ist das umfangreiche Medien Streaming. Dies bedeutet, dass Sie Ihre Webseiten zu Ihrem Digital Media-Stream hinzufügen, sodass Sie zur gleichen Zeit wie die Audiodaten oder Videodaten bereitgestellt werden.

Rich-Media-Streaming verwendet ein einfaches framesetlayout und verhält sich genau wie das normale URL-Flipping. Ebenso wie beim URL-Flipping werden die in digitale Medienströme eingebetteten URL-Skript Befehle verwendet, um den Inhalt im Zielframe anzuzeigen. Anstatt auf Seiten im Web zu verweisen, werden die URL-Skript Befehle jedoch von der Windows Media Player 9-Serie oder höher verwendet, um auf Dateien im Internet Explorer-Cache zuzugreifen, in denen der übertragene HTML-Inhalt beim Empfang platziert wird. Ebenso wie beim normalen URL-Flipping können Sie Ereignishandler schreiben, die auf diese URL-Skript Befehle reagieren, oder Sie können das Windows Media Player-Steuerelement automatisch verarbeiten lassen.

> [!Note]  
> Alle HTML-Inhalte, die über das Rich-Media-Streaming bereitgestellt werden, werden in der Internet Sicherheitszone wiedergegeben und unterliegen den Browser Sicherheitseinstellungen des Benutzers.

 

Weitere Informationen zum Erstellen von Rich-Media-Präsentationen finden Sie im Windows Media-Format 9 oder höher und im Windows Media Encoder 9-Serien-SDK.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Erstellen von Web-Based Präsentationen**](creating-web-based-presentations.md)
</dt> <dt>

[**Verwenden von Skripts zum Steuern von URL-Flipping**](using-script-to-control-url-flipping.md)
</dt> </dl>

 

 




