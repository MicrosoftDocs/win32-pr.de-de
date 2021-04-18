---
title: Erweiterte Abfragesyntax
description: Die Erweiterte Abfrage Syntax (Advanced Query Syntax, AQS) wird von Microsoft Windows Desktop Search (WDS) verwendet, um Benutzern und Programmierern zu helfen, Ihre Suchvorgänge besser zu definieren und einzuschränken.
ms.assetid: 8e55bd40-c7cf-44a6-bc18-24bc7a267779
ms.topic: article
ms.date: 05/19/2020
ms.openlocfilehash: bd00821e60c8d950a7ec384b62d7ff062066f224
ms.sourcegitcommit: 8bba855bfee06d018edb16c1af70fa4d4344445b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/19/2020
ms.locfileid: "106340255"
---
# <a name="advanced-query-syntax"></a>Erweiterte Abfragesyntax

> [!NOTE]
> Windows-Desktop Suche 2. x ist eine veraltete Technologie, die ursprünglich als Add-in für Windows XP und Windows Server 2003 verfügbar war. Verwenden Sie in späteren Versionen stattdessen [Windows Search](../search/-search-3x-wds-overview.md) .

Die Erweiterte Abfrage Syntax (Advanced Query Syntax, AQS) wird von Microsoft Windows Desktop Search (WDS) verwendet, um Benutzern und Programmierern zu helfen, Ihre Suchvorgänge besser zu definieren und einzuschränken. Die Verwendung von AQS ist eine einfache Möglichkeit zum Einschränken von Such Vorgängen und Bereitstellung besserer Resultsets. Suchvorgänge können mit den folgenden Parametern eingeschränkt werden:

-   Dateitypen: Ordner, Dokumente, Präsentationen, Bilder usw.
-   Dateispeicher: bestimmte Datenbanken und Speicherorte.
-   Dateieigenschaften: Größe, Datum, Titel usw.
-   Dateiinhalt: Schlüsselwörter wie "Projektleistungen", "AQS", "Blue Suede-Schuhe" usw.

Außerdem können Suchparameter mithilfe von Such Operatoren kombiniert werden. Im restlichen Teil dieses Abschnitts werden die Abfrage Syntax, die Parameter und die Operatoren erläutert und erläutert, wie diese kombiniert werden können, um gezielte Suchergebnisse anzubieten. In den Tabellen wird die Syntax beschrieben, die mit WDS verwendet werden soll, sowie die Eigenschaften, die für die einzelnen im Fenster " **Windows-Desktop Such** Ergebnisse" angezeigten Dateitypen abgefragt werden können.

## <a name="desktop-search-syntax"></a>Syntax der Desktop Suche

Eine Suchabfrage kann ein oder mehrere Schlüsselwörter mit booleschen Operatoren und optionalen Kriterien enthalten. Diese optionalen Kriterien können eine Suche einschränken, die auf folgenden Bedingungen basiert:

-   Bereich oder Datenspeicher, in dem sich Dateien befinden
-   Arten von Dateien
-   Verwaltete Eigenschaften von Dateien

Die optionalen Kriterien, die nachfolgend ausführlicher beschrieben werden, verwenden die folgende Syntax:

`<scope name>:<value>`

`<file kind>:<value>`

`<property name>:<value>`

Angenommen, ein Benutzer möchte nach einem Dokument suchen, das den Ausdruck "Letztes Quartal" enthält, der von John oder Joanne erstellt wurde, und der Benutzer im Ordner "MyDocuments" gespeichert hat. Die Abfrage könnte wie folgt aussehen:

`"last quarter" author:(john OR joanne) foldername:mydocuments`

### <a name="scope-locations-and-data-stores"></a>Bereich: Standorte und Datenspeicher

Benutzer können den Suchbereich auf bestimmte Ordner Speicherorte oder Datenspeicher beschränken. Wenn Sie z. b. mehrere e-Mail-Konten verwenden und eine Abfrage entweder auf Microsoft Outlook oder Microsoft Outlook Express beschränken möchten, können Sie `store:outlook` oder verwenden `store:oe` .



