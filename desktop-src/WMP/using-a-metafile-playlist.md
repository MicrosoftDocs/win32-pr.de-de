---
title: Verwenden einer Metafile-Wiedergabeliste
description: Verwenden einer Metafile-Wiedergabeliste
ms.assetid: e6cbdb76-4405-409e-93c3-38a3baa7c231
keywords:
- Windows Media Metadatei-Wiedergabelisten mit
- Metadatei-Wiedergabelisten, verwenden
- Wiedergabelisten mit
- Windows Media Metadatei-Wiedergabelisten, Informationen zu
- Metadatei-Wiedergabelisten, Informationen
- Wiedergabelisten, Informationen
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a5f1832c0c739874fbbd4db219f2c622fc2debfa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709851"
---
# <a name="using-a-metafile-playlist"></a>Verwenden einer Metafile-Wiedergabeliste

Da keine direkte Verknüpfung von einer Webseite mit einem Streaming Media-Server möglich ist, verwenden Sie Metadatei-Wiedergabelisten. Die Metadatei-Wiedergabelisten enthalten die Informationen, die von Windows Media Player benötigt werden und auf einem Webserver gespeichert sind. Anschließend können Sie eine Verknüpfung zwischen dem Webdokument und einer Metadatendatei-Wiedergabeliste herstellen. Wenn eine Metadatei-Wiedergabeliste geöffnet wird, Steuern Sie die Übertragung an Windows-Media Player, das die Datei verarbeitet, eine Verbindung mit dem Streamingmedienserver herstellt und den angegebenen Inhalt wieder gibt.

Der Browser lädt zuerst die Metadatendatei-Wiedergabeliste in das Cache Verzeichnis des Benutzers herunter. Da die Metadatendatei-Wiedergabeliste klein ist, ist dies ein sehr schneller Schritt. Der Computer des Benutzers findet dann in der Datei Zuordnungs Tabelle die Zuordnung der Metadatei-Wiedergabeliste zu Windows Media Player. Windows Media Player öffnet und interpretiert die Skripterstellung in der Metadatei-Wiedergabeliste, die unter anderem die URL des Streaminginhalts enthält. Windows Media Player verwendet die URL, um den Inhalt zu suchen und den Stream zu initiieren. Die metadatenwiedergabe-Wiedergabeliste steuert dann das Streaming.

Da Metadatei-Wiedergabelisten über eine Hilfsanwendung funktionieren, die dem asxmime-Typ (Application/Mplayer2 oder Video/x-ms-ASF) zugeordnet ist, sind Sie mit jedem Browser kompatibel, der Hilfsanwendungen unterstützt. Die in diesem Dokument gezeigten Beispiele funktionieren mit Microsoft Internet Explorer 4,0 und höher sowie mit Netscape Navigator 4,0 und höher auf Microsoft Win32-® und Apple Macintosh-Plattformen. In allen Beispielen müssen Sie sicherstellen, dass alle digitalen Mediendateien, auf die verwiesen wird, über gültige Pfade und Dateinamen für Ihre Umgebung verfügen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Leitfaden für Windows Media-Metadateien**](windows-media-metafile-guide.md)
</dt> <dt>

[**Referenz zu Windows Media-Metadateien**](windows-media-metafile-reference.md)
</dt> <dt>

[**Übersicht über Windows Media-Metadatendateien**](windows-media-metafiles-overview.md)
</dt> </dl>

 

 




