---
description: Steuerungs Codes, die in der Dateiverwaltung verwendet werden.
ms.assetid: e27ded4b-d104-4244-b38e-5fed10d32e1e
title: Dateiverwaltungs-Steuerungscodes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64cb3baf78c4066a640242afe8465592bc9a6f8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868243"
---
# <a name="file-management-control-codes"></a>Dateiverwaltungs-Steuerungscodes

Die folgenden Kontrollcodes werden in der Dateiverwaltung verwendet.

## <a name="in-this-section"></a>In diesem Abschnitt



| Steuerungscode                                                                                    | BESCHREIBUNG                                                                                                                                                                                         |
|-------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ \_ Erweiterte \_ DASD-e/a-Vorgänge zulassen \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_allow_extended_dasd_io)<br/>             | Weist den Dateisystem Treiber an, keine e/a-Begrenzungs Prüfungen bei Lese-oder Schreib Aufrufen von Partitionen auszuführen.<br/>                                                                                  |
| [**\_Objekt-ID zum Erstellen oder zum Erstellen von \_ \_ \_ Objekten \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_create_or_get_object_id)<br/>          | Ruft den Objekt Bezeichner für die angegebene Datei oder das angegebene Verzeichnis ab. Wenn kein Objekt Bezeichner vorhanden ist, wird durch die Verwendung von " **\_ Create" oder " \_ \_ get \_ Object \_ ID** " eine solche erstellt<br/>                           |
| [**CSV-Steuerelement "f" \_ \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_csv_control)<br/>                                     | Ruft die Ergebnisse eines CSV-Steuerelement Vorgangs ab.<br/>                                                                                                                                        |
| [**ID des bsctl- \_ Lösch \_ Objekts \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_delete_object_id)<br/>                          | Entfernt den Objekt Bezeichner aus einer angegebenen Datei bzw. einem angegebenen Verzeichnis.<br/>                                                                                                                        |
| [**Datei Blöcke mit doppelter FSCTL- \_ \_ \_ \_ Datei**](/windows/win32/api/winioctl/ni-winioctl-fsctl_duplicate_extents_to_file)<br/>       | Weist das Dateisystem an, einen Bereich von Datei Bytes für eine Anwendung zu kopieren.<br/>                                                                                                     |
| [**\_Trim auf Dateiebene auf Datei \_ Ebene \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_file_level_trim)<br/>                            | Gibt dem Speichersystem an, welche Bereiche in der Datei nicht gespeichert werden müssen.<br/>                                                                                                    |
| [**\_Datei "File File System \_ get \_ Statistics"**](/windows/win32/api/winioctl/ni-winioctl-fsctl_filesystem_get_statistics)<br/>        | Ruft die Informationen aus verschiedenen Leistungsindikatoren des Dateisystems ab.<br/>                                                                                                                 |
| [**\_Datei "File File System \_ get \_ Statistics \_ from"**](/windows/win32/api/winioctl/ni-winioctl-fsctl_filesystem_get_statistics_ex)<br/> | Ruft die Informationen aus verschiedenen Leistungsindikatoren des Dateisystems ab.<br/> Unterstützung für diesen Steuerungs Code wurde mit Windows 10 gestartet.<br/>                                               |
| [**\_ \_ Dateien \_ nach \_ sid suchen**](/windows/win32/api/winioctl/ni-winioctl-fsctl_find_files_by_sid)<br/>                       | Durchsucht ein Verzeichnis nach einer Datei, deren Ersteller-Besitzer mit der angegebenen SID übereinstimmt.<br/>                                                                                                           |
| [**Komprimierung von "f" \_ \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_compression)<br/>                             | Ruft den aktuellen Komprimierungs Status einer Datei oder eines Verzeichnisses auf einem Volume ab, dessen Dateisystem die Komprimierung pro Stream unterstützt.<br/>                                                            |
| [**ssctl \_ - \_ NTFS- \_ Datei \_ Daten Satz**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_file_record)<br/>                 | Ruft den ersten verwendeten Datei Daten Satz ab, der für die angeforderte Datei Verweis Nummer einen niedrigeren oder gleichen Ordinalwert hat.<br/>                                                    |
| [**ID des abzuruf- \_ \_ Objekts \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_object_id)<br/>                                | Ruft den Objekt Bezeichner für die angegebene Datei oder das angegebene Verzeichnis ab.<br/>                                                                                                                     |
| [**ssctl \_ - \_ Reparatur**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_repair)<br/>                                       | Ruft Informationen zum Selbstreparatur Mechanismus des NTFS-Dateisystems ab.<br/>                                                                                                               |
| [**Reparieren von "ssctl \_ initiieren" \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_initiate_repair)<br/>                             | Hiermit wird das NTFS-Dateisystem ausgelöst, um einen Selbstheilungs Zeitraum für eine einzelne Datei zu starten.<br/>                                                                                                            |
| [**mit "f \_ " \_ Medien \_ kompatibel machen**](/windows/win32/api/winioctl/ni-winioctl-fsctl_make_media_compatible)<br/>                | Schließt eine geöffnete UDF-Sitzung auf einem Write-Once-Medium, damit die Medien-ROM kompatibel ist.<br/>                                                                                                         |
| [**Schließen von "ssctl \_ opbatch \_ ACK" \_ steht \_ aus**](/windows/win32/api/winioctl/ni-winioctl-fsctl_opbatch_ack_close_pending)<br/>       | Benachrichtigt einen Server, dass eine Client Anwendung bereit ist, eine Datei zu schließen.<br/>                                                                                                                    |
| [**Ssctl- \_ Oplock- \_ break- \_ ACK Nr. \_ \_ 2**](/windows/win32/api/winioctl/ni-winioctl-fsctl_oplock_break_ack_no_2)<br/>              | Antwortet auf Benachrichtigung, dass eine opportunistische Sperre für eine Datei im Begriff ist, beschädigt zu werden. Verwenden Sie diesen Vorgang, um alle opportunistischen Sperren für die Datei zu entsperren, aber die Datei offen zu lassen.<br/>            |
| [**losctl- \_ Oplock- \_ Abbruch \_ bestätigen**](/windows/win32/api/winioctl/ni-winioctl-fsctl_oplock_break_acknowledge)<br/>          | Antwortet auf Benachrichtigung, dass eine exklusive, opportunistische Sperre für eine Datei im Begriff ist, beschädigt zu werden. Verwenden Sie diesen Vorgang, um anzugeben, dass die Datei eine opportunistische Sperre der Ebene 2 empfangen soll.<br/> |
| [**Benachrichtigung zum Abbrechen der Sperre von "f" \_ \_ \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_oplock_break_notify)<br/>                    | Ermöglicht der aufrufenden Anwendung, auf den Abschluss eines opportunistischen Sperr Bruchs zu warten.<br/>                                                                                                   |
| [**\_ \_ zugeordnete Bereiche der ssctl-Abfrage \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_allocated_ranges)<br/>              | Scannt eine Datei oder einen alternativen Stream und sucht nach Bereichen, die möglicherweise Daten enthalten, die nicht NULL sind.<br/>                                                                                                       |
| [**ssctl- \_ Abfrage zu Datenträger \_ Volume- \_ \_ \_ Informationen**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_on_disk_volume_info)<br/>      | Fordert UDF-spezifische Volumeinformationen an.<br/>                                                                                                                                                |
| [**Informationen zur ssktl- \_ Abfrage \_ \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_sparing_info)<br/>                      | Ruft die Eigenschaften der Mängel Verwaltung des Volumes ab. Wird für UDF-Dateisysteme verwendet.<br/>                                                                                                     |
| [**Datei für die \_ Datei-Rückruf \_ Datei**](/windows/win32/api/winioctl/ni-winioctl-fsctl_recall_file)<br/>                                     | Gibt eine Datei von einem Speichermedium an, das von Remote Speicher verwaltet wird, also der hierarchischen Speicherverwaltungssoftware.<br/>                                                                    |
| [**Sperre für den ssctl- \_ Anforderungs \_ Batch \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_batch_oplock)<br/>                  | Fordert eine Batch opportunistische Sperre für eine Datei an.<br/>                                                                                                                                           |
| [**\_Oplock für die Anforderung des volltextsfilters \_ \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_filter_oplock)<br/>                | Fordert eine durch einen Filter opportunistische Sperre für eine Datei an.<br/>                                                                                                                                          |
| [**Oplock für die ssctl- \_ Anforderung \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_oplock)<br/>                               | Fordert eine opportunistische Sperre (Oplock) für eine Datei an und bestätigt, dass ein Oplock-Break aufgetreten ist.<br/>                                                                                    |
| [**Ssctl- \_ Anforderungs- \_ Oplock- \_ Ebene \_ 1**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_oplock_level_1)<br/>             | Fordert eine opportunistische Sperre der Ebene 1 für eine Datei an.<br/>                                                                                                                                         |
| [**Ssctl- \_ Anforderungs- \_ Oplock- \_ Ebene \_ 2**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_oplock_level_2)<br/>             | Fordert eine opportunistische Sperre der Ebene 2 für eine Datei an.<br/>                                                                                                                                         |
| [**Komprimierung von ssctl- \_ Satz \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_compression)<br/>                             | Legt den Komprimierungs Status einer Datei oder eines Verzeichnisses auf einem Volume fest, dessen Dateisystem die Komprimierung pro Datei und pro Verzeichnis unterstützt.<br/>                                                         |
| [**\_ \_ Fehler \_ Verwaltung bei der ssctl-Gruppe**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_defect_management)<br/>                | Legt den Zustand der Software Mängel Verwaltung für die angegebene Datei fest. Wird für UDF-Dateisysteme verwendet.<br/>                                                                                             |
| [**Objekt-ID des ssctl- \_ Satzes \_ \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_object_id)<br/>                                | Legt den Objekt Bezeichner für die angegebene Datei bzw. das angegebene Verzeichnis fest.<br/>                                                                                                                          |
| [**Objekt-ID für das bsctl- \_ Set wurde \_ \_ \_ erweitert**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_object_id_extended)<br/>             | Ändert die Benutzerdaten, die dem Objekt Bezeichner für die angegebene Datei oder das angegebene Verzeichnis zugeordnet sind.<br/>                                                                                            |
| [**Reparatur von "ssctl \_ Set" \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_repair)<br/>                                       | Legt den Modus für die Selbstreparatur Funktion eines NTFS-Dateisystems fest.<br/>                                                                                                                          |
| [**ssktl- \_ Satz ( \_ Sparse)**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_sparse)<br/>                                       | Markiert die gekennzeichnete Datei als Sparse oder nicht als geringer Dichte. In einer sparsedatei erfordern große Bereiche von Nullen möglicherweise keine Datenträger Zuordnung.<br/>                                                               |
| [**ssctl \_ Set \_ zero \_ Data**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_zero_data)<br/>                                | Füllt einen angegebenen Bereich einer Datei mit Nullen (0).<br/>                                                                                                                                        |
| [**\_ \_ \_ beim Aufheben der Zuordnung wurde NULL festgelegt. \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_zero_on_deallocation)<br/>         | Gibt an, dass die Cluster eines NTFS-Dateisystem Datei Handles beim Aufheben der Zuordnung mit Nullen aufgefüllt werden sollen.<br/>                                                                             |
| [**ssctl- \_ Wartezeit \_ auf \_ Reparatur**](/windows/win32/api/winioctl/ni-winioctl-fsctl_wait_for_repair)<br/>                            | Gibt zurück, wenn die angegebenen Reparaturen abgeschlossen sind.<br/>                                                                                                                                        |



 

