---
title: Protokollierungs-und Wiederherstellungs Fehler in Funktionen in Active Directory Domain Services
description: In diesem Thema werden die Rückgabewerte für die Protokollierung und Wiederherstellung für Funktionen in Active Directory Domain Services aufgeführt.
ms.assetid: b927073a-8bbc-45d4-b9d3-25f3aa6c6f53
ms.tgt_platform: multiple
keywords:
- Active Directory Protokollierungs-und Wiederherstellungs Fehler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6fba921a63eb399d6ed4f44ef8569ed05370403
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337554"
---
# <a name="logging-and-recovery-errors-in-functions-in-active-directory-domain-services"></a>Protokollierungs-und Wiederherstellungs Fehler in Funktionen in Active Directory Domain Services

In diesem Thema werden die Rückgabewerte für die Protokollierung und Wiederherstellung für Funktionen in Active Directory Domain Services aufgeführt.



| Wert                                | BESCHREIBUNG                                                                                                                      |
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| **hrlogfilebeschädigt**                 | Die Protokolldatei ist beschädigt.                                                                                                         |
| **hrnobackupdirectory**              | Es wurde kein Sicherungs Verzeichnis angegeben.                                                                                                   |
| **hrbackupdirectoriynotempty**        | Das Sicherungs Verzeichnis ist nicht leer.                                                                                               |
| **hrbackupinprogress**               | Die Sicherung ist aktiv.                                                                                                                |
| **hrmissingpreviouslogfile**         | Eine Protokolldatei für den Prüfpunkt fehlt.                                                                                        |
| **hrlogschreitefail**                   | In die Protokolldatei kann nicht geschrieben werden.                                                                                                 |
| **hrbadlogversion**                  | Die Version der Protokolldatei ist nicht mit der Version der Windows NT/Windows 2000-Verzeichnisdienst-Datenbank (NTDS) kompatibel. |
| **hrinvalidlogsequence**             | Der Zeitstempel im nächsten Protokoll entspricht nicht den Erwartungen.                                                                 |
| **hrloggingdeaktiviert**                | Das Protokoll ist nicht aktiv.                                                                                                           |
| **hrlogbufferto osmall**              | Der Protokollpuffer ist zu klein, um wieder hergestellt zu werden.                                                                                     |
| **hrlogsequenceend**                 | Die maximale Anzahl von Protokolldateien wurde überschritten.                                                                               |
| **hrnobackup**                       | Es wird keine Sicherung durchgeführt.                                                                                                  |
| **hrinvalidbackupsequence**          | Der Sicherungs Aufrufwert ist nicht in der Reihenfolge.                                                                                              |
| **hrbackupnotallowedyet**            | Eine Sicherung kann jetzt nicht ausgeführt werden.                                                                                                  |
| **hrdeletebackupfilefail**           | Die Sicherungsdatei kann nicht gelöscht werden.                                                                                                |
| **hrmakebackupdirectoriyfail**        | Ein temporäres Sicherungs Verzeichnis kann nicht erstellt werden.                                                                                     |
| **hrinvalidbackup**                  | Eine inkrementelle Sicherung kann nicht ausgeführt werden, wenn die zirkuläre Protokollierung                                                      |
| **hrwiederherstellungsmethoden**            | Fehler während des Reparatur Vorgangs.                                                                               |
| **hrmissinglogfile**                 | Die aktuelle Protokolldatei fehlt.                                                                                                 |
| **hrlogdiskfull**                    | Der Protokolldatenträger ist voll.                                                                                                            |
| **hrbadlogsignature**                | Eine Protokolldatei ist beschädigt.                                                                                                           |
| **hrbaddbsignature**                 | Eine Datenbankdatei ist beschädigt.                                                                                                      |
| **hrbadcheckpointsignature**         | Eine Prüf Punkt Datei ist beschädigt.                                                                                                    |
| **hrcheckpointbeschädigt**              | Eine Prüf Punkt Datei konnte nicht gefunden werden oder ist beschädigt.                                                                       |
| **hrdatabasinkonsistent**           | Die Datenbank ist beschädigt.                                                                                                         |
| **hrkonsistenttimemismatch**         | Bei der letzten konsistenten Zeit der Datenbank ist ein Konflikt aufgetreten.                                                                      |
| **hrpatchdatmisübereinstimmung**              | Die Patchdatei wird nicht aus dieser Sicherung generiert.                                                                                |
| **hrrestorelogzu olow**               | Die Start Protokollnummer ist zu niedrig für die Wiederherstellung.                                                                              |
| **hrrestorelogtohigh**              | Die Start Protokollnummer ist zu hoch für die Wiederherstellung.                                                                             |
| **hrgivenlogfilehasbadsignature**    | Die vom Band heruntergeladene Protokolldatei ist beschädigt.                                                                                |
| **hrgivenlogfileisnotcontiguous**    | Nach dem Herunterladen des Bands konnte keine verbindliche Protokolldatei gefunden werden.                                                               |
| **hrmissingrestorelogfiles**         | Die Daten werden nicht vollständig wieder hergestellt, da einige Protokolldateien fehlen.                                                               |
| **hrexistinglogflehasbadsignature** | Die Protokolldatei im Pfad der Protokolldatei ist beschädigt.                                                                                    |
| **hrexistinglogfleisnotcontiguous** | Im Protokolldatei Pfad wurde keine verbindliche Protokolldatei gefunden.                                                                        |
| **hrmissingfullbackup**              | Die Datenbank hat vor der inkrementellen Sicherung eine vorherige vollständige Sicherung verpasst.                                                        |
| **hrbadbackupdatabasesize**          | Die Größe der Sicherungs Datenbank muss ein Vielfaches von 4000 (4096 Bytes) sein.                                                                |
| **hrterminprogress**                 | Die Datenbank wird heruntergefahren.                                                                                                 |
| **hrfeaturenotavailable**            | Die Funktion ist nicht verfügbar.                                                                                                    |
| **hrinvalidname**                    | Der Name ist ungültig.                                                                                                             |
| **hrinvalidparameter**               | Der-Parameter ist ungültig.                                                                                                        |
| **hrcolumnnull**                     | Der Wert der Spalte ist NULL.                                                                                                 |
| **hrbuffertruncated**                | Der Puffer ist zu klein für die Daten.                                                                                                |
| **hrdatabaseattached**               | Die Datenbank ist bereits angefügt.                                                                                                |
| **hrinvaliddatabaseid**              | Die Datenbank-ID ist ungültig.                                                                                                      |
| **hrouto-Memory**                    | Der Computer verfügt nicht über genügend Arbeitsspeicher.                                                                                                   |
| **hrouesfdatabasespace**             | Die Datenbank hat die maximale Größe von 16 GB erreicht.                                                                              |
| **hrouto-Cursorn**                   | Out-of-table-Cursors.                                                                                                            |
| **hrouto-Puffer**                   | Nicht genügend Datenbankseiten Puffer.                                                                                                    |
| **hrin omanyindexes**                 | Es sind zu viele Indizes vorhanden.                                                                                                      |
| **hrzu-anykeys**                    | Es gibt zu viele Spalten in einem Index.                                                                                          |
| **hrrecorddeleted**                  | Der Datensatz wurde gelöscht.                                                                                                     |
| **hrlesverifyfailure**              | Ein Lese Überprüfungs Fehler ist aufgetreten.                                                                                              |
| **hrouto ffilehandles**               | Keine weiteren Dateihandles vorhanden.                                                                                                             |
| **hrdiskio**                         | Ein Datenträger-e/A-Fehler ist aufgetreten.                                                                                                       |
| **hrinvalidpath**                    | Der Pfad zur Datei ist ungültig.                                                                                                 |
| **hrrecordzu obig**                   | Der Datensatz hat die maximale Größe überschritten.                                                                                        |
| **hrin omanyopendatenbanken**           | Es sind zu viele geöffnete Datenbanken vorhanden.                                                                                               |
| **hrinvaliddatabase**                | Die Datei ist keine Datenbankdatei.                                                                                                 |
| **hrnotinitialisiert**                 | Die Datenbank wurde noch nicht aufgerufen.                                                                                                 |
| **hralleseryinitialisiert**             | Die Datenbank wurde bereits aufgerufen.                                                                                                 |
| **hrfileaccessdenied**               | Auf die Datei kann nicht zugegriffen werden.                                                                                                       |
| **hrbufferto osmall**                 | Der Puffer ist zu klein.                                                                                                         |
| **hrseeklotequal**                   | Entweder SeekLE oder SeekGE kann keine genaue Entsprechung finden.                                                                              |
| **hrin omanycolumns**                 | Es sind zu viele Spalten definiert.                                                                                              |
| **hrcontainernotempty**              | Der Container ist nicht leer.                                                                                                      |
| **hrinvalidfilename**                | Der Dateiname ist ungültig.                                                                                                         |
| **hrinvalidbookmark**                | Das Lesezeichen ist ungültig.                                                                                                         |
| **hrcolumninuse**                    | Die Spalte wird in einem Index verwendet.                                                                                                  |
| **hrinvalidbuffersize**              | Der Datenpuffer stimmt nicht mit der Spaltengröße identisch.                                                                                  |
| **hrcolumnnotupdatable**             | Der Spaltenwert kann nicht festgelegt werden.                                                                                                  |
| **hrindexinuse**                     | Der Index wird verwendet.                                                                                                             |
| **hrnullkeyunallowed**              | NULL-Schlüssel sind für einen Index nicht zulässig.                                                                                           |
| **hrnotintransaction**               | Die Operation muss Teil einer Transaktion sein.                                                                                      |
| **hrnoidleactivity**                 | Es ist keine Aktivität im Leerlauf aufgetreten.                                                                                                       |
| **hrin omanyactiveusers**             | Es sind zu viele aktive Datenbankbenutzer vorhanden.                                                                                        |
| **hrinvalidcountry**                 | Der Landes-oder Regions Code ist entweder nicht bekannt oder ungültig.                                                                    |
| **hrinvalidlanguageid**              | Die Sprach-ID ist entweder nicht bekannt oder ungültig.                                                                               |
| **hrinvalidcodepage**                | Die Codepage ist entweder nicht bekannt oder ungültig.                                                                                 |
| **hrnoschreitelock**                    | Es ist keine Schreibsperre auf Transaktionsebene 0 vorhanden.                                                                                   |
| **hrcolumnsetnull**                  | Der Spaltenwert wird auf NULL festgelegt.                                                                                                 |
| **hrversionstoreouabf-Speicher**        | Lmaxverpages überschritten (nur xjet).                                                                                           |
| **hrvorkomm zystackouabf-Speicher**       | Out-of-Cursors.                                                                                                                  |
| **hrouto-Sitzungen**                  | Außerhalb der Sitzungen.                                                                                                                 |
| **hrschreitekonflikt**                  | Die Schreibsperre konnte aufgrund einer ausstehenden Schreibsperre nicht ausgeführt werden.                                                                          |
| **hrtranstoodeep**                   | Die Transaktionen sind zu tief geschachtelt.                                                                                          |
| **hrinvalidsersid**                   | Das Sitzungs Handle ist ungültig.                                                                                                   |
| **hrsessionschreiteconflict**           | Eine andere Sitzung verfügt über eine private Version der Seite.                                                                               |
| **hrintransaction**                  | Der Vorgang ist innerhalb einer Transaktion nicht zulässig.                                                                               |
| **hrdatabaseduplicate**              | Die Datenbank ist bereits vorhanden.                                                                                                     |
| **hrdatabaseingeuse**                  | Die Datenbank wird verwendet.                                                                                                          |
| **hrdatabasenotfound**               | Die Datenbank ist nicht vorhanden.                                                                                                     |
| **hrdatabaseinvalidname**            | Der Datenbankname ist ungültig.                                                                                                    |
| **hrdatabaseinvalidpages**           | Die Anzahl der Seiten ist ungültig.                                                                                                  |
| **hrDatabaseCorrupted**              | Die Datenbankdatei ist entweder beschädigt oder wurde nicht gefunden.                                                                          |
| **hrdatabaselocked**                 | Die Datenbank ist gesperrt.                                                                                                          |
| **hrtableempty**                     | Eine leere Tabelle wurde geöffnet.                                                                                                       |
| **hrtablelocked**                    | Die Tabelle ist gesperrt.                                                                                                             |
| **hrtableduplicate**                 | Die Tabelle ist bereits vorhanden.                                                                                                        |
| **hrtableinuse**                     | Die Tabelle kann nicht gesperrt werden, da Sie bereits verwendet wird.                                                                           |
| **hrobjectnotfound**                 | Die Tabelle oder das Objekt ist nicht vorhanden.                                                                                              |
| **hrcannotrename**                   | Die temporäre Datei kann nicht umbenannt werden.                                                                                             |
| **hrdensityinvalid**                 | Die Datei-/Indexdichte ist ungültig.                                                                                               |
| **hrtablenotempty**                  | Der gruppierte Index kann nicht definiert werden.                                                                                            |
| **hrinvalidtableid**                 | Die Tabellen-ID ist ungültig.                                                                                                         |
| **hrin omanyopentables**              | Es können keine weiteren Tabellen geöffnet werden.                                                                                                  |
| **hrillegaloperation**               | Der Vorgang wird für Tabellen nicht unterstützt.                                                                                        |
| **hrobjectduplicate**                | Der Tabellen-oder Objektname wird bereits verwendet.                                                                                  |
| **hrinvalidobject**                  | Das Objekt ist für den Vorgang ungültig.                                                                                             |
| **hrindexcantbuild**                 | Ein gruppierter Index kann nicht erstellt werden.                                                                                               |
| **hrindexhasprimary**                | Der primäre Index ist bereits definiert.                                                                                            |
| **hrindexduplicate**                 | Der Index ist bereits definiert.                                                                                                    |
| **hrindexnotfound**                  | Der Index ist nicht vorhanden.                                                                                                        |
| **hrindexmuststay**                  | Ein gruppierter Index kann nicht gelöscht werden.                                                                                              |
| **hrindexinvaliddef**                | Die Index Definition ist unzulässig.                                                                                                 |
| **hrindexhasclustered**              | Der gruppierte Index ist bereits definiert.                                                                                          |
| **hrkreateingedexfailed**              | Der Index kann nicht erstellt werden, weil beim Erstellen einer Tabelle ein Fehler aufgetreten ist.                                                     |
| **hrin omanyopenindexes**             | Nicht genügend Index Beschreibungs Blöcke.                                                                                                 |
| **hrcolumnlong**                     | Der Spaltenwert ist zu lang.                                                                                                    |
| **hrcolumndoesnotfit**               | Das Feld passt nicht in den Datensatz.                                                                                            |
| **hrnullinvalid**                    | Der Wert darf nicht null sein.                                                                                                        |
| **hrcolumnindiziert**                  | Löschen nicht möglich, da die Spalte indiziert ist.                                                                                  |
| **hrcolumnzu obig**                   | Die Länge des Felds überschreitet die maximale Länge von 255 Bytes.                                                                 |
| **hrcolumnnotfound**                 | Die Spalte kann nicht gefunden werden.                                                                                                       |
| **hrcolumnduplicate**                | Das Feld ist bereits definiert.                                                                                                    |
| **hrColumn2ndSysMaint**              | Pro Tabelle ist nur eine automatische Inkrement-oder Versions Spalte zulässig.                                                                  |
| **hrinvalidcolumntype**              | Der Spaltendatentyp ist ungültig.                                                                                                 |
| **hrcolumnmaxtruncated**             | Die Spalte wurde abgeschnitten, weil Sie die maximale Länge von 255 Bytes überschreitet.                                                    |
| **hrcolumncannotindex**              | Eine lange Wert Spalte kann nicht indiziert werden.                                                                                             |
| **hrtaggednotnull**                  | Markierte Spalten dürfen nicht NULL sein.                                                                                                   |
| **hrnocurrentindex**                 | Der Eintrag ist ohne aktuellen Index ungültig.                                                                                    |
| **hrkeyismade**                      | Der Schlüssel ist fertiggestellt.                                                                                                             |
| **hrbadcolumnid**                    | Die Spalten-ID ist falsch.                                                                                                      |
| **hrbaditagsequence**                | Es ist ein fehlerhafter Instanzbezeichner für eine mehrwertige Spalte vorhanden.                                                                     |
| **hrcannotbetaging**                 | AutoIncrement und Version dürfen nicht mehr wertig sein.                                                                                 |
| **hrrecordnotfound**                 | Der Schlüssel wurde nicht gefunden.                                                                                                          |
| **hrnocurrentrecord**                | Die Währung ist nicht in einem Datensatz.                                                                                                 |
| **hrrecordclusteredchanged**         | Ein gruppierter Schlüssel kann nicht geändert werden.                                                                                               |
| **hrkeyduplicate**                   | Der Schlüssel ist bereits vorhanden.                                                                                                          |
| **hralleseryprepared**                | Der aktuelle Eintrag wurde bereits kopiert oder gelöscht.                                                                            |
| **hrkeynotmade**                     | Es wurde kein Schlüssel erstellt.                                                                                                                 |
| **hrupdatenotprepared**              | Das Update wurde nicht vorbereitet.                                                                                                         |
| **hrwrndatahaschge**              | Die Daten wurden geändert.                                                                                                                |
| **hrerrdatahaschge**              | Der Vorgang wurde abgebrochen, weil sich die Daten geändert haben.                                                                            |
| **hrkeychanged**                     | In einen neuen Schlüssel verschoben.                                                                                                              |
| **hresomanysort**                   | Es sind zu viele Sortier Prozesse vorhanden.                                                                                               |
| **hrinvalidonsort**                  | Ein ungültiger Vorgang ist in der Sortierung aufgetreten.                                                                               |
| **hrtempfleopenerror**              | Die temporäre Datei kann nicht geöffnet werden.                                                                                               |
| **hrin omanyattacheddatenbanken**       | Es sind zu viele Datenbanken geöffnet.                                                                                               |
| **hrdiskfull**                       | Der Datenträger ist voll.                                                                                                                |
| **hrpermissiondenied**               | Die Berechtigung wurde verweigert.                                                                                                            |
| **hrfile-found**                   | Die Datei wurde nicht gefunden.                                                                                                         |
| **hrfileopenschreib Only**               | Die Datenbankdatei ist schreibgeschützt.                                                                                                  |
| **HRAF-Initialisierung**            | Nach der Initialisierung kann nicht wieder hergestellt werden.                                                                                          |
| **hrlogbeschädigt**                   | Die Daten Bank Protokolldateien sind beschädigt.                                                                                              |
| **hrinvalidoperation**               | Der Vorgang ist ungültig.                                                                                                        |
| **hraccess verweigert**                   | Zugriff verweigert.“                                                                                                                |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erfolgreich](success.md)
</dt> <dt>

[Sicherungs Fehler in Active Directory Domain Services](backup-errors-in-active-directory-domain-services.md)
</dt> <dt>

[System Fehler in Active Directory Domain Services](system-errors-in-active-directory-domain-services.md)
</dt> <dt>

[Verzeichnis-Manager-Fehler](directory-manager-errors.md)
</dt> <dt>

[Rückgabewerte für Funktionen in Active Directory Domain Services](return-values-for-functions-in-active-directory-domain-services.md)
</dt> </dl>

 

 




