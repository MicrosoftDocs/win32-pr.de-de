---
title: Verwenden von ASP-Seiten zum dynamischen Erstellen von Windows Media Metafile-Wiedergabelisten
description: Verwenden von ASP-Seiten zum dynamischen Erstellen von Windows Media Metafile-Wiedergabelisten
ms.assetid: 9abf04a4-33b9-4502-aaf3-e40de06c7b41
keywords:
- Windows Media Metadatei-Wiedergabelisten, erstellen
- Metadatei-Wiedergabelisten, erstellen
- Wiedergabelisten, erstellen
- Windows Media Metadatei-Wiedergabelisten, dynamisches erstellen
- Metadatei-Wiedergabelisten, dynamisches erstellen
- Wiedergabelisten, dynamisches erstellen
- Windows Media Metadatei-Wiedergabelisten, ASP-Seiten
- Metadatei-Wiedergabelisten, ASP-Seiten
- Wiedergabelisten, ASP-Seiten
- Erstellen von Windows Media-Metadatei-Wiedergabelisten
- Dynamisches Erstellen von Windows Media-Metadatei-Wiedergabelisten
- ASP-Seiten
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0ea3cef88d86078aa95785163d7c2f4b0e57e975
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515687"
---
# <a name="using-asp-pages-to-dynamically-create-windows-media-metafile-playlists"></a>Verwenden von ASP-Seiten zum dynamischen Erstellen von Windows Media Metafile-Wiedergabelisten

Sie können Active Server Seiten (ASP oder ASP-Dateien) verwenden, um auf der Grundlage der von den Benutzern bereitgestellten Informationen dynamisch Wiedergabelisten zu generieren. Eine ASP-Seite ist eine dynamische Webseite, die in Verbindung mit Microsoft Internetinformationsdienste (IIS) verwendet wird. ASP ist eine Umgebung, in der Sie HTML, Skripts und wiederverwendbare ActiveX-Serverkomponenten kombinieren können, um dynamische und leistungsstarke webbasierte Geschäftslösungen zu erstellen. ASP Pages ermöglichen die serverseitige Skripterstellung für IIS mit nativer Unterstützung für Microsoft Visual Basic Scripting Edition (VBScript) und Microsoft JScript. In dieser Erläuterung wird davon ausgegangen, dass Sie mit ASP vertraut sind und Variablen definieren.

Alle Header Informationen müssen in der ersten Zeile der ASP-Seiten Zeichenfolge enthalten sein, die an Windows Media Player zurückgegeben wird.

Wenn Sie ASP-Seiten zum Generieren Media Player von Wiedergabelisten verwenden, müssen Sie Werte für die **ContentType** -Eigenschaft des **Antwort** Objekts angeben und auf der ASP-Seite auf der ASP-Seite die Eigenschaften **ablaufen** . Der **Response. ContentType** -Wert muss eine gültige Dateinamenerweiterung für Windows Media-Metadateien sein. Zulässige Werte sind WMA, Wax, WMV, WVX, ASF und ASX.

Die **Response. abgelaufen** -Eigenschaft gibt die Zeitdauer in Sekunden an, die der Windows-Media Player die Wiedergabelisten Datei zwischenspeichert. Wenn Sie einen Wert von NULL angeben, wird in Windows Media Player jedes Mal, wenn der Benutzer die Seite aktualisiert, eine neue Wiedergabeliste vom Server angefordert.

Ausführliche Informationen zur Verwendung des **Antwort** Objekts auf Active Server Seiten finden Sie im Platform SDK.

Der folgende Code ist ein Beispiel für eine ASP-Seite, die verwendet wird, um eine Windows Media Metadatei-Wiedergabeliste zu generieren.


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

[**Erstellen von Metafile-Wiedergabelisten**](creating-metafile-playlists.md)
</dt> </dl>

 

 




