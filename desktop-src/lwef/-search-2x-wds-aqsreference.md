---
title: Erweiterte Abfragesyntax
description: Die erweiterte Abfragesyntax (Advanced Query Syntax, AQS) wird von Microsoft Windows Desktop Search (WDS) verwendet, um Benutzern und Programmierern zu helfen, ihre Suchvorgänge besser zu definieren und zu verengen.
ms.assetid: 8e55bd40-c7cf-44a6-bc18-24bc7a267779
ms.topic: article
ms.date: 05/19/2020
ms.openlocfilehash: 2daf552f8f750335abacea4b550f92bd71c91c9b2b688a387b035a8180a8b3dc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119601820"
---
# <a name="advanced-query-syntax"></a>Erweiterte Abfragesyntax

> [!NOTE]
> Windows Desktop Search 2.x ist eine veraltete Technologie, die ursprünglich als Add-In für Windows XP und Windows Server 2003 verfügbar war. Verwenden Sie in späteren [Versionen Windows Search.](../search/-search-3x-wds-overview.md)

Die erweiterte Abfragesyntax (Advanced Query Syntax, AQS) wird von Microsoft Windows Desktop Search (WDS) verwendet, um Benutzern und Programmierern zu helfen, ihre Suchvorgänge besser zu definieren und zu verengen. Die Verwendung von AQS ist eine einfache Möglichkeit, Suchvorgänge ein- und bessere Ergebnisse zu liefern. Suchvorgänge können durch die folgenden Parameter eingeengt werden:

-   Dateiarten: Ordner, Dokumente, Präsentationen, Bilder und so weiter.
-   Dateispeicher: bestimmte Datenbanken und Speicherorte.
-   Dateieigenschaften: Größe, Datum, Titel und so weiter.
-   Dateiinhalte: Schlüsselwörter wie "Projekterstellbare", "AQS", "blaue Suede-Kinder" und so weiter.

Darüber hinaus können Suchparameter mithilfe von Suchoperatoren kombiniert werden. Im weiteren Verlauf dieses Abschnitts werden die Abfragesyntax, die Parameter und Operatoren sowie deren Kombination erläutert, um gezielte Suchergebnisse zu bieten. Die Tabellen beschreiben die Syntax, die mit WDS verwendet werden soll, sowie die  Eigenschaften, die für jede Dateiart abgefragt werden können, die im Windows Desktopsuchergebnisfenster angezeigt wird.

## <a name="desktop-search-syntax"></a>Syntax der Desktopsuche

Eine Suchabfrage kann ein oder mehrere Schlüsselwörter mit booleschen Operatoren und optionalen Kriterien enthalten. Diese optionalen Kriterien können eine Suche anhand der folgenden Kriterien einengen:

-   Bereich oder Datenspeicher, in dem sich Dateien befinden
-   Arten von Dateien
-   Verwaltete Eigenschaften von Dateien

Die optionalen Kriterien, die im Folgenden ausführlicher beschrieben werden, verwenden die folgende Syntax:

`<scope name>:<value>`

`<file kind>:<value>`

`<property name>:<value>`

Angenommen, ein Benutzer möchte nach einem Dokument suchen, das den ausdruck "letztes Quartal" enthält, der von John oder Mire erstellt wurde, und das der Benutzer im Ordner mydocuments gespeichert hat. Die Abfrage kann wie die folgende aussehen:

`"last quarter" author:(john OR joanne) foldername:mydocuments`

### <a name="scope-locations-and-data-stores"></a>Bereich: Speicherorte und Datenspeicher

Benutzer können den Bereich ihrer Suchvorgänge auf bestimmte Ordnerspeicherorte oder Datenspeicher beschränken. Wenn Sie beispielsweise mehrere E-Mail-Konten verwenden und eine Abfrage entweder auf Microsoft Outlook oder Microsoft Outlook Express beschränken möchten, können Sie bzw. `store:outlook` `store:oe` verwenden.