| Einschränken der Suche nach Datenspeicher | Verwendung              | Beispiel                                  |
|-------------------------------|------------------|------------------------------------------|
| Desktop                       | Desktop          | Store: Desktop                            |
| Dateien                         | files            | Speichern: Dateien                              |
| Outlook                       | positiv          | Store: Outlook                            |
| Outlook Express               | oe               | Store: OE                                 |
| Bestimmter Ordner               | FolderName oder in | FolderName: MyDocuments oder in: MyDocuments |



 

Wenn Sie über einen Protokollhandler für die durch Forstung von benutzerdefinierten speichern verfügen (z. b. Lotus Notes), können Sie den Namen des Speichers oder Protokoll Handlers für den Speicher verwenden. Wenn Sie z. b. einen Protokollhandler implementiert haben, um einen Lotus Notes-Datenspeicher als "Notizen" einzuschließen, wäre die Abfrage Syntax `store:notes` .

### <a name="common-file-kinds"></a>Allgemeine Dateitypen

Benutzer können Ihre Suchvorgänge auch auf bestimmte Typen von Dateien beschränken, die als Dateitypen bezeichnet werden. In der folgenden Tabelle sind die Dateitypen und Beispiele für die Syntax aufgeführt, die für die Suche nach diesen Arten von Dateien verwendet wird.



| So schränken Sie den Dateityp ein:       | Verwendung              | Beispiel                        |
|---------------------------------|------------------|--------------------------------|
| Alle Dateitypen                  | alles       | Art: alles                |
| Kommunikation                  | Kommunikation   | Art: Kommunikation            |
| Kontakte                        | Kontakte         | Art: Kontakte                  |
| E-Mail                          | email            | Art: e-Mail                     |
| Instant Messenger-Gespräche | im               | Art: im                        |
| Besprechungen                        | t         | Art: Besprechungen                  |
| Aufgaben                           | Tasks            | Art: Aufgaben                     |
| Notizen                           | notes            | Kind: Hinweise                     |
| Dokumente                       | Docs             | Kind: docs                      |
| Text Dokumente                  | text             | Art: Text                      |
| Kalkulationstabellen                    | Tabellen     | Kind: Kalkulations Tabellen              |
| Präsentationen                   | Präsentationen    | Art: Präsentationen             |
| Musik                           | music            | Art: Musik                     |
| Bilder                        | Seht             | Kind: Bilder                      |
| Videos                          | videos           | Art: Videos                    |
| Ordner                         | Ordner          | Art: Ordner                   |
| Ordnername                     | FolderName oder in | FolderName: MyDocs oder in: MyDocs |
| Favoriten                       | Favoriten        | Kind: Favoriten                 |
| Programs                        | Programme         | Art: Programme                  |



 

### <a name="boolean-operators"></a>Boolesche Operatoren

Such Schlüsselwörter und Dateieigenschaften können kombiniert werden, um eine Suche mit Operatoren zu erweitern oder einzuschränken. In der folgenden Tabelle werden allgemeine Operatoren erläutert, die in einer Suchabfrage verwendet werden.



| Schlüsselwort/Symbol  | Beispiele                                              | Funktion                                                                                                       |
|-----------------|-------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| NICHT             | soziale Sicherheit, nicht Sicherheit<br/>                        | Sucht Elemente, die *soziale* Netzwerke enthalten, aber keine *Sicherheit*.<br/>                                              |
|                 | soziale Sicherheit<br/>                           | Sucht nach Elementen, die *Social* und *Security* enthalten.<br/>                                              |
| oder              | soziale Netzwerke oder Sicherheit<br/>                         | Sucht nach Elementen, die *Social* oder *Security* enthalten.<br/>                                                    |
| Anführungszeichen | "soziale Sicherheit"<br/>                          | Sucht nach Elementen, die den exakten Ausdruck für *soziale Sicherheit* enthalten.<br/>                                        |
| Klammern     | (soziale Sicherheit)<br/>                          | Sucht nach Elementen, die in beliebiger Reihenfolge *soziale* und *Sicherheits* Elemente enthalten.<br/>                                      |
| >            | Datum: >11/05/04<br/> Größe: >500<br/>  | Sucht nach Elementen mit einem Datum nach 11/05/04. <br/> Sucht nach Elementen mit einer Größe von mehr als 500 Bytes.<br/> |
| <            | Datum: <11/05/04 <br/> Größe: <500<br/> | Sucht nach Elementen mit einem Datum vor 11/05/04. <br/> Sucht nach Elementen mit einer Größe von weniger als 500 Bytes.<br/>   |
| ..              | Datum: 11/05/04.. 11/10/04<br/>                    | Findet Elemente mit einem Datum, das am 11/05/04 beginnt und auf 11/10/04 endet.<br/>                               |



 

