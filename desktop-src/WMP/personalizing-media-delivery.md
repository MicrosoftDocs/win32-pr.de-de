---
title: Personalisieren der Medien Bereitstellung
description: Personalisieren der Medien Bereitstellung
ms.assetid: ffd62602-8bfc-4ca7-91fd-c610faa330cd
keywords:
- Windows Media Metadatei-Wiedergabelisten, Personalisieren der Medien Bereitstellung
- Wiedergabelisten, Personalisieren der Medien Übermittlung
- Metadatei-Wiedergabelisten, Personalisieren der Medien Übermittlung
- Windows Media Metadatei-Wiedergabelisten, Personalisierung von Medien Übermittlung
- Wiedergabelisten, Personalisierung von Medien Übermittlung
- Metadatei-Wiedergabelisten, Personalisierung von Medien Übermittlung
- Personalisierung der Medien Übermittlung
- Personalisieren der Medien Bereitstellung
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ddb01364e2ea36214b94d01517f1d3d3b802ba63
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206347"
---
# <a name="personalizing-media-delivery"></a>Personalisieren der Medien Bereitstellung

Anders als bei der unidirektionalen Kommunikation, bei der identische Inhalte an eine große Zielgruppe übermittelt werden, bietet Windows Media-Technologien Ihnen die Tools, mit denen Demographics zum Individualisieren von Sendungen Mit dem Internet ist die bidirektionale Kommunikation mit einer großen Skalierung sofort verfügbar. Dieser dynamische Informationsaustausch ermöglicht Inhaltsanbietern, Ihre Zielgruppe zu kennen und mit angepassten Präsentationen zu antworten.

Im folgenden Beispiel wird mithilfe eines fiktiven Unternehmens veranschaulicht, wie die Übermittlung von Streaminginhalten personalisiert werden kann. In dieser Erläuterung wird davon ausgegangen, dass Sie mit Active Server Seiten (ASP-oder ASP-Dateien) vertraut sind und Variablen definieren.

News Network ist eine fiktive Broadcast-News-Organisation, die den Betrieb erweitert hat, um eine Website einzubeziehen. Das Haupt Feature der Site ist ein Abschnitt, in dem Benutzer ihre eigenen personalisierten neuskoren erstellen können. Anstatt eine herkömmliche newscast anzuzeigen, die auf eine große Zielgruppe ausgerichtet ist, zeigt ein Benutzer ein umfassendes Nachrichtenprogramm an, das nur Themen mit persönlichem Interesse enthält. In der folgenden Sequenz wird eine typische Benutzer Darstellung beschrieben.

1.  Ein neuer Benutzer wechselt zur Website und klickt auf **Create Your Personal newscast**.
2.  Ein bevorzugte Formular wird geöffnet. In diesem Formular beantwortet der Benutzer Fragen zu persönlichen Vorlieben, wie z. b. bevorzugte News Storys, am wenigsten bevorzugte News Stories, Hobbys und eine übliche Methode zum empfangen täglicher Nachrichten.
3.  Der Benutzer sendet diese Informationen, und einige Sekunden später wird eine komplette, 15-minütige, persönliche newscast mit Programm Inhalt,-Übergängen und-Werbeeinblendungen angezeigt. Die Auswahl der einzelnen Medienelemente (einschließlich der Werbespots) basiert auf dem Benutzerprofil und wird automatisch mit den Komponenten der Windows Media-Technologien und den Tools für das Offline-Internet erreicht.

In der folgenden Liste wird beschrieben, wie die verschiedenen Tools interagieren, um eine personalisierte newscast zu erstellen.