| Einschränken der Suche nach Store | Verwendung              | Beispiel                                  |
|-------------------------------|------------------|------------------------------------------|
| Desktop                       | Desktop          | store:desktop                            |
| Dateien                         | files            | store:files                              |
| Outlook                       | Outlook          | store:outlook                            |
| Outlook Express               | oe               | store:oe                                 |
| Bestimmter Ordner               | foldername oder in | foldername:MyDocuments oder in:MyDocuments |



 

Wenn Sie über einen Protokollhandler verfügen, um benutzerdefinierte Speicher wie Lotus Notes zu durchforsten, können Sie den Namen des Speichers oder Protokollhandlers für den Speicher verwenden. Wenn Sie z. B. einen Protokollhandler implementiert haben, der einen Lotus Notes-Datenspeicher als "Notizen" enthält, wäre die Abfragesyntax `store:notes` .

### <a name="common-file-kinds"></a>Allgemeine Dateiarten

Benutzer können ihre Suchvorgänge auch auf bestimmte Dateitypen beschränken, die als Dateiarten bezeichnet werden. In der folgenden Tabelle sind die Dateitypen und Beispiele für die Syntax aufgeführt, mit der nach diesen Arten von Dateien gesucht wird.



| So beschränken Sie nach Dateityp:       | Verwendung              | Beispiel                        |
|---------------------------------|------------------|--------------------------------|
| Alle Dateitypen                  | alles       | kind:everything                |
| Kommunikation                  | Kommunikation   | kind:communications            |
| Kontakte                        | Kontakte         | kind:contacts                  |
| E-Mail                          | email            | kind:email                     |
| Instant Messenger-Konversationen | im               | kind:im                        |
| Besprechungen                        | Sitzungen         | kind:meetings                  |
| Aufgaben                           | Tasks            | kind:tasks                     |
| Hinweise                           | notes            | kind:notes                     |
| Dokumente                       | Docs             | kind:docs                      |
| Textdokumente                  | text             | kind:text                      |
| Kalkulationstabellen                    | Tabellen     | kind:spreadsheets              |
| Präsentationen                   | Präsentationen    | kind:presentations             |
| Musik                           | music            | kind:music                     |
| Bilder                        | Bilder             | kind:pics                      |
| Videos                          | videos           | kind:videos                    |
| Ordner                         | Ordner          | kind:folders                   |
| Ordnername                     | foldername oder in | foldername:mydocs oder in:mydocs |
| Favoriten                       | Favoriten        | kind:favorites                 |
| Programme                        | Programme         | kind:programs                  |



 

### <a name="boolean-operators"></a>Boolesche Operatoren

Suchbegriffe und Dateieigenschaften können kombiniert werden, um eine Suche mit Operatoren zu erweitern oder einzugrenzen. In der folgenden Tabelle werden allgemeine Operatoren erläutert, die in einer Suchabfrage verwendet werden.



| Schlüsselwort/Symbol  | Beispiele                                              | Funktion                                                                                                       |
|-----------------|-------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| NICHT             | social NOT security<br/>                        | Sucht Nach Elementen, die *soziale Netzwerke* enthalten, aber keine *Sicherheitselemente.*<br/>                                              |
|                 | Sozialversicherung<br/>                           | Sucht Nach Elementen, die *soziale Netzwerke* und *Sicherheitselemente* enthalten.<br/>                                              |
| oder              | Social OR-Sicherheit<br/>                         | Sucht Nach Elementen, die *soziale Netzwerke* oder *Sicherheitselemente* enthalten.<br/>                                                    |
| Anführungszeichen | "Soziale Sicherheit"<br/>                          | Sucht Nach Elementen, die den genauen Ausdruck *social security* enthalten.<br/>                                        |
| Klammern     | (Sozialversicherung)<br/>                          | Sucht Nach Elementen, die *soziale Netzwerke* und *Sicherheit* in beliebiger Reihenfolge enthalten.<br/>                                      |
| >            | date:>05.11.04<br/> size:>500<br/>  | Sucht Elemente mit einem Datum nach dem 05.11.04. <br/> Sucht Elemente mit einer Größe von mehr als 500 Byte.<br/> |
| <            | date:<05.11.04 <br/> size:<500<br/> | Sucht Nach Elementen mit einem Datum vor dem 05.11.04. <br/> Sucht Elemente mit einer Größe von weniger als 500 Byte.<br/>   |
| ..              | date:11/05/04...11/10/04<br/>                    | Sucht nach Elementen mit einem Datum, das am 04.11.05 beginnt und am 10.11.04 endet.<br/>                               |



 

