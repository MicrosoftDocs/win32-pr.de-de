---
title: Schema (Legacy Windows Umgebungsfeatures)
description: Das Schema dokumentiert die Werte und Eigenschaften, die der Index zum Speichern von Daten für die Indizierung oder Sortierung verwendet.
ms.assetid: dfd8862c-8f84-441e-a4b4-4af3c76c48f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2d5c80690914073af1c67e2bd00376974547d30c4dc487c0656d4452d3fe828
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118753149"
---
# <a name="schema"></a>Schema

> [!NOTE]
> Windows Desktop Search 2.x ist eine veraltete Technologie, die ursprünglich als Add-In für Windows XP und Windows Server 2003 verfügbar war. Verwenden Sie in späteren [Versionen Windows Search.](../search/-search-3x-wds-overview.md)

Das Schema dokumentiert die Werte und Eigenschaften, die der Index zum Speichern von Daten für die Indizierung oder Sortierung verwendet. In der Tabelle Schema sind die Spalten und ihre Eigenschaften (Typ und Propid) aufgeführt, die im Schema für Microsoft Windows Desktop Search (WDS) 2.6.5 enthalten sind.

## <a name="schema"></a>Schema



| Spaltenname                  | Beschreibung                                                                                                             | Propid                                                            |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| DocComments                  | Kommentare                                                                                                                | F29F85E0-4FF9-1068-AB91-08002B27B3D9/6                            |
| Erstellen                       | Datum und Uhrzeit der Erstellung der Datei                                                                                      | B725F130-47EF-101A-A5F1-02608C9EEBAC/15                           |
| DisplayFolder                | Benutzerfreundlicher Ordner für Element                                                                                           | D5CDD505-2E9C-101B-9397-08002B2CF9AE/DisplayFolder                |
| DocAuthor                    | Autor des Dokuments                                                                                                  | F29F85E0-4FF9-1068-AB91-08002B27B3D9/4                            |
| DocCategory                  | Kategorie                                                                                                                | D5CDD502-2E9C-101B-9397-08002B2CF9AE/2                            |
| DocKeywords                  | Keywords                                                                                                                | F29F85E0-4FF9-1068-AB91-08002B27B3D9/5                            |
| DocTitlePrefix               | Präfix des Betreffs (Re:, Fw:usw.)                                                                                      | D5CDD505-2E9C-101B-9397-08002B2CF9AE/DocTitlePrefix               |
| DocTitle                     | Titel                                                                                                                   | F29F85E0-4FF9-1068-AB91-08002B27B3D9/2                            |
| FileExtDesc                  | Benutzerfreundliche Beschreibung des Dateityps aus der Registrierung (z.B. .psq --> Product Studio-Abfragedatei)                | D5CDD505-2E9C-101B-9397-08002B2CF9AE/FileExtDesc                  |
| FolderName                   | Name des übergeordneten Ordners                                                                                               | D5CDD505-2E9C-101B-9397-08002B2CF9AE/FolderName                   |
| IsAttachment                 | Gibt an, dass es sich bei dem Element um eine Anlage handelt.                                                                                         | D5CDD505-2E9C-101B-9397-08002B2CF9AE/IsAttachment                 |
| isDeleted                    | Gibt an, dass das Element zum Löschen markiert ist (Papierkorb, gelöschte Elemente usw.).                                                | D5CDD505-2E9C-101B-9397-08002B2CF9AE/isDeleted                    |
| LastViewed                   | Datum, an dem das Element zuletzt vom Benutzer angezeigt wurde                                                                                   | D5CDD505-2E9C-101B-9397-08002B2CF9AE/LastViewed                   |
| Personen                       | Personen, die an diesem Element beteiligt sind                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/People                       |
| PerceivedType                | PerceivedType des Objekts HINWEIS: Dies ist nur zum Abrufen.                                                           | D5CDD505-2E9C-101B-9397-08002B2CF9AE/PerceivedType                |
| PerceivedTypeName            | Anzeigename des PerceivedType.  Nie angezeigt oder abgefragt                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/PerceivedTypeName            |
| PrimaryDate                  | Interessantstes Datum (Zeitpunkt des letzten Schreibzugriffs für Dateien, Empfangen des E-Mail-Datums)                                              | D5CDD505-2E9C-101B-9397-08002B2CF9AE/PrimaryDate                  |
| Size                         | Größe einer Datei.                                                                                                         | B725F130-47EF-101A-A5F1-02608C9EEBAC/12                           |
| DocSubject                   | Betreff der Datei. HINWEIS: Derzeit werden E-Mail-Themen primaryTitle zuordnen und aufgrund ihrer Länge nicht dupliziert. | F29F85E0-4FF9-1068-AB91-08002B27B3D9/3                            |
| URL                          | Abfragebasierte URL                                                                                                         | 49691C90-7E17-101A-A91C-08002B2ECDA9/9                            |
| Schreiben                        | Datum und Uhrzeit des letzten Schreibzugriffs in die Datei                                                                             | B725F130-47EF-101A-A5F1-02608C9EEBAC/14                           |
| DueDate                      | Datum, an dem ein Element fällig ist                                                                                                     | D5CDD505-2E9C-101B-9397-08002B2CF9AE/DueDate                      |
| IsIncomplete                 | Gibt an, dass das Element nicht vollständig verfügbar ist.                                                                                   | D5CDD505-2E9C-101B-9397-08002B2CF9AE/IsIncomplete                 |
| IsFlaggedCompleted           | Gibt an, dass das Element als abgeschlossen gekennzeichnet ist.                                                                                  | D5CDD505-2E9C-101B-9397-08002B2CF9AE/IsFlaggedCompleted           |
| IsFlagged                    | Gibt an, dass das Element gekennzeichnet ist.                                                                                               | D5CDD505-2E9C-101B-9397-08002B2CF9AE/IsFlagged                    |
| FlagText                     | Text, der für das Flag angezeigt wird, z. B. Überprüfen, Nach verfolgen usw.                                                              | D5CDD505-2E9C-101B-9397-08002B2CF9AE/FlagText                     |
| Identity                     | Identität für OE-Benutzer                                                                                                   | D5CDD505-2E9C-101B-9397-08002B2CF9AE/Identity                     |
| IsRead                       | Gibt an, dass das Element gelesen wurde.                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/IsRead                       |
| Wichtigkeit                   | MAPI-Wichtigkeit oder -Priorität                                                                                             | D5CDD505-2E9C-101B-9397-08002B2CF9AE/Importance                   |
| ContainerHash                | Hashcode, der anlagen identifiziert, die basierend auf einer gemeinsamen Container-URL gelöscht werden sollen                                     | D5CDD505-2E9C-101B-9397-08002B2CF9AE/ContainerHash                |
| Docformat                    | Dokumentformat oder MIMETYPE (z.B. "message/rfc822" für eine EML-Datei)                                              | 0B63E350-9CCC-11D0-BCDB-00805 NAPE04/5                            |
| GatherTimeModified           | Zeitpunkt, zu dem der Indexer das Dokument zuletzt für die Katalogaktualisierung durchforstet hat                                                           | 0b63e350-9ccc-11d0-bcdb-00805 flocke04/4                            |
| Speicher                        | Der Speicher- oder Protokollhandler (FILE, MAIL, OUTLOOKEXPRESS)                                                              | D5CDD505-2E9C-101B-9397-08002B2CF9AE/Store                        |
| FileExt                      | Dateierweiterung                                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/FileExt                      |
| FileName                     | Der Name der Datei.                                                                                                        | B725F130-47EF-101A-A5F1-02608C9EEBAC/10                           |
| ShortName                    | Kurzer Dateiname (8.3) für die Datei                                                                                      | B725F130-47EF-101A-A5F1-02608C9EEBAC/20                           |
| AttachmentNames              | Namen von Anlagen in einer Nachricht                                                                                       | D5CDD505-2E9C-101B-9397-08002B2CF9AE/AttachmentNames              |
| BccAddress                   | Adressen in Bcc: feld                                                                                                 | D5CDD505-2E9C-101B-9397-08002B2CF9AE/BccAddress                   |
| BccName                      | Personennamen in Bcc: Feld                                                                                              | D5CDD505-2E9C-101B-9397-08002B2CF9AE/BccName                      |
| CcAddress                    | Adressen im Feld Cc:                                                                                                  | D5CDD505-2E9C-101B-9397-08002B2CF9AE/CcAddress                    |
| CcName                       | Personennamen im Feld Cc:                                                                                               | D5CDD505-2E9C-101B-9397-08002B2CF9AE/CcName                       |
| ConversationID               | Eindeutige ID für eine Konversation in E-Mail-Threads                                                                           | D5CDD505-2E9C-101B-9397-08002B2CF9AE/ConversationID               |
| FromAddress                  | Adressen im Feld Von:                                                                                                | D5CDD505-2E9C-101B-9397-08002B2CF9AE/FromAddress                  |
| FromName                     | Personenname im Feld From:                                                                                              | D5CDD505-2E9C-101B-9397-08002B2CF9AE/FromName                     |
| FwdRply                      | Gibt an, dass E-Mails beantwortet oder weitergeleitet wurden (cdoPR \_ ACTION=261 262).                                                      | D5CDD505-2E9C-101B-9397-08002B2CF9AE/FwdRply                      |
| HasAttach                    | Gibt an, dass die E-Mail über eine Anlage verfügt (T oder F).                                                                               | D5CDD505-2E9C-101B-9397-08002B2CF9AE/HasAttach                    |
| ReceivedDate                 | Übermittlungszeit                                                                                                           | D5CDD505-2E9C-101B-9397-08002B2CF9AE/ReceivedDate                 |
| ToAddress                    | Adressen im Feld An:                                                                                                  | D5CDD505-2E9C-101B-9397-08002B2CF9AE/ToAddress                    |
| ToName                       | Personennamen im Feld An:                                                                                               | D5CDD505-2E9C-101B-9397-08002B2CF9AE/ToName                       |
| TaskStatus                   | Status einer Aufgabe                                                                                                        | D5CDD505-2E9C-101B-9397-08002B2CF9AE/TaskStatus                   |
| EndDate                      | Endzeit (in der Regel für Besprechungen/Ereignisse)                                                                                  | D5CDD505-2E9C-101B-9397-08002B2CF9AE/EndDate                      |
| IsRecurring                  | Gibt an, dass sich das Element wiederholt (z. B. Besprechungen)                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/IsRecurring                  |
| StartDate                    | Startzeit (normalerweise für Besprechungen/Ereignisse)                                                                                | D5CDD505-2E9C-101B-9397-08002B2CF9AE/StartDate                    |
| Duration                     | Dauer der Besprechung in Minuten                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/Duration                     |
| Standort                     | Ort, an dem das Element (z. B. eine Besprechung) auftritt                                                                             | D5CDD505-2E9C-101B-9397-08002B2CF9AE/Location                     |
| Jahrestag                  | Anniversary date (Jahrestag)                                                                                                        | D5CDD505-2E9C-101B-9397-08002B2CF9AE/Anniversary                  |
| AssistantName                | Name des Assistenten                                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/AssistantName                |
| AssistantTelephone           | Telefon des Assistenten                                                                                                     | D5CDD505-2E9C-101B-9397-08002B2CF9AE/AssistantTelephone           |
| Birthday                     | Kontaktperson                                                                                                     | D5CDD505-2E9C-101B-9397-08002B2CF9AE/Org                     |
| BusinessAddressCity          | Geschäftsadresseninformationen                                                                                                   | D5CDD505-2E9C-101B-9397-08002B2CF9AE/BusinessAddressCity          |
| BusinessAddressPostalCode    | Geschäftsadresseninformationen                                                                                                   | D5CDD505-2E9C-101B-9397-08002B2CF9AE/BusinessAddressPostalCode    |
| BusinessAddressPostOfficeBox | Geschäftsadresseninformationen                                                                                                   | D5CDD505-2E9C-101B-9397-08002B2CF9AE/BusinessAddressPostOfficeBox |
| BusinessAddressState         | Geschäftsadresseninformationen                                                                                                   | D5CDD505-2E9C-101B-9397-08002B2CF9AE/BusinessAddressState         |
| BusinessAddressBusiness        | Geschäftsadresseninformationen                                                                                                   | D5CDD505-2E9C-101B-9397-08002B2CF9AE/BusinessAddressBusiness        |
| BusinessAddressCountry       | Geschäftsadresseninformationen                                                                                                   | D5CDD505-2E9C-101B-9397-08002B2CF9AE/BusinessAddressCountry       |
| CallbackTelephone            | Telefoninformationen zurückrufen                                                                                                | D5CDD505-2E9C-101B-9397-08002B2CF9AE/CallbackTelephone            |
| CarTelephone                 | Telefoninformationen                                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/CarTelephone                 |
| Children                     | Namen der untergeordneten Elemente für den Kontakt                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/Children                     |
| CompanyMainTelephone         | Telefoninformationen                                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/CompanyMainTelephone         |
| EmailAddress                 | Kontakt-E-Mail-Name                                                                                                      | D5CDD505-2E9C-101B-9397-08002B2CF9AE/EmailAddress                 |
| EmailName                    | Anzeigename für E-Mail-Adresse                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/EmailName                    |
| FirstName                    | Vorname des Kontakts                                                                                                    | D5CDD505-2E9C-101B-9397-08002B2CF9AE/FirstName                    |
| FullName                     | Vollständiger Name des Kontakts                                                                                                     | D5CDD505-2E9C-101B-9397-08002B2CF9AE/FullName                     |
| Geschlecht                       | Male/female/other                                                                                                       | D5CDD505-2E9C-101B-9397-08002B2CF9AE/Gender                       |
| Hobby                        | Kontaktinformationen                                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/Rates                        |
| HomeAddressCity              | Startadresseninformationen                                                                                                       | D5CDD505-2E9C-101B-9397-08002B2CF9AE/HomeAddressCity              |
| HomeAddressCountry           | Startadresseninformationen                                                                                                       | D5CDD505-2E9C-101B-9397-08002B2CF9AE/HomeAddressCountry           |
| HomeAddressPostalCode        | Startadresseninformationen                                                                                                       | D5CDD505-2E9C-101B-9397-08002B2CF9AE/HomeAddressPostalCode        |
| HomeAddressState             | Startadresseninformationen                                                                                                       | D5CDD505-2E9C-101B-9397-08002B2CF9AE/HomeAddressState             |
| HomeAddressMap            | Startadresseninformationen                                                                                                       | D5CDD505-2E9C-101B-9397-08002B2CF9AE/HomeAddressLadung            |
| HomeFaxNumber                | Faksimile-Informationen                                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/HomeFaxNumber                |
| BusinessFaxNumber            | Faksimile-Informationen                                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/BusinessFaxNumber            |
| HomeTelephone                | Telefoninformationen                                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/HomeTelephone                |
| IMAddress                    | Sofortmeldungsinformationen                                                                                                    | D5CDD505-2E9C-101B-9397-08002B2CF9AE/IMAddress                    |
| JobTitle                     | Position des Kontakts                                                                                                     | D5CDD505-2E9C-101B-9397-08002B2CF9AE/JobTitle                     |
| MiddleName                   | Kontaktinformationen                                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/MiddleName                   |
| MobileTelephone              | Telefoninformationen                                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/MobileTelephone              |
| NickName                     | Kontaktinformationen                                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/NickName                     |
| Office                       | Kontaktinformationen                                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/Office                       |
| OfficeTelephone              | Telefoninformationen                                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/OfficeTelephone              |
| PagerTelephone               | Telefoninformationen                                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/PagerTelephone               |
| LastName                     | Kontaktinformationen                                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/LastName                     |
| PersonalTitle                | Profession title (Dr., Mr., Mrs., Ms.)                                                                                  | D5CDD505-2E9C-101B-9397-08002B2CF9AE/PersonalTitle                |
| PrimaryTelephone             | Telefoninformationen                                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/PrimaryTelephone             |
| Profession                   | Kontaktinformationen                                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/Austragen                   |
| Ehepartner                       | Kontaktinformationen                                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/Alle                       |
| Suffix                       | Kontaktinformationen                                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/suffix                       |
| TelexNumber                  | Telex-Informationen                                                                                                              | D5CDD505-2E9C-101B-9397-08002B2CF9AE/TelexNumber                  |
| TTYTDDTelephone              | TTY/TDD-Informationen                                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/TTYTDDTelephone              |
| WebPage                      | Kontaktwebseite                                                                                                        | D5CDD505-2E9C-101B-9397-08002B2CF9AE/WebPage                      |
| DocCompany                   | Company                                                                                                                 | D5CDD502-2E9C-101B-9397-08002B2CF9AE/15                           |
| DocLastAuthor                | Benutzer, von dem die Dokumentation zuletzt gespeichert wurde                                                                                           | F29F85E0-4FF9-1068-AB91-08002B27B3D9/8                            |
| DocLastPrinted               | Zuletzt gedruckt                                                                                                            | F29F85E0-4FF9-1068-AB91-08002B27B3D9/11                           |
| DocManager                   | Manager                                                                                                                 | D5CDD502-2E9C-101B-9397-08002B2CF9AE/14                           |
| DocPresentationFormat        | PresentationTarget                                                                                                      | D5CDD502-2E9C-101B-9397-08002B2CF9AE/3                            |
| DocSlideCount                | Folien                                                                                                                  | D5CDD502-2E9C-101B-9397-08002B2CF9AE/7                            |
| AudioAvgDataRate             | Durchschnittliche Datenrate in KBit/s für die Audiodatei                                                                            | 64440490-4C8B-11D1-8B70-080036B11A03/4                            |
| AudioTimeLength              | Länge der Audiodatei in Millisekunden                                                                                | 56A3372E-CE9C-11D2-9F0E-006097C686F6/8                            |
| MusicAlbum                   | Albumname                                                                                                              | 56A3372E-CE9C-11D2-9F0E-006097C686F6/4                            |
| MusicArtist                  | Name des Interpreten                                                                                                      | 56A3372E-CE9C-11D2-9F0E-006097C686F6/2                            |
| MusicGenre                   | Genre des Albums                                                                                                      | 56A3372E-CE9C-11D2-9F0E-006097C686F6/11                           |
| MusicTrack                   | Anzahl der Titel im Album                                                                                           | 56A3372E-CE9C-11D2-9F0E-006097C686F6/7                            |
| MusicYear                    | Jahr, in dem das Album aufgezeichnet wurde                                                                                    | 56A3372E-CE9C-11D2-9F0E-006097C686F6/5                            |
| ExifCameraMake               | Hersteller der Kamera                                                                                                  | 14B81DA1-0135-4D31-96D9-6CBFC9671A99/271                          |
| ExifCameraModel              | Kameramodell                                                                                                         | 14B81DA1-0135-4D31-96D9-6CBFC9671A99/272                          |
| DateTaken                    | FILETIME der aufgenommenen Daten                                                                                                  | D5CDD505-2E9C-101B-9397-08002B2CF9AE/DateTaken                    |
| ExifOrientation              | Orientation                                                                                                             | 14B81DA1-0135-4D31-96D9-6CBFC9671A99/274                          |
| ImageDimensions              | Dimensionen des Bilds                                                                                                 | 6444048F-4C8B-11D1-8B70-080036B11A03/13                           |
| ImageResX                    | X-Auflösung für das Bild                                                                                              | 6444048F-4C8B-11D1-8B70-080036B11A03/5                            |
| ImageResy                    | Y-Auflösung für das Bild                                                                                              | 6444048F-4C8B-11D1-8B70-080036B11A03/6                            |
| VideoFrameHeight             | Framehöhe für den Videostream                                                                                       | 64440491-4C8B-11D1-8B70-080036B11A03/4                            |
| VideoFrameRate               | Bildfrequenz in Frames pro Millisekunde für den Videostream                                                               | 64440491-4C8B-11D1-8B70-080036B11A03/6                            |
| VideoFrameWidth              | Framebreite für den Videostream                                                                                        | 64440491-4C8B-11D1-8B70-080036B11A03/3                            |
| Klasse                        | Klassenname                                                                                                              | 8dee0300-16c2-101b-b121-08002b2ecda9/class                        |
| Funktion                     | Funktionsname                                                                                                           | 8dee0300-16c2-101b-b121-08002b2ecda9/func                         |
| Struktur                       | Strukturname                                                                                                          | 8dee0300-16c2-101b-b121-08002b2ecda9/struct                       |
| Schnittstelle                    | Schnittstellenname                                                                                                          | 8dee0300-16c2-101b-b121-08002b2ecda9/interface                    |
| Delegat                     | Delegatname                                                                                                           | 8dee0300-16c2-101b-b121-08002b2ecda9/delegate                     |
| Eigenschaft                     | Eigenschaftenname                                                                                                           | 8dee0300-16c2-101b-b121-08002b2ecda9/property                     |
| Enumeration                         | Enumerationsname                                                                                                               | 8dee0300-16c2-101b-b121-08002b2ecda9/enum                         |
| Const                        | Const-Name                                                                                                              | 8dee0300-16c2-101b-b121-08002b2ecda9/const                        |
| Ereignis                        | Ereignisname                                                                                                              | 8dee0300-16c2-101b-b121-08002b2ecda9/event                        |
| Feld                        | Feldname                                                                                                              | 8dee0300-16c2-101b-b121-08002b2ecda9/field                        |
| Definieren                       | Definieren des Namens                                                                                                             | 8dee0300-16c2-101b-b121-08002b2ecda9/def                          |
| Komponente                    | Komponentenname                                                                                                          | 8dee0300-16c2-101b-b121-08002b2ecda9/component                    |
| Project                      | Projektname                                                                                                            | 8dee0300-16c2-101b-b121-08002b2ecda9/project                      |
| Lösung                     | Projektmappenname                                                                                                           | 8dee0300-16c2-101b-b121-08002b2ecda9/solution                     |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Referenz**
</dt> <dt>

[Entwickeln von IFilter-Add-Ins](-search-2x-wds-ifilteraddins.md)
</dt> <dt>

[Entwickeln von Protokollhandlern](-search-2x-wds-phaddins.md)
</dt> <dt>

[Erweiterte Abfragesyntax](-search-2x-wds-aqsreference.md)
</dt> <dt>

[Wahrgenommene Typen](-search-2x-wds-perceivedtype.md)
</dt> </dl>

 

 