1.  Das bevorzugte Formular, das der Benutzer ausfüllt, ist eine Active Server Seite (ASP) ("Choices. asp"). Daten, die aus dem bevorzugten Formular abgerufen werden, werden von zwei Serverkomponenten analysiert. Eine Komponente verwendet die Informationen, um eine Microsoft SQL Server Datenbank von News Storys abzufragen. Bei der anderen Komponente handelt es sich um einen Ad-Server, der einen komplexen Regelsatz verwendet, der auf vertraglichen Anforderungen und demografiken basiert, um die Werbeeinblendungen zu diesem Zeitpunkt zu planen.
2.  Die beiden Datenbanken geben verschiedene Teile einer Wiedergabeliste zurück. Die News Story-Datenbank gibt eine Reihe entsprechender Story-Einträge zurück, und der Ad-Server gibt eine Reihe geeigneter kommerzieller Einträge zurück.
3.  Eine zweite ASP-Seite (playshow. ASP) empfängt die Einträge aus der News Story-Datenbank und dem Ad-Server und kombiniert diese mit den standardmäßigen Show Open-, Close-und Transition-Einträgen. Alle Einträge werden dann entsprechend der von playshow. ASP bereitgestellten Vorlage angeordnet, und die ASP-Seite gibt eine Wiedergabeliste an den Benutzer zurück.
4.  Das eingebettete Windows Media Player-Steuerelement auf dem Computer des Benutzers spielt die Wiedergabeliste von Anfang bis Ende, und der Benutzer zeigt eine personalisierte newscast an.

Das folgende Beispiel ist ein Teil einer Wiedergabelisten Datei, die ein Benutzer möglicherweise empfängt. Ad-Banner, moreingefo-Links und Abstracts wurden hinzugefügt.


```XML
<ASX Version="3">
<TITLE>MyPersonalized NewsCast</TITLE>
<ENTRY ClientSkip="no">
    <!<entity type="mdash"/>- Commercial Element 1 -->
    <REF HREF="mms://proseware.com/Commercial.wma" />
    <BANNER HREF="https://www.proseware.com/images/MoreInfo.gif" >
        <MOREINFO HREF="https://www.proseware.com" target="_blank" />
    <ABSTRACT>Courtesy of Windows Media Technologies
    </ABSTRACT>
    </BANNER>
</ENTRY>
<ENTRY>
    <!<entity type="mdash"/>- Program Element 1 -->
    <TITLE>A Celebrity's Life</TITLE>
    <COPYRIGHT>Copyright 2004</COPYRIGHT>
    <REF HREF="mms://proseware.com/SomePath/TheFile.wma" />
    <ABSTRACT>
     :: A celebrity looks back on her career after 40 years in public life.
    </ABSTRACT>
    <COPYRIGHT>Copyright 2004-- All Rights
         Reserved
    </COPYRIGHT>
</ENTRY>

<ENTRY>
    <!<entity type="mdash"/>Program Element 2 -->
    <TITLE>City council votes to build new bicycle path</TITLE>
    <COPYRIGHT>Copyright 2004</COPYRIGHT>
    <REF HREF="mms://proseware.com/SomePath/MyFile.wma" />
    <ABSTRACT>
        :: Some residents opposed changing the landscape in the public parks to accommodate bicycles.
    </ABSTRACT>
    <COPYRIGHT>Copyright 2004 -- All Rights Reserved
    </COPYRIGHT>
</ENTRY>
</ASX>

```



-   Die in den Beispielen verwendeten Firmen, Organisationen, Produkte, Personen und Ereignisse sind frei erfunden, soweit nichts anderes angegeben ist. Jede Ähnlichkeit mit bestehenden Firmen, Organisationen, Produkten, Personen oder Ereignissen ist rein zufällig.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Erstellen von Metafile-Wiedergabelisten**](creating-metafile-playlists.md)
</dt> <dt>

[**Metafile-Wiedergabelisten**](metafile-playlists.md)
</dt> <dt>

[**Verwenden von Metafile-Wiedergabelisten**](using-metafile-playlists.md)
</dt> <dt>

[**Verweis auf Windows Media-Metadateielemente**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Leitfaden für Windows Media-Metadateien**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




