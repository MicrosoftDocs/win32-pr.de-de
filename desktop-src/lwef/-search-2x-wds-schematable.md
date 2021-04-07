---
title: Schema (Features der Legacy-Windows-Umgebung)
description: Das Schema dokumentiert die Werte und Eigenschaften, die der Index zum Speichern von Daten für die Indizierung oder Sortierung verwendet.
ms.assetid: dfd8862c-8f84-441e-a4b4-4af3c76c48f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a122959b007ba4d4434e65b53fc2e330857cafe
ms.sourcegitcommit: b9a94cea8f83153214af4c09509e1cc61a1bb616
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/19/2020
ms.locfileid: "104038661"
---
# <a name="schema"></a>Schema

> [!NOTE]
> Windows-Desktop Suche 2. x ist eine veraltete Technologie, die ursprünglich als Add-in für Windows XP und Windows Server 2003 verfügbar war. Verwenden Sie in späteren Versionen stattdessen [Windows Search](../search/-search-3x-wds-overview.md) .

Das Schema dokumentiert die Werte und Eigenschaften, die der Index zum Speichern von Daten für die Indizierung oder Sortierung verwendet. In der Schema Tabelle werden die Spalten und ihre Eigenschaften (Typ und PROPID) aufgelistet, die im Schema für die Microsoft Windows-Desktop Suche (WDS) 2.6.5 enthalten sind.

## <a name="schema"></a>Schema