Die folgenden Steuerungs Codes werden bei der [Dateikomprimierung und-Dekomprimierung](file-compression-and-decompression.md)verwendet.

<dl>

[**Komprimierung von "f" \_ \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_compression)  
[**Komprimierung von ssctl- \_ Satz \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_compression)  
</dl>

Die folgenden Steuerungs Codes werden für [Objekt](distributed-link-tracking-and-object-identifiers.md)Bezeichner verwendet.

<dl>

[**\_Objekt-ID zum Erstellen oder zum Erstellen von \_ \_ \_ Objekten \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_create_or_get_object_id)  
[**ID des bsctl- \_ Lösch \_ Objekts \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_delete_object_id)  
[**ID des abzuruf- \_ \_ Objekts \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_object_id)  
[**Objekt-ID des ssctl- \_ Satzes \_ \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_object_id)  
[**Objekt-ID für das bsctl- \_ Set wurde \_ \_ \_ erweitert**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_object_id_extended)  
</dl>

Die folgenden Steuerungs Codes werden mit [opportunistischen Sperren](opportunistic-locks.md)verwendet.

<dl>

[**Schließen von "ssctl \_ opbatch \_ ACK" \_ steht \_ aus**](/windows/win32/api/winioctl/ni-winioctl-fsctl_opbatch_ack_close_pending)  
[**Ssctl- \_ Oplock- \_ break- \_ ACK Nr. \_ \_ 2**](/windows/win32/api/winioctl/ni-winioctl-fsctl_oplock_break_ack_no_2)  
[**losctl- \_ Oplock- \_ Abbruch \_ bestätigen**](/windows/win32/api/winioctl/ni-winioctl-fsctl_oplock_break_acknowledge)  
[**Benachrichtigung zum Abbrechen der Sperre von "f" \_ \_ \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_oplock_break_notify)  
[**Sperre für den ssctl- \_ Anforderungs \_ Batch \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_batch_oplock)  
[**\_Oplock für die Anforderung des volltextsfilters \_ \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_filter_oplock)  
[**Oplock für die ssctl- \_ Anforderung \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_oplock)  
[**Ssctl- \_ Anforderungs- \_ Oplock- \_ Ebene \_ 1**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_oplock_level_1)  
[**Ssctl- \_ Anforderungs- \_ Oplock- \_ Ebene \_ 2**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_oplock_level_2)  
</dl>