> [!Note]
>
> Die Operatoren **Not** and **or** müssen in Großbuchstaben angegeben werden und können nicht in einer Abfrage (z. b.) kombiniert werden `social OR security NOT retirement` .

 

### <a name="boolean-properties"></a>Boolesche Eigenschaften

Einige Dateitypen ermöglichen Benutzern das Suchen nach Dateien mithilfe von booleschen Eigenschaften, wie in der folgenden Tabelle beschrieben.



| Eigenschaft       | Beispiel                   | Funktion                                                                                                        |
|----------------|---------------------------|-----------------------------------------------------------------------------------------------------------------|
| ist: Anhang  | Bericht ist: Anlage      | Sucht nach Elementen, die Anhänge enthalten, die einen *Bericht* enthalten. Wie in `isattachment:true`.                           |
| IsOnline:      | Bericht IsOnline: true      | Sucht nach Elementen, die Online sind und *Berichte* enthalten.                                                         |
| isperiodisch:   | Bericht "isperiodisch": true   | Sucht nach Elementen, die sich wiederholt und die *Berichte* enthalten.                                                       |
| isflaging:     | Report isflaging: true     | Sucht nach Elementen, die gekennzeichnet sind (z. b. überprüfen, Nachverfolgung) und die einen *Bericht* enthalten.                       |
| isDeleted     | Bericht "isDeleted": true     | Sucht nach Elementen, die als gelöscht gekennzeichnet sind (z. b. Papierkorb oder gelöschte Elemente) und die einen *Bericht* enthalten. |
| IsCompleted   | Bericht "isabgeschlossen": false  | Sucht Elemente, die nicht als "Complete" gekennzeichnet sind und einen *Bericht* enthalten.                                        |
| HasAttachment: | berichtshasattachment: true | Sucht Elemente, die einen *Bericht* enthalten und über Anlagen verfügen.                                                          |
| hasflag       | berichtshasflag: true       | Sucht Elemente, die den *Bericht* enthalten und über Flags verfügen.                                                                |



 

### <a name="dates"></a>Datumsangaben

Neben der Suche nach bestimmten Datums-und Datumsbereichen mithilfe der zuvor beschriebenen Operatoren werden in AQS relative Datumswerte ( `today` z `tomorrow` . b.,, oder `next week` ) und die Werte für den Tag (wie `Tuesday` oder `Monday..Wednesday` ) und Month ( `February` ) ermöglicht.



| Relativ zu:    | Syntax Beispiel                                                                                                                         | Ergebnis                                                                                                                                                                                                                                                                                                                                                    |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tag             | Datum: heute<br/> Datum: Morgen<br/> Datum: Gestern<br/>                                                               | Sucht nach Elementen mit dem heutigen Datum.<br/> Sucht nach Elementen mit dem Morgen.<br/> Sucht nach Elementen mit dem gestrigen Datum. <br/>                                                                                                                                                                                                                     |
| Woche/Monat/Jahr | Datum: diese Woche<br/> Datum: Letzte Woche<br/> Datum: nächster Monat<br/> Datum: vergangener Monat<br/> Datum: das kommende Jahr <br/> | Findet Elemente mit einem Datum, das innerhalb der aktuellen Woche liegt.<br/> Findet Elemente mit einem Datum, das in der vorherigen Woche liegt.<br/> Findet Elemente mit einem Datum, das innerhalb der bevorstehenden Woche liegt.<br/> Findet Elemente mit einem Datum, das innerhalb des vorherigen Monats liegt.<br/> Sucht nach Elementen mit einem Datum, das in das bevorstehende Jahr fällt. <br/> |



 

## <a name="properties-by-file-kind"></a>Eigenschaften nach Dateiart

