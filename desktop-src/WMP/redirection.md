---
title: Umleitung
description: Umleitung
ms.assetid: c8e3b43f-c11a-4ca7-b85c-038f0bfc3eb3
keywords:
- Windows Wiedergabelisten von Medienmetadateien,Umleitung
- Wiedergabelisten,Umleitung
- Metafile-Wiedergabelisten,Umleitung
- Windows Media Player,Redirection
- Umleiten
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e335250777c92634a805221a2d4f915a0dcadcad152cd03091cc9c79a662193d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117934155"
---
# <a name="redirection"></a>Umleitung

Die Wiedergabeliste leitet den Browser an Windows Media Player, um den angegebenen Medienstream oder die Mediendatei wiederzuspielen. Die grundlegendste Metadateiwiedergabeliste enthält nur die Uniform Resource Locator (URL) einer Mediendatei.

Um eine einfache Metadateiwiedergabeliste zu erstellen, öffnen Sie Ihren bevorzugten Text-Editor, z. B. Microsoft Editor, und geben Sie den folgenden Beispielcode ein.


```XML
<ASX version="3.0">
   <ENTRY>
      <REF HREF="PathToYourFile"/>
   </ENTRY>
</ASX>

```



Ersetzen Sie einen gültigen Pfad zu Ihrer Windows-Mediendatei mithilfe der Syntax in der folgenden Tabelle.



| Quelle des Inhalts                                                                                 | Syntax                                    |
|---------------------------------------------------------------------------------------------------|-------------------------------------------|
| Inhalt ist eine Datei auf einem Windows Medienserver.                                                       | mms://ServerName/Path/FileName.wma        |
| Inhalt ist ein Broadcast-Multicast, auf den von einer Media Station Windows zugegriffen wird.                    | https://WebServerName/Stations/kxyz.nsc    |
| Inhalt ist ein Broadcast-Unicast, auf den von einem Veröffentlichungspunkt auf einem Windows Zugegriffen wird. | mms://ServerName/PublishingPointAlias     |
| Inhalt ist eine Datei auf einem Webserver.                                                                 | https://WebServerName/Path/Filename.wma    |
| Inhalt ist eine Datei auf einer lokalen Festplatte.                                                            | file://c: \\ \\ Pfaddateiname.wma             |
| Inhalt ist eine Datei auf einer Netzwerkfreigabe.                                                              | file:// \\ \\ ServerName \\ Path \\ Filename.wma |
| Inhalt ist eine Datei auf einem Windows Medienserver.                                                       | mms://ServerName/Path/FileName.wmv        |



 

Speichern Sie die erstellte Datei mit einem Dateinamen und einer Erweiterung, wie unter [Dateinamenerweiterungen beschrieben.](file-name-extensions.md) Doppelklicken Sie im Windows Explorer darauf. Windows Media Player sollte geöffnet werden und mit dem Streamen des Inhalts beginnen. Sie können die Datei zusammen mit Ihren Webseiten auf Ihrem Webserver speichern und mit einem **HREF-Element** darauf verknüpfen oder sie mithilfe des Windows Media Player **OBJECT-Tags** in eine Webseite einbetten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Metafile-Wiedergabelisten**](metafile-playlists.md)
</dt> <dt>

[**Verwenden von Metafile-Wiedergabelisten**](using-metafile-playlists.md)
</dt> <dt>

[**Windows Referenz zu Medienmetadateielementen**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Leitfaden zur Medienmetadatei**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