> [!Note]
>
> Die Operatoren **NOT** und **OR** müssen groß geschrieben sein und können nicht in einer Abfrage kombiniert werden (z. B. `social OR security NOT retirement` ).

 

### <a name="boolean-properties"></a>Boolesche Eigenschaften

Bei einigen Dateitypen können Benutzer mit booleschen Eigenschaften nach Dateien suchen, wie in der folgenden Tabelle beschrieben.



| Eigenschaft       | Beispiel                   | Funktion                                                                                                        |
|----------------|---------------------------|-----------------------------------------------------------------------------------------------------------------|
| is:attachment  | bericht is:attachment      | Sucht Nach Elementen mit Anlagen, die *Den Bericht* enthalten. Wie in `isattachment:true`.                           |
| isonline:      | bericht isonline:true      | Sucht Nach Elementen, die online sind und *Den Bericht* enthalten.                                                         |
| isrecurring:   | report isrecurring:true   | Sucht elemente, die sich wiederholen und *Berichts* enthalten.                                                       |
| isflagged:     | bericht isflagged:true     | Sucht nach Elementen, die gekennzeichnet sind (z. B. Überprüfen, Nachverfolgung) und *den Bericht* enthalten.                       |
| Isdeleted:     | bericht isdeleted:true     | Sucht nach Elementen, die als gelöscht gekennzeichnet sind (z. B. Papierkorb oder gelöschte Elemente), und die *den Bericht* enthalten. |
| Iscompleted:   | report iscompleted:false  | Sucht Nach Elementen, die nicht als vollständig gekennzeichnet sind und *den Bericht* enthalten.                                        |
| hasattachment: | report hasattachment:true | Sucht Nach Elementen, die *Berichte* enthalten und Anlagen enthalten                                                          |
| hasflag:       | report hasflag:true       | Sucht Elemente, die *Berichte* enthalten und Flags enthalten.                                                                |



 

### <a name="dates"></a>Datumsangaben

Zusätzlich zur Suche nach bestimmten Datums- und Datumsbereichen mithilfe der zuvor beschriebenen Operatoren lässt AQS relative Datumswerte (wie `today` , oder ) und `tomorrow` `next week` Tageswerte (wie `Tuesday` oder ) und `Monday..Wednesday` `February` Monatswerte () zu.



| Relativ zu:    | Syntaxbeispiel                                                                                                                         | Ergebnis                                                                                                                                                                                                                                                                                                                                                    |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tag             | date:today<br/> date:tomorrow<br/> date:yesterday<br/>                                                               | Sucht Nach Elementen mit dem heutigen Datum.<br/> Sucht Nach Elementen mit dem Datum von morgen.<br/> Sucht Nach Elementen mit dem gestrigen Datum. <br/>                                                                                                                                                                                                                     |
| Woche/Monat/Jahr | date:this week<br/> date:last week<br/> date:next month<br/> date:past month<br/> date:coming year <br/> | Sucht Elemente mit einem Datum, das innerhalb der aktuellen Woche liegen.<br/> Sucht Elemente mit einem Datum, das innerhalb der vorherigen Woche liegen.<br/> Sucht Nach Elementen mit einem Datum, das innerhalb der kommenden Woche liegen soll.<br/> Sucht Elemente mit einem Datum, das in den vorherigen Monat fällt.<br/> Sucht Elemente mit einem Datum, das innerhalb des nächsten Jahres liegen. <br/> |



 