Benutzer können nach bestimmten Eigenschaften verschiedener Dateiarten suchen. Einige Eigenschaften (z. b. die Dateigröße) sind für alle Dateien üblich, während andere auf eine bestimmte Art beschränkt sind. Die Folien Anzahl ist beispielsweise spezifisch für Präsentationen. In den folgenden Tabellen sind diese Eigenschaften nach Dateiart aufgelistet.

### <a name="file-kind-everything"></a>Dateiart: alles

Dabei handelt es sich um Eigenschaften, die allen Dateitypen gemeinsam sind. Wenn Sie alle Dateitypen in eine Abfrage einschließen möchten, lautet die Syntax wie folgt:

`kind:everything <property>:<value>`

dabei `<property>` ist eine Eigenschaft, die unten aufgeführt ist, und `<value>` ist der vom Benutzer angegebene Suchbegriff.



| Eigenschaft       | Verwendung                      | Beispiel                        |
|----------------|--------------------------|--------------------------------|
| Titel          | Titel, Betreff oder info  | Title: "Quartals Finanz"    |
| Status         | status                   | Status: Fertigstellen                |
| Datum           | Datum                     | Datum: Letzte Woche                 |
| Geändert am  | DateModified oder modified | geändert: Letzte Woche             |
| Wichtigkeit     | Wichtigkeit oder Priorität   | Wichtigkeit: hoch                |
| Size           | Größe                     | Größe: > 50                   |
| Deleted        | gelöscht oder isDeleted     | IsDeleted: true                 |
| Ist Anhang  | isattachment             | isattachment: true              |
| Beschreibung             | zu oder ToName             | an: Bob                         |
| Cc             | CC oder ccname             | cc: John                        |
| Company        | company                  | Unternehmen: Microsoft              |
| Standort       | location                 | Standort: "Konferenzraum 102" |
| Category       | category                 | Kategorie: Business              |
| Keywords       | keywords                 | Schlüsselwörter: "Sales Projektionen"   |
| Aufzunehmen          | aufzunehmen                    | Album: "Fly by Nacht"           |
| Dateiname      | Dateiname oder Datei         | Dateiname: myresume              |
| Genre          | genre                    | Genre: Rock                     |
| Autor         | Autor oder durch             | Autor: "Stephen King"          |
| Personen         | Personen oder mit           | mit: (Sonja oder David)          |
| Ordner         | Ordner, unter oder Pfad    | Ordner: Downloads               |
| Dateierweiterung | ext oder fileext           | ext:.txt                       |



 

### <a name="attachment"></a>Attachment

Dies sind die Eigenschaften, die Anlagen gemeinsam haben. Um die Suche nur auf Anlagen einzuschränken, lautet die Syntax wie folgt:

`kind:attachment <property>:<value>`

dabei `<property>` ist eine Eigenschaft, die unten aufgeführt ist, und `<value>` ist der vom Benutzer angegebene Suchbegriff.



| Eigenschaft | Verwendung            | Beispiel                  |
|----------|----------------|--------------------------|
| Personen   | Personen oder mit | Personen: John oder mit: John |



 

### <a name="contacts"></a>Kontakte

Dies sind Eigenschaften, die von Kontakten gemeinsam sind. Um die Suche nur auf Kontakte zu beschränken, lautet die Syntax wie folgt:

`kind:contacts <property>:<value>`

dabei `<property>` ist eine Eigenschaft, die unten aufgeführt ist, und `<value>` ist der vom Benutzer angegebene Suchbegriff.



