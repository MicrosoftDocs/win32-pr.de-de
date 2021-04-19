---
description: Transaktionale NTFS-Strukturen (TxF).
ms.assetid: 85b3cf8e-bff3-4693-b00e-64bf5d1f5065
title: TxF-Strukturen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d490f608ef9ebfa6906d1acffa374a0c9327489b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348459"
---
# <a name="txf-structures"></a>TxF-Strukturen

Transaktionale NTFS (TxF) bietet die folgenden Strukturen.

## <a name="in-this-section"></a>In diesem Abschnitt



| Struktur                                                                                                    | BESCHREIBUNG                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**txfs \_ - \_ Informationen zur Miniversion erstellen \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_create_miniversion_info)<br/>                           | Enthält die Versionsinformationen über die Triggerszenarios, die von [**\_ sxfs \_ Create \_ Triggerszenarios**](/windows/win32/api/winioctl/ni-winioctl-fsctl_txfs_create_miniversion)erstellt wurde.<br/>                                            |
| [**txfs \_ - \_ Informationen zur Metadatenausgabe \_ \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_get_metadata_info_out)<br/>                              | Enthält die Versionsinformationen zur Triggerszenarios, die erstellt wird.<br/>                                                                                                                 |
| [**TxF- \_ ID**](/windows/desktop/api/TxfW32/ns-txfw32-txf_id)<br/>                                                                         | Stellt einen eindeutigen Bezeichner im Kontext der Ressourcen-Manager dar.<br/>                                                                                                              |
| [**txfs \_ erhalten \_ transaktive \_ Version**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_get_transacted_version)<br/>                             | Enthält die Informationen über die Basisversion und die neueste Version der angegebenen Datei.<br/>                                                                                                      |
| [**txfs-Liste der von der \_ \_ Transaktion \_ gesperrten \_ Dateien**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_list_transaction_locked_files)<br/>              | Enthält eine Liste der Dateien, die von einem transaktiven Writer gesperrt wurden.<br/>                                                                                                                                 |
| [**Eintrag der Liste der in txfs \_ \_ \_ gesperrten \_ Dateien \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_list_transaction_locked_files_entry)<br/> | Enthält Informationen zu einer gesperrten Transaktion.<br/>                                                                                                                                        |
| [**txfs- \_ Listen \_ Transaktionen**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_list_transactions)<br/>                                        | Enthält eine Liste mit Transaktionen.<br/>                                                                                                                                                        |
| [**Eintrag für txfs- \_ Listen \_ Transaktionen \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_list_transactions_entry)<br/>                           | Enthält Informationen zu einer Transaktion.<br/>                                                                                                                                               |
| [**Datei des TxF- \_ Protokoll \_ Datensatzes \_ betroffen \_**](/windows/desktop/api/TxfW32/ns-txfw32-txf_log_record_affected_file)<br/>                          | Enthält Informationen zu einer Datei, die von einer Transaktion betroffen war.<br/>                                                                                                                     |
| [**TxF- \_ Protokoll \_ Daten Satz \_ Basis**](/windows/desktop/api/TxfW32/ns-txfw32-txf_log_record_base)<br/>                                             | Enthält die grundlegenden Datensatzinformationen.<br/>                                                                                                                                                  |
| [**TxF- \_ Protokoll \_ Daten Satz \_ Abschneiden**](/windows/desktop/api/TxfW32/ns-txfw32-txf_log_record_truncate)<br/>                                     | Enthält den Datensatz für einen TRUNCATE-Vorgang.<br/>                                                                                                                                           |
| [**TxF- \_ Protokoll \_ Daten Satz \_ Schreibvorgang**](/windows/desktop/api/TxfW32/ns-txfw32-txf_log_record_write)<br/>                                           | Enthält den Datensatz für einen Schreibvorgang.<br/>                                                                                                                                              |
| [**txfs \_ Modify \_ RM**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_modify_rm)<br/>                                                        | Enthält die Informationen, die beim Ändern von Protokoll Parametern und Protokollierungs Modus für einen sekundären Ressourcen-Manager erforderlich sind.<br/>                                                                      |
| [**Informationen zu txfs- \_ Abfrage \_ RM \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_query_rm_information)<br/>                                 | Enthält Informationen zum Ressourcen-Manager (RM).<br/>                                                                                                                                   |
| [**txfs- \_ Lese \_ Sicherungs \_ Informationen \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_read_backup_information_out)<br/>                  | Enthält eine spezifische Transaktions-NTFS-Struktur (TxF). Diese Informationen sollten nur verwendet werden, wenn [**txfs- \_ Schreib \_ Sicherungs \_ Informationen**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_write_backup_information)aufgerufen werden.<br/>    |
| [**txfs-Sicherungs \_ Punkt \_ Informationen**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_savepoint_information)<br/>                                | Die [**FSCTL \_ txfs-Sicherungs \_ Punkt \_ Informations**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_savepoint_information) Struktur gibt die Aktion an, die ausgeführt werden soll, und für welche Transaktion.<br/>                                      |
| [**\_ \_ aktive \_ Informationen zur txfs-Transaktion**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_transaction_active_info)<br/>                           | Enthält das Flag, das angibt, ob Transaktionen aktiv waren oder nicht, als eine Momentaufnahme erstellt wurde.<br/>                                                                                     |
| [**txfs- \_ Schreib \_ Sicherungs \_ Informationen**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_write_backup_information)<br/>                         | Enthält eine spezifische Transaktions-NTFS-Struktur (TxF). Diese Informationen sollten nur verwendet werden, wenn [**txfs- \_ Schreib \_ Sicherungs \_ Informationen**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_read_backup_information_out)aufgerufen werden.<br/> |



 

 