## <a name="properties-by-file-kind"></a>Eigenschaften nach Dateiart

Benutzer können nach bestimmten Eigenschaften verschiedener Dateitypen suchen. Einige Eigenschaften (z. B. die Dateigröße) gelten für alle Dateien, während andere auf eine bestimmte Art beschränkt sind. Die Anzahl der Folien ist z. B. spezifisch für Präsentationen. In den folgenden Tabellen sind diese Eigenschaften nach Dateiart aufgeführt.

### <a name="file-kind-everything"></a>Dateiart: Alles

Dies sind Eigenschaften, die allen Dateitypen gemeinsam sind. Um alle Dateitypen in eine Abfrage einzufügen, lautet die Syntax:

`kind:everything <property>:<value>`

dabei `<property>` ist eine unten aufgeführte Eigenschaft und der vom Benutzer angegebene `<value>` Suchbegriff.



| Eigenschaft       | Verwendung                      | Beispiel                        |
|----------------|--------------------------|--------------------------------|
| Titel          | title, subject oder about  | title:"Quarterly Financial"    |
| Status         | status                   | status:complete                |
| Datum           | Datum                     | date:last week                 |
| Geändert am  | datemodified oder modified | modified:last week             |
| Wichtigkeit     | Wichtigkeit oder Priorität   | importance:high                |
| Size           | Größe                     | size:> 50                   |
| Deleted        | gelöscht oder gelöscht     | isdeleted:true                 |
| Ist anlage  | isattachment             | isattachment:true              |
| Beschreibung             | to oder toname             | to:bob                         |
| Cc             | cc oder ccname             | cc:john                        |
| Company        | company                  | company:Microsoft              |
| Standort       | location                 | location:"Conference Room 102" |
| Category       | category                 | category:Business              |
| Keywords       | keywords                 | keywords:"sales projections"   |
| Album          | Album                    | album:"Fly by Night"           |
| Dateiname      | Dateiname oder Datei         | dateiname:MyResume              |
| Genre          | genre                    | genre:rock                     |
| Autor         | autor oder von             | author:"Stephen King"          |
| Personen         | Personen oder mit           | with:(sonja oder david)          |
| Ordner         | Ordner, unter oder Pfad    | folder:downloads               |
| Dateierweiterung | ext oder fileext           | ext:.txt                       |



 

### <a name="attachment"></a>Attachment

Dies sind Eigenschaften, die Anlagen gemeinsam sind. Um die Suche nur auf Anlagen zu beschränken, lautet die Syntax:

`kind:attachment <property>:<value>`

dabei `<property>` ist eine unten aufgeführte Eigenschaft und der vom Benutzer angegebene `<value>` Suchbegriff.



| Eigenschaft | Verwendung            | Beispiel                  |
|----------|----------------|--------------------------|
| Personen   | Personen oder mit | people:john oder with:john |



 

### <a name="contacts"></a>Kontakte

Dies sind Eigenschaften, die kontaktverbreitet sind. Um die Suche nur auf Kontakte zu beschränken, lautet die Syntax:

`kind:contacts <property>:<value>`

dabei `<property>` ist eine unten aufgeführte Eigenschaft und der vom Benutzer angegebene `<value>` Suchbegriff.



