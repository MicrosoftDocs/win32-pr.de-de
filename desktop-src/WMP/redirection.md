---
title: Umleitung
description: Umleitung
ms.assetid: c8e3b43f-c11a-4ca7-b85c-038f0bfc3eb3
keywords:
- Windows Media Metadatei-Wiedergabelisten, Umleitung
- Wiedergabelisten, Umleitung
- Metadatei-Wiedergabelisten, Umleitung
- Windows-Media Player, Umleitung
- Umleiten
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bf1bb4d690c8aa6808e009a45a7bff1d6efada72
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309327"
---
# <a name="redirection"></a>Umleitung

Die Wiedergabeliste leitet den Browser an Windows Media Player, um den festgelegten Mediendaten Strom oder die angegebene Mediendatei wiederzugeben. Die einfachste Metadatendatei-Wiedergabeliste enthält nur die Uniform Resource Locator (URL) einer Mediendatei.

Öffnen Sie zum Erstellen einer einfachen Metadatei-Wiedergabeliste Ihren bevorzugten Text-Editor, z. b. Microsoft Notepad, und geben Sie den folgenden Beispielcode ein.


```XML
<ASX version="3.0">
   <ENTRY>
      <REF HREF="PathToYourFile"/>
   </ENTRY>
</ASX>

```



Ersetzen Sie mithilfe der in der folgenden Tabelle aufgeführten Syntax einen gültigen Pfad zu Ihrer Windows-Mediendatei.



| Quelle des Inhalts                                                                                 | Syntax                                    |
|---------------------------------------------------------------------------------------------------|-------------------------------------------|
| Der Inhalt ist eine Datei auf einem Windows Media-Server.                                                       | mms://ServerName/Path/FileName.wma        |
| Inhalt ist ein Broadcast-Multicast, auf den von einer Windows-Medienstation aus zugegriffen wird.                    | https://WebServerName/Stations/kxyz.nsc    |
| Der Inhalt ist ein Broadcast-Unicast, auf den von einem Publishing Point auf einem Windows Media-Server zugegriffen wird. | mms://ServerName/PublishingPointAlias     |
| Der Inhalt ist eine Datei auf einem Webserver.                                                                 | https://WebServerName/Path/Filename.wma    |
| Der Inhalt ist eine Datei auf einer lokalen Festplatte.                                                            | file://c: \\ Pfad \\ Dateiname. WMA             |
| Der Inhalt ist eine Datei auf einer Netzwerkfreigabe.                                                              | file:// \\ \\ Servername \\ Pfad \\ Dateiname. WMA |
| Der Inhalt ist eine Datei auf einem Windows Media-Server.                                                       | mms://ServerName/Path/FileName.wmv        |



 

Speichern Sie die Datei, die Sie erstellt haben, mit einem Dateinamen und einer Erweiterung, wie in [Dateinamen Erweiterungen](file-name-extensions.md)beschrieben. Doppelklicken Sie in Windows-Explorer auf die Datei. Windows Media Player sollte geöffnet werden und mit dem Streamen der Inhalte beginnen. Sie können die Datei zusammen mit ihren Webseiten auf dem Webserver speichern und mit einem **href** -Element verknüpfen oder Sie mithilfe des Windows-Media Player **Objekttags** in eine Webseite einbetten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Metafile-Wiedergabelisten**](metafile-playlists.md)
</dt> <dt>

[**Verwenden von Metafile-Wiedergabelisten**](using-metafile-playlists.md)
</dt> <dt>

[**Verweis auf Windows Media-Metadateielemente**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Leitfaden für Windows Media-Metadateien**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




