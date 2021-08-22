---
description: Stellt die Typen für Hauptdatenbanken und benutzerdefinierte Shimdatenbanken dar.
ms.assetid: e893963a-6130-4f65-b925-6f3d292fc86d
title: Shim-Datenbanktypen
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5cc36cbb198570618fbd1a6524e4e7c6dc6812fb01bd74fe04cf1bd91b31f9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075924"
---
# <a name="shim-database-types"></a>Shim-Datenbanktypen

Stellt die Typen für Hauptdatenbanken und benutzerdefinierte Shimdatenbanken dar.



| Konstante/Wert                                                                                                                                                                                                                                                | Beschreibung                                                                                   |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------|
| <span id="SDB_DATABASE_MAIN"></span><span id="sdb_database_main"></span><dl> <dt>**SDB \_ DATABASE \_ MAIN**</dt> <dt>0x80000000</dt> </dl>                    | Die Hauptdatenbank. Wenn dieses Flag nicht vorhanden ist, ist die Datenbank eine benutzerdefinierte Datenbank.<br/> |
| <span id="SDB_DATABASE_SHIM"></span><span id="sdb_database_shim"></span><dl> <dt>**SDB \_ \_DATENBANK-SHIM 0x00010000**</dt> <dt></dt> </dl>                    | Die Datenbank enthält Anwendungseinträge, für die ein Shiming erstellt werden soll.<br/>                           |
| <span id="SDB_DATABASE_MSI"></span><span id="sdb_database_msi"></span><dl> <dt>**SDB \_ \_DATENBANK-MSI 0x00020000**</dt> <dt></dt> </dl>                       | Die Datenbank enthält MSI-Einträge.<br/>                                                 |
| <span id="SDB_DATABASE_DRIVERS"></span><span id="sdb_database_drivers"></span><dl> <dt>**SDB \_ \_DATENBANKTREIBER**</dt> <dt>0X00040000</dt> </dl>           | Die Datenbank enthält Treiberblockeinträge.<br/>                                        |
| <span id="SDB_DATABASE_DETAILS"></span><span id="sdb_database_details"></span><dl> <dt>**SDB \_ \_DATENBANKDETAILS**</dt> <dt>0X00080000</dt> </dl>           | Die Datenbank enthält Apphelp-Details.<br/>                                             |
| <span id="SDB_DATABASE_SP_DETAILS"></span><span id="sdb_database_sp_details"></span><dl> <dt>**SDB \_ \_ \_ DATENBANK-SP-0X00100000**</dt> <dt></dt> </dl> | Die Datenbank enthält SP Apphelp-Details.<br/>                                          |
| <span id="SDB_DATABASE_RESOURCE"></span><span id="sdb_database_resource"></span><dl> <dt>**SDB \_ DATABASE \_ RESOURCE**</dt> <dt>0x00200000</dt> </dl>        | Die Ressourcen-DLL enthält Apphelp-Details.<br/>                                         |
| <span id="SDB_DATABASE_TYPE_MASK"></span><span id="sdb_database_type_mask"></span><dl> <dt>**SDB \_ DATABASE \_ TYPE \_ MASK**</dt> <dt>0xF02F0000</dt> </dl>    | Eine Maske, die zum Extrahieren von Hauptdatenbankinformationen verwendet wird.<br/>                                  |
| <span id="SDB_DATABASE_MAIN_SHIM"></span><span id="sdb_database_main_shim"></span><dl> <dt>**SDB \_ DATABASE \_ MAIN \_ SHIM**</dt> </dl>                                                                    | SDB \_ DATABASE \_ SHIM \| SDB \_ DATABASE \_ MSI \| SDB \_ DATABASE \_ MAIN<br/>                   |
| <span id="SDB_DATABASE_MAIN_MSI"></span><span id="sdb_database_main_msi"></span><dl> <dt>**SDB \_ DATABASE \_ MAIN \_ MSI**</dt> </dl>                                                                       | SDB \_ DATABASE \_ MSI \| SDB \_ DATABASE \_ MAIN<br/>                                          |
| <span id="SDB_DATABASE_MAIN_DRIVERS"></span><span id="sdb_database_main_drivers"></span><dl> <dt>**HAUPTTREIBER \_ DER SDB-DATENBANK \_ \_**</dt> </dl>                                                           | \_SDB-DATENBANKTREIBER \_ \| SDB \_ DATABASE \_ MAIN<br/>                                      |
| <span id="SDB_DATABASE_MAIN_DETAILS"></span><span id="sdb_database_main_details"></span><dl> <dt>**\_SDB-DATENBANK \_ – \_ HAUPTDETAILS**</dt> </dl>                                                           | SDB \_ DATABASE \_ DETAILS \| SDB \_ DATABASE \_ MAIN<br/>                                      |
| <span id="SDB_DATABASE_MAIN_SP_DETAILS"></span><span id="sdb_database_main_sp_details"></span><dl> <dt>**SDB \_ DATABASE \_ MAIN \_ SP \_ DETAILS**</dt> </dl>                                                 | SDB \_ DATABASE \_ SP \_ DETAILS \| SDB \_ DATABASE \_ MAIN<br/>                                  |
| <span id="SDB_DATABASE_MAIN_RESOURCE"></span><span id="sdb_database_main_resource"></span><dl> <dt>**\_HAUPTRESSOURCE DER SDB-DATENBANK \_ \_**</dt> </dl>                                                        | SDB \_ DATABASE \_ RESOURCE \| SDB \_ DATABASE \_ MAIN<br/>                                     |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**SdbOpenDatabase**](sdbopendatabase.md)
</dt> </dl>

 

 