| Spaltenname                  | Beschreibung                                                                                                             | PROPID                                                            |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| DocComments                  | Kommentare                                                                                                                | F29F85E0-4FF9-1068-AB91-08002B27B3D9/6                            |
| Erstellen                       | Datum und Uhrzeit der Dateierstellung                                                                                      | B725F130-47EF-101A-A5F1-02608C9EEBAC/15                           |
| DisplayFolder                | Benutzerfreundlicher Ordner für Element                                                                                           | D5CDD505-2E9C-101B-9397-08002B2CF9AE/DisplayFolder                |
| DocAuthor                    | Autor des Dokuments                                                                                                  | F29F85E0-4FF9-1068-AB91-08002B27B3D9/4                            |
| DocCategory                  | Category                                                                                                                | D5CDD502-2E9C-101B-9397-08002B2CF9AE/2                            |
| Dockeywords                  | Keywords                                                                                                                | F29F85E0-4FF9-1068-AB91-08002B27B3D9/5                            |
| Doctitleprefix               | Präfix des Subjekts (Re:, FW: usw.)                                                                                      | D5CDD505-2E9C-101B-9397-08002B2CF9AE/doctitleprefix               |
| DocTitle                     | Titel                                                                                                                   | F29F85E0-4FF9-1068-AB91-08002B27B3D9/2                            |
| Fileextde                  | Benutzerfreundliche Beschreibung des Dateityps aus der Registrierung (Beispiel:. PSQ--> Product Studio-Abfrage Datei)                | D5CDD505-2E9C-101B-9397-08002B2CF9AE/fileextde                  |
| FolderName                   | Name des übergeordneten Ordners                                                                                               | D5CDD505-2E9C-101B-9397-08002B2CF9AE/FolderName                   |
| Isattachment                 | Gibt an, dass Element eine Anlage ist                                                                                         | D5CDD505-2E9C-101B-9397-08002B2CF9AE/isattachment                 |
| isDeleted                    | Gibt an, dass das Element zum Löschen markiert ist (Papierkorb, gelöschte Elemente usw.).                                                | D5CDD505-2E9C-101B-9397-08002B2CF9AE/isDeleted                    |
| Lastansicht                   | Datum, an dem das Element zuletzt vom Benutzer angezeigt wurde                                                                                   | D5CDD505-2E9C-101B-9397-08002B2CF9AE/lastansicht                   |
| Personen                       | Personen, die an diesem Element beteiligt sind                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/Personen                       |
| Wahrnehmungstyp                | Wahrnehmvedtype des Objekt Hinweises: Dies dient nur zum Abrufen.                                                           | D5CDD505-2E9C-101B-9397-08002B2CF9AE/wahrnehmvedtype                |
| Wahrnehmvetypname            | Anzeige Name von "wahrnehmvedtype".Niemals angezeigt oder abgefragt                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/wahrnehmvedty-Name            |
| Primarydate                  | Interessantesten Datumsangaben (Letzter Schreib Zeitpunkt für Dateien, empfangene Daten für e-Mail)                                              | D5CDD505-2E9C-101B-9397-08002B2CF9AE/primarydate                  |
| Size                         | Größe einer Datei.                                                                                                         | B725F130-47EF-101A-A5F1-02608C9EEBAC/12                           |
| DocSubject                   | Betreff der Datei. Hinweis: Derzeit sind e-Mail-betrefffächer heute primarytitle zugeordnet und werden aufgrund ihrer Länge nicht dupliziert. | F29F85E0-4FF9-1068-AB91-08002B27B3D9/3                            |
| URL                          | Abfrage basierte URL                                                                                                         | 49691c90-7e17-101A-a91c-08002b2ecda9/9                            |
| Schreiben                        | Datum und Uhrzeit des letzten Schreibzugriffs auf die Datei                                                                             | B725F130-47EF-101A-A5F1-02608C9EEBAC/14                           |
| DueDate                      | Fälligkeitsdatum eines Elements                                                                                                     | D5CDD505-2E9C-101B-9397-08002B2CF9AE/DueDate                      |
| Isincomplete                 | Gibt an, dass das Element nicht voll verfügbar ist                                                                                   | D5CDD505-2E9C-101B-9397-08002B2CF9AE/isincomplete                 |
| Isflaggedabgeschlossen           | Gibt an, dass das Element als abgeschlossen gekennzeichnet ist.                                                                                  | D5CDD505-2E9C-101B-9397-08002B2CF9AE/isflaggedabgeschlossen           |
| Isflag                    | Gibt an, dass das Element gekennzeichnet ist                                                                                               | D5CDD505-2E9C-101B-9397-08002B2CF9AE/isflag                    |
| Flagtext                     | Der für das Flag angezeigte Text, z. b. Review, Nachverfolgung usw.                                                              | D5CDD505-2E9C-101B-9397-08002B2CF9AE/flagtext                     |
| Identity                     | Identität für OE-Benutzer                                                                                                   | D5CDD505-2E9C-101B-9397-08002B2CF9AE/Identität                     |
| IsRead                       | Gibt an, dass das Element gelesen wurde                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/isread                       |
| Wichtigkeit                   | MAPI-Wichtigkeit oder Priorität                                                                                             | D5CDD505-2E9C-101B-9397-08002B2CF9AE/Wichtigkeit                   |
| Containerhash                | Hashcode, der die zu löschenden Anhänge anhand einer gemeinsamen Container-URL identifiziert                                     | D5CDD505-2E9C-101B-9397-08002B2CF9AE/containerhash                |
| Docformat                    | Dokumentformat oder mimetype (z. b. "Message/RFC822" für eine EML-Datei)                                              | 0b63e350-9ccc-11D0-bcdb-00805f ccce04/5                            |
| Gathertimemodified           | Zeitpunkt, zu dem der Indexer das Dokument zuletzt für die Katalog Aktualisierung durchsucht                                                           | 0b63e350-9ccc-11D0-bcdb-00805f ccce04/4                            |
| Speicher                        | Der Speicher-oder Protokollhandler (File, Mail, OutlookExpress)                                                              | D5CDD505-2E9C-101B-9397-08002B2CF9AE/Store                        |
| Fileext                      | Dateierweiterung                                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/fileext                      |
| FileName                     | Der Name der Datei.                                                                                                        | B725F130-47EF-101A-A5F1-02608C9EEBAC/10                           |
| ShortName                    | Kurzname (8,3) der Datei.                                                                                      | B725F130-47EF-101A-A5F1-02608C9EEBAC/20                           |
| Attachmentnames              | Namen von Anlagen in einer Nachricht                                                                                       | D5CDD505-2E9C-101B-9397-08002B2CF9AE/attachmentnames              |
| Bccaddress                   | Adressen in Bcc: Field                                                                                                 | D5CDD505-2E9C-101B-9397-08002B2CF9AE/bccaddress                   |
| Bccname                      | Personennamen in Bcc: Field                                                                                              | D5CDD505-2E9C-101B-9397-08002B2CF9AE/bccname                      |
| CcAddress                    | Adressen in cc: Field                                                                                                  | D5CDD505-2E9C-101B-9397-08002B2CF9AE/ccAddress                    |
| Ccname                       | Personennamen in cc: Field                                                                                               | D5CDD505-2E9C-101B-9397-08002B2CF9AE/ccname                       |
| Konverationid               | Eindeutige ID für eine Konversation in e-Mail-Threads                                                                           | D5CDD505-2E9C-101B-9397-08002B2CF9AE/ConversationId               |
| FromAddress                  | Adressen in aus: Feld                                                                                                | D5CDD505-2E9C-101B-9397-08002B2CF9AE/FromAddress                  |
| FromName                     | Personen Name in from: Field                                                                                              | D5CDD505-2E9C-101B-9397-08002B2CF9AE/FromName                     |
| "F"                      | Gibt an, dass die e-Mail an oder weitergeleitet wurde (cdopr \_ Action = 261 262).                                                      | D5CDD505-2E9C-101B-9397-08002B2CF9AE/f                      |
| Hasattach                    | Gibt an, dass die e-Mail eine Anlage hat (T oder F).                                                                               | D5CDD505-2E9C-101B-9397-08002B2CF9AE/hasattach                    |
| ReceivedDate                 | Übermittlungszeit                                                                                                           | D5CDD505-2E9C-101B-9397-08002B2CF9AE/receiveddate                 |
| ToAddress                    | Adressen im Feld:                                                                                                  | D5CDD505-2E9C-101B-9397-08002B2CF9AE/Adresse                    |
| ToName                       | Personennamen in: Feld                                                                                               | D5CDD505-2E9C-101B-9397-08002B2CF9AE/ToName                       |
| TaskStatus                   | Status einer Aufgabe                                                                                                        | D5CDD505-2E9C-101B-9397-08002B2CF9AE/Taskstatus                   |
| EndDate                      | Endzeit (in der Regel für Besprechungen/Ereignisse)                                                                                  | D5CDD505-2E9C-101B-9397-08002B2CF9AE/EndDate                      |
| Isperiodisch                  | Gibt an, dass das Element wiederholt wird (z.b. Besprechungen).                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/isperiodisch                  |
| StartDate                    | Startzeit (in der Regel für Besprechungen/Ereignisse)                                                                                | D5CDD505-2E9C-101B-9397-08002B2CF9AE/StartDate                    |
| Duration                     | Dauer der Besprechung in Minuten                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/Dauer                     |
| Standort                     | Speicherort, an dem das Element (z.b. eine Besprechung) auftritt                                                                             | D5CDD505-2E9C-101B-9397-08002B2CF9AE/Speicherort                     |
| Jahr                  | Jahrestag                                                                                                        | D5CDD505-2E9C-101B-9397-08002B2CF9AE/Jahrestag                  |
| AssistantName                | Name des Assistenten                                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/AssistantName                |
| Assistanttelephone           | Assistant-Telefon                                                                                                     | D5CDD505-2E9C-101B-9397-08002B2CF9AE/assistanttelephone           |
| Birthday                     | Geburtstag des Kontakts                                                                                                     | D5CDD505-2E9C-101B-9397-08002B2CF9AE/Geburtstag                     |
| BusinessAddressCity          | Informationen zur Unternehmens Adresse                                                                                                   | D5CDD505-2E9C-101B-9397-08002B2CF9AE/BusinessAddressCity          |
| Businessadresssspostalcode    | Informationen zur Unternehmens Adresse                                                                                                   | D5CDD505-2E9C-101B-9397-08002B2CF9AE/businessadresspostalcode    |
| Businessadresspostofficebox | Informationen zur Unternehmens Adresse                                                                                                   | D5CDD505-2E9C-101B-9397-08002B2CF9AE/businessadresssspostofficebox |
| BusinessAddressState         | Informationen zur Unternehmens Adresse                                                                                                   | D5CDD505-2E9C-101B-9397-08002B2CF9AE/BusinessAddressState         |
| Businessaddressstreet        | Informationen zur Unternehmens Adresse                                                                                                   | D5CDD505-2E9C-101B-9397-08002B2CF9AE/businessaddressstraße        |
| BusinessAddressCountry       | Informationen zur Unternehmens Adresse                                                                                                   | D5CDD505-2E9C-101B-9397-08002B2CF9AE/BusinessAddressCountry       |
| Callbacktelefon            | Rückruf telefoninfo                                                                                                | D5CDD505-2E9C-101B-9397-08002B2CF9AE/callbacktelefon            |
| Telefonisch                 | Telefon Informationen                                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/Telefonnummer                 |
| Children                     | Namen der Kinder für den Kontakt                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/untergeordnete Elemente                     |
| Companymaintelefon         | Telefon Informationen                                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/companymaintelefon         |
| EmailAddress                 | Kontakt-e-Mail                                                                                                      | D5CDD505-2E9C-101B-9397-08002B2CF9AE/EmailAddress                 |
| Emailname                    | Anzeige Name für e-Mail-Adresse                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/emailname                    |
| FirstName                    | Vorname des Kontakts                                                                                                    | D5CDD505-2E9C-101B-9397-08002B2CF9AE/FirstName                    |
| FullName                     | Vollständiger Name des Kontakts                                                                                                     | D5CDD505-2E9C-101B-9397-08002B2CF9AE/FullName                     |
| Geschlecht                       | Männlich/weiblich/andere                                                                                                       | D5CDD505-2E9C-101B-9397-08002B2CF9AE/Geschlecht                       |
| Hobby                        | Kontaktinformationen                                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/Hobby                        |
| HomeAddressCity              | Privat Adressinformationen                                                                                                       | D5CDD505-2E9C-101B-9397-08002B2CF9AE/HomeAddressCity              |
| HomeAddressCountry           | Privat Adressinformationen                                                                                                       | D5CDD505-2E9C-101B-9397-08002B2CF9AE/HomeAddressCountry           |
| Homeadresspostalcode        | Privat Adressinformationen                                                                                                       | D5CDD505-2E9C-101B-9397-08002B2CF9AE/homeadresspostalcode        |
| HomeAddressState             | Privat Adressinformationen                                                                                                       | D5CDD505-2E9C-101B-9397-08002B2CF9AE/HomeAddressState             |
| HomeAddressStreet            | Privat Adressinformationen                                                                                                       | D5CDD505-2E9C-101B-9397-08002B2CF9AE/homeaddressstraße            |
| Homefaxnummer                | Informationen zum Fax                                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/homefaxnummer                |
| Businessfaxnummer            | Informationen zum Fax                                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/businessfaxnummer            |
| HomeTelephone                | Telefon Informationen                                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/homeTelephone                |
| IMAddress                    | Sofortnachrichten Informationen                                                                                                    | D5CDD505-2E9C-101B-9397-08002B2CF9AE/IMAddress                    |
| JobTitle                     | Berufsbezeichnung des Kontakts                                                                                                     | D5CDD505-2E9C-101B-9397-08002B2CF9AE/JobTitle                     |
| MiddleName                   | Kontaktinformationen                                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/MiddleName                   |
| Mobiletelefon              | Telefon Informationen                                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/Mobiletelefon              |
| NickName                     | Kontaktinformationen                                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/Spitzname                     |
| Office                       | Kontaktinformationen                                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/Office                       |
| Officetelephone              | Telefon Informationen                                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/officetelephone              |
| PagerTelephone               | Telefon Informationen                                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/PagerTelephone               |
| LastName                     | Kontaktinformationen                                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/LastName                     |
| Personal Titel                | Berufsbezeichnung (Dr., Mr., Mrs., ms.)                                                                                  | D5CDD505-2E9C-101B-9397-08002B2CF9AE/Personal Titel                |
| Primarytelefon             | Telefon Informationen                                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/primarytelefon             |
| Profession                   | Kontaktinformationen                                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/Beruf                   |
| Gat                       | Kontaktinformationen                                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/Ehepartner                       |
| Suffix                       | Kontaktinformationen                                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/Suffix                       |
| Telexnumber                  | Telex-Informationen                                                                                                              | D5CDD505-2E9C-101B-9397-08002B2CF9AE/telexnumber                  |
| Ttytddtelefon              | TTY/TDD-Informationen                                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/ttytddtelefon              |
| WebPage                      | Webseite kontaktieren                                                                                                        | D5CDD505-2E9C-101B-9397-08002B2CF9AE/Webseite                      |
| Doccompany                   | Company                                                                                                                 | D5CDD502-2E9C-101B-9397-08002B2CF9AE/15                           |
| DocLastAuthor                | Benutzer, der zuletzt von der doc-WA gespeichert wurde                                                                                           | F29F85E0-4FF9-1068-AB91-08002B27B3D9/8                            |
| DOCLASTPRINT               | Zuletzt gedruckt                                                                                                            | F29F85E0-4FF9-1068-AB91-08002B27B3D9/11                           |
| DocManager                   | Manager                                                                                                                 | D5CDD502-2E9C-101B-9397-08002B2CF9AE/14                           |
| Docpresentationformat        | PresentationTarget                                                                                                      | D5CDD502-2E9C-101B-9397-08002B2CF9AE/3                            |
| Docdiascount                | Folien                                                                                                                  | D5CDD502-2E9C-101B-9397-08002B2CF9AE/7                            |
| Audioavgdatarate             | Durchschnittliche Daten Rate in Kbit/s für die Audiodatei                                                                            | 64440490-4c8b-11d1-8b70-080036b11a03/4                            |
| Audiotimelength              | Länge in Millisekunden der Audiodatei                                                                                | 56a3372e-ce9c-11d2-9F 0E-006097c686f 6/8                            |
| MusicAlbum                   | Name des Albums                                                                                                              | 56a3372e-ce9c-11d2-9F 0E-006097c686/4                            |
| Musik                  | Der Name des Künstlers.                                                                                                      | 56a3372e-ce9c-11d2-9-e-006097c686-Dienst/2                            |
| Musikgenre                   | Genre des Albums                                                                                                      | 56a3372e-ce9c-11d2-9F 0E-006097c686/11                           |
| Musiktitel                   | Anzahl der Titel im Album                                                                                           | 56a3372e-ce9c-11d2-9F 0E-006097c686/7                            |
| Musik Jahr                    | Jahr, in dem das Album aufgezeichnet wurde                                                                                    | 56a3372e-ce9c-11d2-9F 0E-006097c686/5                            |
| Exigcameramake               | Hersteller der Kamera                                                                                                  | 14b81da1-0135-4d31-96d9-6cbfc9671a99/271                          |
| Exiamcameramodel              | Kameramodell                                                                                                         | 14b81da1-0135-4d31-96d9-6cbfc9671a99/272                          |
| DateTaken                    | FILETIME der ernommenen Daten                                                                                                  | D5CDD505-2E9C-101B-9397-08002B2CF9AE/DateTaken                    |
| Verlassen              | Orientation                                                                                                             | 14b81da1-0135-4d31-96d9-6cbfc9671a99/274                          |
| Imagedimensions              | Dimensionen des Bilds                                                                                                 | 6444048f -4c8b-11d1-8b70-080036b11a03/13                           |
| Imageresx                    | X-Auflösung für das Bild                                                                                              | 6444048f -4c8b-11d1-8b70-080036b11a03/5                            |
| Imageresy                    | Y-Auflösung für das Bild                                                                                              | 6444048f -4c8b-11d1-8b70-080036b11a03/6                            |
| Videoframeheight             | Rahmenhöhe für den Videostream                                                                                       | 64440491-4c8b-11d1-8b70-080036b11a03/4                            |
| Videoframerate               | Frame Rate in Frames pro Millisekunde für den Videostream                                                               | 64440491-4c8b-11d1-8b70-080036b11a03/6                            |
| Videoframewidth              | Rahmenbreite für den Videostream                                                                                        | 64440491-4c8b-11d1-8b70-080036b11a03/3                            |
| Klasse                        | Klassenname                                                                                                              | 8dee0300-16c2-101B-B121-08002b2ecda9/Klasse                        |
| Funktion                     | Funktionsname                                                                                                           | 8dee0300-16c2-101B-B121-08002b2ecda9/Func                         |
| Struktur                       | Strukturname                                                                                                          | 8dee0300-16c2-101B-B121-08002b2ecda9/struct                       |
| Schnittstelle                    | Schnittstellen Name                                                                                                          | 8dee0300-16c2-101B-B121-08002b2ecda9/Schnittstelle                    |
| Delegat                     | Delegatname                                                                                                           | 8dee0300-16c2-101B-B121-08002b2ecda9/Delegat                     |
| Eigenschaft                     | Eigenschaftenname                                                                                                           | 8dee0300-16c2-101B-B121-08002b2ecda9/Eigenschaft                     |
| Enumeration                         | Enum-Name                                                                                                               | 8dee0300-16c2-101B-B121-08002b2ecda9/Aufzählung                         |
| Const                        | Konstanter Name                                                                                                              | 8dee0300-16c2-101B-B121-08002b2ecda9/konstant                        |
| Ereignis                        | Ereignisname                                                                                                              | 8dee0300-16c2-101B-B121-08002b2ecda9/Ereignis                        |
| Feld                        | Feldname                                                                                                              | 8dee0300-16c2-101B-B121-08002b2ecda9/Feld                        |
| Definieren                       | Name definieren                                                                                                             | 8dee0300-16c2-101B-B121-08002b2ecda9/DEF                          |
| Komponente                    | Komponentenname                                                                                                          | 8dee0300-16c2-101B-B121-08002b2ecda9/Komponente                    |
| Project                      | Projektname                                                                                                            | 8dee0300-16c2-101B-B121-08002b2ecda9/Project                      |
| Lösung                     | Projektmappenname                                                                                                           | 8dee0300-16c2-101B-B121-08002b2ecda9/Lösung                     |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Referenz**
</dt> <dt>

[Entwickeln von IFilter-Add-ins](-search-2x-wds-ifilteraddins.md)
</dt> <dt>

[Entwickeln von Protokoll Handlern](-search-2x-wds-phaddins.md)
</dt> <dt>

[Erweiterte Abfragesyntax](-search-2x-wds-aqsreference.md)
</dt> <dt>

[Wahrgenommene Typen](-search-2x-wds-perceivedtype.md)
</dt> </dl>

 

 