| Eigenschaft              | Verwendung                 | Beispiel                            |
|-----------------------|---------------------|------------------------------------|
| Berufsbezeichnung             | jobtitle            | JobTitle: CFO                       |
| IM-Adresse            | IMAddress           | IMAddress: John\_doe@msn.com        |
| Telefon des Assistenten     | assistantsphone     | assistantsphone: 555-3323           |
| Name des Assistenten        | AssistantName       | AssistantName: Paul                 |
| Profession            | Arzt          | Beruf: Plumber                 |
| Spitzname              | nickname            | Spitzname: TeX                       |
| Gat                | Gat              | Ehepartner: Debbie                      |
| Geschäftstadt         | businesscity        | businesscity: Seattle               |
| Geschäftliche Postleitzahl  | businesspostalcode  | businesspostalcode: 98006           |
| Business-Homepage    | BusinessHomePage    | BusinessHomePage:www. Microsoft. com |
| Rückruf Telefonnummer | callbackphonenumber | callbackphonenumber: 555-555-2121   |
| Mobiltelefon             | Carphone            | Carphone: 555-555-2121              |
| Children              | Untergeordnete            | untergeordnete Elemente: Timmy                     |
| Vorname            | firstname           | FirstName: John                     |
| Nachname             | lastname            | LastName: Doe                       |
| Faxgerät              | homefax             | homefax: 555-555-2121               |
| Name des Managers        | managersname        | managersname: John                  |
| Pager                 | pager               | Pager: 555-555-2121                 |
| Telefon (geschäftlich)        | Karte Businessphone erscheint       | Businessphone: 555-555-2121         |
| Telefon (privat)            | homePhone           | HomePhone: 555-555-2121             |
| Mobiltelefon          | MobilePhone         | MobilePhone: 555-555-2121           |
| Office                | Office              | Office: Beispiel                      |
| Jahr           | Jahr         | Jahrestag: 1/1/06                 |
| Birthday              | geschenkt            | Geburtstag: 1/1/06                    |
| Webseite              | Rewards             | Webseite:www. Microsoft. com          |



 

> [!Note]
>
> Telefonnummern werden als eingegeben indiziert. Wenn ein Benutzer beispielsweise bei der Eingabe der Telefonnummer keinen Länder-oder flächencode enthielt, können Benutzer keinen Kontakt finden, wenn Sie in der Telefonnummer nach Land oder Region-Code suchen.

 

### <a name="communications"></a>Kommunikation

Dies sind die Eigenschaften, die für die Kommunikation üblich sind. Um die Suche nur auf die Kommunikation einzuschränken, lautet die Syntax wie folgt:

`kind:communications <property>:<value>`

dabei `<property>` ist eine Eigenschaft, die unten aufgeführt ist, und `<value>` ist der vom Benutzer angegebene Suchbegriff.



| Eigenschaft       | Verwendung                           | Beispiel                         |
|----------------|-------------------------------|---------------------------------|
| From           | from-oder-Planer             | von: John                       |
| Empfangen       | empfangen oder gesendet              | gesendet: Gestern                  |
| Subject        | Betreff oder Titel              | Betreff: "Quartals Finanz"   |
| Hat Anlage | hasattachments, HasAttachment | HasAttachment: true              |
| Attachments    | Anlagen oder Anlage     | attachment:presentation.ppt     |
| Bcc            | BCC, bccname oder bccaddress    | BCC: Dave                        |
| CC-Adresse     | ccAddress oder CC               | ccAddress: John\_doe@outlook.com |
| Flag für die Nachverfolgung | Follow-PFLAG                  | Follow-PFLAG: 2                  |
| Fälligkeitsdatum       | DueDate oder Due                | Due: Letzte Woche                   |
| Lesen           | Lesen oder isread                | ist: Lesen                         |
| Ist abgeschlossen   | IsCompleted                   | ist: abgeschlossen                    |
| Unvollständig     | unvollständig oder isincomplete    | ist: unvollständig                   |
| Has-Flag       | hasflag oder isflaging          | has:-Flag                        |
| Duration       | duration                      | Dauer: > 50                |



 

### <a name="calendar"></a>Kalender

Dies sind die Eigenschaften, die Kalender gemeinsam sind. Um die Suche nur auf Kalender einzuschränken, lautet die Syntax wie folgt:

`kind:calendar <property>:<value>`

dabei `<property>` ist eine Eigenschaft, die unten aufgeführt ist, und `<value>` ist der vom Benutzer angegebene Suchbegriff.



| Eigenschaft  | Verwendung                      | Beispiel          |
|-----------|--------------------------|------------------|
| Wiederholt | wiederkehrende oder iswiederkehr Ende | ist: Wiederholung     |
| Organizer | Planer, von oder von    | Planer: Debbie |



 

### <a name="documents"></a>Dokumente

Dies sind die Eigenschaften, die von Dokumenten gemeinsam sind. Um die Suche nur auf Dokumente einzuschränken, lautet die Syntax wie folgt:

`kind:documents <property>:<value>`

dabei `<property>` ist eine Eigenschaft, die unten aufgeführt ist, und `<value>` ist der vom Benutzer angegebene Suchbegriff.