| Eigenschaft              | Verwendung                 | Beispiel                            |
|-----------------------|---------------------|------------------------------------|
| Berufsbezeichnung             | jobtitle            | jobtitle:CFO                       |
| IM-Adresse            | imaddress           | imaddress:john\_doe@msn.com        |
| Telefon des Assistenten     | assistantsphone     | assistantsphone:555-3323           |
| Name des Assistenten        | Assistentname       | assistentname:Paul                 |
| Profession            | Beruf          | bei:plumber                 |
| Spitzname              | nickname            | spitzname:Tex                       |
| Ehepartner                | Ehepartner              | vor: Debbie                      |
| Geschäfts-Stadt         | businesscity        | businesscity:Seattle               |
| Geschäftliche Postleitzahl  | businesspostalcode  | businesspostalcode:98006           |
| Unternehmens-Homepage    | businesshomepage    | businesshomepage:www.microsoft.com |
| Rückruftelefonnummer | callbackphonenumber | callbackphonenumber:555-555-2121   |
| Autotelefon             | Carphone            | carphone:555-555-2121              |
| Children              | Untergeordnete            | children:Timmy                     |
| Vorname            | firstname           | firstname:John                     |
| Nachname             | lastname            | lastname:Doe                       |
| Homefax              | homefax             | homefax:555-555-2121               |
| Name des Vorgesetzten        | managername        | managersname:John                  |
| Pager                 | pager               | pager:555-555-2121                 |
| Telefon (geschäftlich)        | businessphone       | businessphone:555-555-2121         |
| Telefon (privat)            | homePhone           | homephone:555-555-2121             |
| Mobiltelefon          | Handy         | mobilephone:555-555-2121           |
| Office                | Office              | office:sample                      |
| Jahrestag           | Jahrestag         | anniversary:1/1/06                 |
| Birthday              | Geburtstag            | 06.1.2016                    |
| Webseite              | Webseite             | webseite:www.microsoft.com          |



 

> [!Note]
>
> Telefon Zahlen werden wie eingegeben indiziert. Wenn ein Benutzer z. B. bei der Eingabe der Telefonnummer keine Landes- oder Ortsvorwahl verwendet hat, können Benutzer keinen Kontakt finden, wenn er mit Länder- oder Ortsvorwahl in der Telefonnummer sucht.

 

### <a name="communications"></a>Kommunikation

Dies sind Eigenschaften, die für die Kommunikation gelten. Um die Suche auf die Kommunikation zu beschränken, ist die Syntax:

`kind:communications <property>:<value>`

dabei `<property>` ist eine unten aufgeführte Eigenschaft und der vom Benutzer angegebene `<value>` Suchbegriff.



| Eigenschaft       | Verwendung                           | Beispiel                         |
|----------------|-------------------------------|---------------------------------|
| From           | von oder Organisator             | von:john                       |
| Empfangen       | empfangen oder gesendet              | sent:yesterday                  |
| Gegenstand        | Betreff oder Titel              | betreff:"Vierteljährliche Finanzlage"   |
| Verfügt über eine Anlage | hasattachments, hasattachment | hasattachment:true              |
| Attachments    | Anlagen oder Anlagen     | attachment:presentation.ppt     |
| Bcc            | bcc, bccname oder bccaddress    | bcc:dave                        |
| CC-Adresse     | ccaddress oder cc               | ccaddress:john\_doe@outlook.com |
| Follow-up-Flag | followupflag                  | followupflag:2                  |
| Fälligkeitsdatum       | duedate oder due                | due:letzte Woche                   |
| Überwachungsdaten           | read oder isread                | is:read                         |
| Abgeschlossen   | Iscompleted                   | is:completed                    |
| Unvollständig     | incomplete oder isincomplete    | is:incomplete                   |
| Has-Flag       | hasflag oder isflagged          | has:flag                        |
| Duration       | duration                      | duration:> 50                |



 

### <a name="calendar"></a>Kalender

Dies sind Eigenschaften, die Kalendern gemeinsam sind. Um die Suche auf Kalender zu beschränken, ist die Syntax:

`kind:calendar <property>:<value>`

dabei `<property>` ist eine unten aufgeführte Eigenschaft und der vom Benutzer angegebene `<value>` Suchbegriff.



| Eigenschaft  | Verwendung                      | Beispiel          |
|-----------|--------------------------|------------------|
| Wiederholt | wiederholt oder isrecurring | is:recurring     |
| Organizer | Organisator, nach oder von    | organizer:debbie |



 

### <a name="documents"></a>Dokumente

Dies sind Eigenschaften, die für Dokumente gelten. Um die Suche nur auf Dokumente zu beschränken, ist die Syntax:

`kind:documents <property>:<value>`

