---
description: Stellt die Typen für die Haupt-und benutzerdefinierten Shimdatenbanken dar.
ms.assetid: e893963a-6130-4f65-b925-6f3d292fc86d
title: Shim-Datenbanktypen
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 789265ea945ce068d2b0b74e3358582d5e4ccd78
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103747673"
---
# <a name="shim-database-types"></a>Shim-Datenbanktypen

Stellt die Typen für die Haupt-und benutzerdefinierten Shimdatenbanken dar.



| Konstante/Wert                                                                                                                                                                                                                                                | BESCHREIBUNG                                                                                   |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------|
| <span id="SDB_DATABASE_MAIN"></span><span id="sdb_database_main"></span><dl> <dt>**SDB \_ Datenbank- \_ Haupt**</dt> - <dt>0x80000000</dt> </dl>                    | Die Hauptdatenbank. Wenn dieses Flag nicht vorhanden ist, handelt es sich bei der Datenbank um eine benutzerdefinierte Datenbank.<br/> |
| <span id="SDB_DATABASE_SHIM"></span><span id="sdb_database_shim"></span><dl> <dt>**SDB \_ \_Datenbankshim**</dt> <dt>0x00010000 bis</dt> </dl>                    | Die Datenbank enthält Anwendungs Einträge, für die eine shimmverbindung besteht.<br/>                           |
| <span id="SDB_DATABASE_MSI"></span><span id="sdb_database_msi"></span><dl> <dt>**SDB \_ Datenbank- \_ MSI**</dt> <dt>0x00020000</dt> </dl>                       | Die Datenbank enthält MSI-Einträge.<br/>                                                 |
| <span id="SDB_DATABASE_DRIVERS"></span><span id="sdb_database_drivers"></span><dl> <dt>**SDB \_ Daten Bank \_ Treiber**</dt> <dt>0x00040000</dt> </dl>           | Die Datenbank enthält Treiber Blockeinträge.<br/>                                        |
| <span id="SDB_DATABASE_DETAILS"></span><span id="sdb_database_details"></span><dl> <dt>**SDB \_ Daten Bank \_ Details**</dt> <dt>0x00080000</dt> </dl>           | Die Datenbank enthält AppHelp-Details.<br/>                                             |
| <span id="SDB_DATABASE_SP_DETAILS"></span><span id="sdb_database_sp_details"></span><dl> <dt>**SDB \_ Datenbank- \_ SP- \_ Details**</dt> <dt>0x00100000</dt> </dl> | Die Datenbank enthält die SP-AppHelp-Details.<br/>                                          |
| <span id="SDB_DATABASE_RESOURCE"></span><span id="sdb_database_resource"></span><dl> <dt>**SDB \_ Daten Bank \_ Ressource**</dt> <dt>0x00200000</dt> </dl>        | Die Ressourcen-DLL enthält AppHelp-Details.<br/>                                         |
| <span id="SDB_DATABASE_TYPE_MASK"></span><span id="sdb_database_type_mask"></span><dl> <dt>**SDB \_ Datenbank \_ - \_ typmaske**</dt> <dt>0xF 02f 0000</dt> </dl>    | Eine Maske, die zum Extrahieren von Hauptdaten Bankinformationen verwendet wird.<br/>                                  |
| <span id="SDB_DATABASE_MAIN_SHIM"></span><span id="sdb_database_main_shim"></span><dl> <dt>**Haupt- \_ \_ \_ Shim der SDB-Datenbank**</dt> </dl>                                                                    | SDB- \_ Datenbank \_ Shim \| SDB- \_ Datenbank \_ MSI \| SDB- \_ Datenbank \_ Main<br/>                   |
| <span id="SDB_DATABASE_MAIN_MSI"></span><span id="sdb_database_main_msi"></span><dl> <dt>**SDB- \_ Datenbank- \_ Haupt- \_ MSI**</dt> </dl>                                                                       | SDB- \_ Datenbank \_ MSI \| SDB- \_ Datenbank \_ Main<br/>                                          |
| <span id="SDB_DATABASE_MAIN_DRIVERS"></span><span id="sdb_database_main_drivers"></span><dl> <dt>**\_ \_ Haupt \_ Treiber der SDB-Datenbank**</dt> </dl>                                                           | SDB- \_ Daten Bank \_ Treiber \| SDB- \_ Datenbank \_ Main<br/>                                      |
| <span id="SDB_DATABASE_MAIN_DETAILS"></span><span id="sdb_database_main_details"></span><dl> <dt>**\_ \_ Haupt \_ Details der SDB-Datenbank**</dt> </dl>                                                           | SDB-Daten \_ Bank \_ Details \| SDB- \_ Datenbank \_ Main<br/>                                      |
| <span id="SDB_DATABASE_MAIN_SP_DETAILS"></span><span id="sdb_database_main_sp_details"></span><dl> <dt>**Haupt- \_ \_ SP- \_ \_ Details der SDB-Datenbank**</dt> </dl>                                                 | SDB- \_ Datenbank \_ SP \_ Details \| SDB- \_ Datenbank \_ Main<br/>                                  |
| <span id="SDB_DATABASE_MAIN_RESOURCE"></span><span id="sdb_database_main_resource"></span><dl> <dt>**\_ \_ Haupt \_ Ressource der SDB-Datenbank**</dt> </dl>                                                        | SDB- \_ Daten Bank \_ Ressource \| SDB- \_ Datenbank \_ Main<br/>                                     |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Sdbopendatabase**](sdbopendatabase.md)
</dt> </dl>

 

 




