---
description: Transaktionale NTFS-Strukturen (TxF).
ms.assetid: 85b3cf8e-bff3-4693-b00e-64bf5d1f5065
title: TxF-Strukturen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac6acdbaac0798ef2dac3b3fefad9a1f5de505eb9781316fca82d45cfad26af0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119765840"
---
# <a name="txf-structures"></a>TxF-Strukturen

Transactional NTFS (TxF) stellt die folgenden Strukturen zur Verfügung.

## <a name="in-this-section"></a>In diesem Abschnitt



| Struktur                                                                                                    | Beschreibung                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**TXFS \_ CREATE \_ MINIVERSION \_ INFO**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_create_miniversion_info)<br/>                           | Enthält die Versionsinformationen zur Miniversion, die von [**FSCTL \_ TXFS \_ CREATE \_ MINIVERSION erstellt wurde.**](/windows/win32/api/winioctl/ni-winioctl-fsctl_txfs_create_miniversion)<br/>                                            |
| [**TXFS: \_ ABRUFEN \_ VON \_ \_ METADATENINFORMATIONEN**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_get_metadata_info_out)<br/>                              | Enthält die Versionsinformationen über die miniversion, die erstellt wird.<br/>                                                                                                                 |
| [**TXF-ID \_**](/windows/desktop/api/TxfW32/ns-txfw32-txf_id)<br/>                                                                         | Stellt einen eindeutigen Bezeichner innerhalb des Kontexts der Resource Manager.<br/>                                                                                                              |
| [**TXFS \_ GET \_ TRANSACTED \_ VERSION**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_get_transacted_version)<br/>                             | Enthält die Informationen über die Basisversion und die neuesten Versionen der angegebenen Datei.<br/>                                                                                                      |
| [**TXFS \_ LIST \_ TRANSACTION \_ LOCKED \_ FILES**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_list_transaction_locked_files)<br/>              | Enthält eine Liste von Dateien, die von einem transaktiven Writer gesperrt wurden.<br/>                                                                                                                                 |
| [**TXFS LIST TRANSACTION LOCKED FILES ENTRY (EINTRAG FÜR \_ \_ \_ \_ GESPERRTE TXFS-DATEIEN \_ AUFLISTEN)**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_list_transaction_locked_files_entry)<br/> | Enthält Informationen zu einer gesperrten Transaktion.<br/>                                                                                                                                        |
| [**\_TXFS-LISTENTRANSAKTIONEN \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_list_transactions)<br/>                                        | Enthält eine Liste von Transaktionen.<br/>                                                                                                                                                        |
| [**\_TXFS-EINTRAG \_ "TRANSAKTIONEN \_ AUFLISTEN"**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_list_transactions_entry)<br/>                           | Enthält Informationen zu einer Transaktion.<br/>                                                                                                                                               |
| [**BETROFFENE \_ \_ TXF-PROTOKOLLDATENSATZDATEI \_ \_**](/windows/desktop/api/TxfW32/ns-txfw32-txf_log_record_affected_file)<br/>                          | Enthält Informationen zu einer Datei, die von einer Transaktion betroffen war.<br/>                                                                                                                     |
| [**\_ \_ TXF-PROTOKOLLDATENSATZBASIS \_**](/windows/desktop/api/TxfW32/ns-txfw32-txf_log_record_base)<br/>                                             | Enthält die grundlegenden Datensatzinformationen.<br/>                                                                                                                                                  |
| [**TXF \_ LOG \_ RECORD \_ TRUNCATE**](/windows/desktop/api/TxfW32/ns-txfw32-txf_log_record_truncate)<br/>                                     | Enthält den Datensatz für einen Abschneidevorgang.<br/>                                                                                                                                           |
| [**TXF \_ LOG \_ RECORD \_ WRITE**](/windows/desktop/api/TxfW32/ns-txfw32-txf_log_record_write)<br/>                                           | Enthält den Datensatz für einen Schreibvorgang.<br/>                                                                                                                                              |
| [**TXFS \_ MODIFY \_ RM**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_modify_rm)<br/>                                                        | Enthält die Informationen, die beim Ändern von Protokollparametern und des Protokollierungsmodus für einen sekundären Ressourcen-Manager erforderlich sind.<br/>                                                                      |
| [**TXFS \_ QUERY \_ RM \_ INFORMATION**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_query_rm_information)<br/>                                 | Enthält Informationen zum Ressourcen-Manager (RM).<br/>                                                                                                                                   |
| [**TXFS \_ LIEST \_ \_ SICHERUNGSINFORMATIONEN \_ AUS.**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_read_backup_information_out)<br/>                  | Enthält eine TxF-spezifische (Transactional NTFS)-Struktur. Diese Informationen sollten nur beim Aufrufen von [**TXFS \_ WRITE BACKUP INFORMATION verwendet \_ \_ werden.**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_write_backup_information)<br/>    |
| [**TXFS \_ SAVEPOINT \_ INFORMATION**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_savepoint_information)<br/>                                | Die [**FSCTL \_ TXFS \_ SAVEPOINT \_ INFORMATION-Struktur**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_savepoint_information) gibt an, welche Aktion ausgeführt werden soll und für welche Transaktion.<br/>                                      |
| [**TXFS \_ TRANSACTION \_ ACTIVE \_ INFO**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_transaction_active_info)<br/>                           | Enthält das Flag, das angibt, ob Transaktionen aktiv waren, als eine Momentaufnahme erstellt wurde.<br/>                                                                                     |
| [**TXFS \_ WRITE \_ BACKUP \_ INFORMATION**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_write_backup_information)<br/>                         | Enthält eine TxF-spezifische (Transactional NTFS)-Struktur. Diese Informationen sollten nur beim Aufrufen von [**TXFS \_ WRITE BACKUP INFORMATION verwendet \_ \_ werden.**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_read_backup_information_out)<br/> |



 

 