dabei `<property>` ist eine unten aufgeführte Eigenschaft und der vom Benutzer angegebene `<value>` Suchbegriff.



| Eigenschaft          | Verwendung             | Beispiel                       |
|-------------------|-----------------|-------------------------------|
| Kommentare          | comments        | comments:"needs final review" |
| Zuletzt gespeichert von     | lastsavedby     | lastsavedby:john              |
| Dokument-Manager  | documentmanager | documentmanager:john          |
| Revisionsnummer   | Revisionnumber  | revisionnumber:1.0.3          |
| Dokumentformat   | documentformat  | documentformat:MIMETYPE       |
| Datum des letzten Drucks | datelastprinted | datelastprinted:letzte Woche     |



 

### <a name="presentation"></a>Präsentation

Dies sind Eigenschaften, die für Präsentationen üblich sind. Um die Suche auf Präsentationen zu beschränken, ist die Syntax:

`kind:presentation <property>:<value>`

dabei `<property>` ist eine unten aufgeführte Eigenschaft und der vom Benutzer angegebene `<value>` Suchbegriff.



| Eigenschaft    | Verwendung        | Beispiel           |
|-------------|------------|-------------------|
| Anzahl der Folien | Slidecount | slidecount:>20 |



 

### <a name="music"></a>Musik

Dies sind Eigenschaften, die musikdateien gemeinsam sind. Um die Suche nur auf Musik zu beschränken, ist die Syntax:

`kind:music <property>:<value>`

dabei `<property>` ist eine unten aufgeführte Eigenschaft und der vom Benutzer angegebene `<value>` Suchbegriff.



| Eigenschaft | Verwendung                | Beispiel                  |
|----------|--------------------|--------------------------|
| Bitrate | Bitrate, Rate      | bitrate:192              |
| Künstler   | interpret, by oder from | interpret:John John John       |
| Duration | duration           | duration:3               |
| Album    | Album              | album:"greatest hits"    |
| Genre    | genre              | genre:rock               |
| Track    | track              | track:12                 |
| Jahr     | year               | jahr:> 1980 < 1990 |



 

### <a name="picture"></a>Picture

Dies sind Eigenschaften, die bildern gemeinsam sind. Um die Suche nur auf Bilder zu beschränken, ist die Syntax:

`kind:picture <property>:<value>`

dabei `<property>` ist eine unten aufgeführte Eigenschaft und der vom Benutzer angegebene `<value>` Suchbegriff.



| Eigenschaft     | Verwendung         | Beispiel               |
|--------------|-------------|-----------------------|
| Kamera make  | cameramake  | cameramake:sample     |
| Kameramodell | cameramodel | cameramodel:sample    |
| Dimensionen   | dimensions  | Dimensionen:8X10       |
| Orientation  | orientation | orientation:landscape |
| Datum der Erstellung   | datetaken   | datetaken:yesterday   |
| Width        | width       | width:1600            |
| Height       | height      | height:1200           |



 

### <a name="video"></a>Video

Dies sind Eigenschaften, die videos gemeinsam sind. Um die Suche nur auf Videos zu beschränken, lautet die Syntax:

`kind:video <property>:<value>`

dabei `<property>` ist eine unten aufgeführte Eigenschaft und der vom Benutzer angegebene `<value>` Suchbegriff.



| Eigenschaft | Verwendung           | Beispiel                                |
|----------|---------------|----------------------------------------|
| Name     | name, subject | name:"Family Vacation to the Beach 05" |
| Durchw.      | ext, fileext  | ext:.avi                               |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Referenz**
</dt> <dt>

[Wahrgenommene Typen](-search-2x-wds-perceivedtype.md)
</dt> <dt>

[SchemaTable](-search-2x-wds-schematable.md)
</dt> <dt>

[Aufrufen von WDS über die Befehlszeile](-search-2x-wds-fromcommandline.md)
</dt> <dt>

[Aufrufen von WDS über Webseiten](-search-2x-wds-browserhelpobject.md)
</dt> </dl>

 

 





