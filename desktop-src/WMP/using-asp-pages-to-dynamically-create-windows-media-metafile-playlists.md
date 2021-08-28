---
title: Verwenden von ASP-Seiten zum dynamischen Erstellen Windows Medienmetadatei-Wiedergabelisten
description: Verwenden von ASP-Seiten zum dynamischen Erstellen Windows Medienmetadatei-Wiedergabelisten
ms.assetid: 9abf04a4-33b9-4502-aaf3-e40de06c7b41
keywords:
- Windows Wiedergabelisten von Medienmetadateien, Erstellen
- Metafile-Wiedergabelisten,erstellen
- Wiedergabelisten,erstellen
- Windows Wiedergabelisten von Medienmetadateien, dynamisch erstellen
- Metafile-Wiedergabelisten, dynamisch erstellen
- Wiedergabelisten,dynamisch erstellen
- Windows Wiedergabelisten von Medienmetadateien, ASP-Seiten
- Metafile-Wiedergabelisten, ASP-Seiten
- Wiedergabelisten, ASP-Seiten
- Erstellen Windows Medienmetadatei-Wiedergabelisten
- Dynamisches Erstellen Windows Medienmetadatei-Wiedergabelisten
- ASP-Seiten
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 096a71a5ffedb353cbfd75fb1b5c23b97065ca96c0d75ac30588c44e7720f779
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119762070"
---
# <a name="using-asp-pages-to-dynamically-create-windows-media-metafile-playlists"></a>Verwenden von ASP-Seiten zum dynamischen Erstellen Windows Medienmetadatei-Wiedergabelisten

Sie können Active Server Pages (ASP- oder ASP-Dateien) verwenden, um Wiedergabelisten basierend auf den von Benutzern bereitgestellten Informationen dynamisch zu generieren. Eine ASP-Seite ist eine dynamische Webseite, die in Verbindung mit Microsoft-Internetinformationsdienste (IIS) verwendet wird. ASP ist eine Umgebung, in der Sie HTML, Skripts und wiederverwendbare ActiveX-Serverkomponenten kombinieren können, um dynamische und leistungsstarke webbasierte Geschäftslösungen zu erstellen. ASP-Seiten ermöglichen serverseitige Skripts für IIS mit nativer Unterstützung für Microsoft Visual Basic Scripting Edition (VBScript) und Microsoft JScript. In dieser Diskussion wird davon ausgegangen, dass Sie mit ASP und dem Definieren von Variablen vertraut sind.

Alle Headerinformationen müssen in der ersten Zeile der ASP-Seitenzeichenfolge enthalten sein, die an die Windows Media Player.

Wenn Sie ASP-Seiten zum Generieren von Wiedergabelisten verwenden, müssen Sie  Werte für **den ContentType** des **Response-Objekts** angeben und laufen die Eigenschaften auf der ASP-Seite aufgrund von Latenzproblemen mit Windows Media Player. Der **Response.ContentType-Wert** muss eine gültige Dateierweiterung für Windows Medienmetadateien sein. Zulässige Werte sind wma, wr, wmv, wvx, asf und asx.

Die **Response.expires-Eigenschaft** gibt die Zeitdauer in Sekunden an, die Windows Media Player Wiedergabelistendatei zwischenspeichert. Wenn Sie den Wert 0 (null) angeben, Windows Media Player immer dann eine neue Wiedergabeliste vom Server anfordern, wenn der Benutzer die Seite aktualisiert.

Weitere Informationen zur Verwendung des  Response-Objekts in Active Server Pages finden Sie im Plattform-SDK.

Der folgende Code ist ein Beispiel für eine ASP-Seite, die verwendet wird, um eine Windows Media-Metadateiwiedergabeliste zu generieren.


```XML
<%Response.ContentType = "video/x-ms-wma"%><%Response.expires=0 %>
<ASX VERSION="3.0">
    <TITLE>Your title here</TITLE>
    <ENTRY>
        <REF HREF ="mms://adventure-works.com/pubpt/filename.wma" />
    </ENTRY>
</ASX>

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Erstellen von Metadateiwiedergabelisten**](creating-metafile-playlists.md)
</dt> </dl>

 

 




