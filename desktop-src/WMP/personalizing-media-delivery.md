---
title: Personalisieren der Medienbereitstellung
description: Personalisieren der Medienbereitstellung
ms.assetid: ffd62602-8bfc-4ca7-91fd-c610faa330cd
keywords:
- Windows Wiedergabelisten von Medienmetadateien, Personalisieren der Medienbereitstellung
- Wiedergabelisten,Personalisierung der Medienbereitstellung
- Metafile-Wiedergabelisten, Personalisieren der Medienbereitstellung
- Windows Wiedergabelisten von Medienmetadateien, Personalisierung der Medienbereitstellung
- Wiedergabelisten,Media Delivery-Personalisierung
- Metafile-Wiedergabelisten,Media Delivery-Personalisierung
- Media Delivery-Personalisierung
- Personalisieren der Medienbereitstellung
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9483f4fc7a068c6f6456a5d170b4be73a9ba31ef85294f9a6939181dff00c826
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996010"
---
# <a name="personalizing-media-delivery"></a>Personalisieren der Medienbereitstellung

Im Gegensatz zur 1-Wege-Kommunikation, bei der identische Inhalte an eine Massenaudienz übertragen werden, stellt Windows Media Technologies Ihnen die Tools zur Verfügung, mit denen Sie demografische Daten verwenden können, um Broadcasts zu individualisieren. Mit dem Internet ist die kommunikation in großem Umfang problemlos möglich. Dieser dynamische Informationsaustausch ermöglicht Inhaltsanbietern, ihre Zielgruppe zu kennen und mit benutzerdefinierten Präsentationen zu reagieren.

Im folgenden Beispiel wird anhand eines fiktiven Unternehmens veranschaulicht, wie die Übermittlung von Streaminginhalten personalisiert werden kann. In dieser Diskussion wird davon ausgegangen, dass Sie mit Active Server Pages (ASP- oder ASP-Dateien) und definierenden Variablen vertraut sind.

News Network ist eine fiktive Nachrichtenorganisation, die ihren Betrieb um eine Website erweitert hat. Das Hauptfeature der Website ist ein Abschnitt, in dem Benutzer eigene personalisierte Newscasts erstellen können. Anstatt sich einen herkömmlichen Nachrichtennachrichten zu ansehen, der auf eine Massenaudienz ausgerichtet ist, sieht ein Benutzer ein vollständiges Nachrichtenprogramm, das nur Themen von persönlichem Interesse enthält. In der folgenden Sequenz wird eine typische Benutzeroberfläche beschrieben.

1.  Ein neuer Benutzer geht zur Website und klickt auf Create Your Personal Newscast (Persönlichen **Newscast erstellen).**
2.  Ein Einstellungsformular wird geöffnet. In diesem Formular beantwortet der Benutzer Fragen zu persönlichen Vorlieben, z. B. bevorzugte Nachrichten, am wenigsten bevorzugte Nachrichten, Nachbildungen und die übliche Methode zum Empfangen täglicher Nachrichten.
3.  Der Benutzer sendet diese Informationen, und einige Sekunden später wird ein vollständiger, 15-minütiger persönlicher Newscast angezeigt, der Programminhalte, Übergänge und Werbespots enthält. Die Auswahl der einzelnen Medienelemente, einschließlich Werbespots, basiert auf dem Benutzerprofil und wird automatisch mithilfe von Windows Media Technologies-Komponenten und standardbasierten Internettools durchgeführt.

In der folgenden Liste wird beschrieben, wie die verschiedenen Tools interagieren, um einen personalisierten Newscast zu erstellen.

1.  Das Vom Benutzer ausfüllende Einstellungsformular ist eine Active Server-Seite (ASP) (Choices.asp). Aus dem Einstellungsformular erhaltene Daten werden von zwei Serverkomponenten analysiert. Eine Komponente verwendet die Informationen, um eine Microsoft SQL Server Datenbank mit Nachrichten abfragt. Die andere Komponente ist ein Werbeserver, der einen komplexen Satz von Regeln basierend auf vertraglichen Anforderungen und demografischen Daten verwendet, um für den Benutzer geeignete Anzeigen zu diesem Zeitpunkt zu planen.
2.  Die beiden Datenbanken geben unterschiedliche Teile einer Wiedergabeliste zurück. Die News Story-Datenbank gibt eine Reihe von entsprechenden Storyeinträgen zurück, und der Werbeserver gibt einen Satz entsprechender kommerzieller Einträge zurück.
3.  Eine zweite ASP-Seite (PlayShow.asp) empfängt die Einträge aus der News Story-Datenbank und dem Werbeserver und kombiniert diese mit standardmäßigen Show Open-, Close- und Transition-Einträgen. Alle Einträge werden dann gemäß der von PlayShow.asp bereitgestellten Vorlage festgelegt, und die ASP-Seite gibt eine Wiedergabeliste an den Benutzer zurück.
4.  Das eingebettete Windows Media Player auf dem Computer des Benutzers gibt die Wiedergabeliste von Anfang bis Ende wieder, und der Benutzer sieht einen personalisierten Newscast an.

Das folgende Beispiel ist ein Teil einer Wiedergabelistendatei, den ein Benutzer möglicherweise erhält. Werbebanner, MOREINFO-Links und ABSTRACTS wurden hinzugefügt.


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

[**Erstellen von Metadateiwiedergabelisten**](creating-metafile-playlists.md)
</dt> <dt>

[**Metafile-Wiedergabelisten**](metafile-playlists.md)
</dt> <dt>

[**Verwenden von Metafile-Wiedergabelisten**](using-metafile-playlists.md)
</dt> <dt>

[**Windows Referenz zu Medienmetadateielementen**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Leitfaden zur Medienmetadatei**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