| Eigenschaft          | Verwendung             | Beispiel                       |
|-------------------|-----------------|-------------------------------|
| Kommentare          | comments        | Kommentare: "erfordert abschließende Überprüfung" |
| Zuletzt gespeichert von     | LastSavedBy     | LastSavedBy: John              |
| Dokument-Manager  | documentmanager enthält | documentmanager: John          |
| Revisionsnummer   | RevisionNumber  | Revisionsnummer: 1.0.3          |
| Dokumentformat   | documentformat  | documentformat: MimeType       |
| Datum der letzten Druckausgabe | datelastprint | datelastprint: Letzte Woche     |



 

### <a name="presentation"></a>Präsentation

Dies sind Eigenschaften, die von Präsentationen gemeinsam sind. Um die Suche nur auf Präsentationen einzuschränken, lautet die Syntax wie folgt:

`kind:presentation <property>:<value>`

dabei `<property>` ist eine Eigenschaft, die unten aufgeführt ist, und `<value>` ist der vom Benutzer angegebene Suchbegriff.



| Eigenschaft    | Verwendung        | Beispiel           |
|-------------|------------|-------------------|
| Folien Anzahl | Anzahl von diasas | Anzahl von diasas: >20 |



 

### <a name="music"></a>Musik

Dies sind Eigenschaften, die von Musikdateien gemeinsam sind. Um die Suche nur auf Musik einzuschränken, lautet die Syntax wie folgt:

`kind:music <property>:<value>`

dabei `<property>` ist eine Eigenschaft, die unten aufgeführt ist, und `<value>` ist der vom Benutzer angegebene Suchbegriff.



| Eigenschaft | Verwendung                | Beispiel                  |
|----------|--------------------|--------------------------|
| Bitrate | Bitrate, Rate      | Bitrate: 192              |
| Interpret   | Künstlerin, von oder von | Künstlerin: John Sänger       |
| Duration | duration           | Dauer: 3               |
| Aufzunehmen    | aufzunehmen              | Album: "größte Treffer"    |
| Genre    | genre              | Genre: Rock               |
| Track    | track              | Nachverfolgung: 12                 |
| Year     | year               | Jahr: > 1980 < 1990 |



 

### <a name="picture"></a>Picture

Dies sind Eigenschaften, die von Bildern gemeinsam sind. Um die Suche nur auf Bilder einzuschränken, lautet die Syntax wie folgt:

`kind:picture <property>:<value>`

dabei `<property>` ist eine Eigenschaft, die unten aufgeführt ist, und `<value>` ist der vom Benutzer angegebene Suchbegriff.



| Eigenschaft     | Verwendung         | Beispiel               |
|--------------|-------------|-----------------------|
| Kamera machen  | cameramake  | cameramake: Beispiel     |
| Kameramodell | CameraModel | CameraModel: Beispiel    |
| Dimensionen   | dimensions  | Dimensionen: 8x10       |
| Orientation  | orientation | Ausrichtung: Querformat |
| Datum der Erstellung   | DateTaken   | DateTaken: Gestern   |
| Breite        | width       | Breite: 1600            |
| Höhe       | height      | Höhe: 1200           |



 

### <a name="video"></a>Video

Dies sind Eigenschaften, die von Videos gemeinsam sind. Um die Suche nur auf Videos einzuschränken, lautet die Syntax wie folgt:

`kind:video <property>:<value>`

dabei `<property>` ist eine Eigenschaft, die unten aufgeführt ist, und `<value>` ist der vom Benutzer angegebene Suchbegriff.



| Eigenschaft | Verwendung           | Beispiel                                |
|----------|---------------|----------------------------------------|
| Name     | Name, Betreff | Name: "Family Vacation to the Beach 05" |
| Durchw.      | ext, fileext  | ext:.avi                               |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Referenz**
</dt> <dt>

[Wahrgenommene Typen](-search-2x-wds-perceivedtype.md)
</dt> <dt>

[Schema Tabelle](-search-2x-wds-schematable.md)
</dt> <dt>

[Aufrufen von WDS über die Befehlszeile](-search-2x-wds-fromcommandline.md)
</dt> <dt>

[Aufrufen von WDS von Webseiten](-search-2x-wds-browserhelpobject.md)
</dt> </dl>

 

 