Die folgenden Kontrollcodes werden für [sparsesdateien](sparse-files.md)verwendet.

<dl>

[**\_ \_ zugeordnete Bereiche der ssctl-Abfrage \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_allocated_ranges)  
[**ssktl- \_ Satz ( \_ Sparse)**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_sparse)  
[**ssctl \_ Set \_ zero \_ Data**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_zero_data)  
</dl>

Die folgenden Steuerungs Codes werden mit dem Selbstreparatur Mechanismus von NTFS verwendet.

<dl>

[**ssctl \_ - \_ Reparatur**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_repair)  
[**Reparieren von "ssctl \_ initiieren" \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_initiate_repair)  
[**Reparatur von "ssctl \_ Set" \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_repair)  
[**ssctl- \_ Wartezeit \_ auf \_ Reparatur**](/windows/win32/api/winioctl/ni-winioctl-fsctl_wait_for_repair)  
</dl>

Die folgenden Steuerungs Codes werden mit UDF verwendet.

<dl>

[**mit "f \_ " \_ Medien \_ kompatibel machen**](/windows/win32/api/winioctl/ni-winioctl-fsctl_make_media_compatible)  
[**ssctl- \_ Abfrage zu Datenträger \_ Volume- \_ \_ \_ Informationen**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_on_disk_volume_info)  
[**Informationen zur ssktl- \_ Abfrage \_ \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_sparing_info)  
[**\_ \_ Fehler \_ Verwaltung bei der ssctl-Gruppe**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_defect_management)  
</dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Steuerungs Codes für die Verzeichnis Verwaltung](directory-management-control-codes.md)
</dt> <dt>

[Volumeverwaltungs-Steuerungscodes](volume-management-control-codes.md)
</dt> </dl>

 

