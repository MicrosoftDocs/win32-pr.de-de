---
title: WINBIO_DATABASE_TYPE Konstanten (winbio \_ types. h)
description: Flags, die für den Attribute-Member der Struktur des winbio- \_ Speicher Schemas verwendet werden können \_ .
ms.assetid: 07e7e91c-3ca6-41cd-a2c7-ac43bb5156a6
topic_type:
- apiref
api_name:
- WINBIO_DATABASE_TYPE_MASK
- WINBIO_DATABASE_TYPE_FILE
- WINBIO_DATABASE_TYPE_DBMS
- WINBIO_DATABASE_TYPE_ONCHIP
- WINBIO_DATABASE_TYPE_SMARTCARD
- WINBIO_DATABASE_FLAG_MASK
- WINBIO_DATABASE_FLAG_REMOVABLE
- WINBIO_DATABASE_FLAG_REMOTE
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acd67f49c5fa689fb4418789aae7c4d6c9a305a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741528"
---
# <a name="winbio_database_type-constants"></a>Winbio- \_ Daten \_ Banktyp Konstanten

Die folgenden Flags können für den **Attribute** -Member der Struktur des [**winbio- \_ Speicher \_ Schemas**](winbio-storage-schema.md) verwendet werden.



| Konstante/Wert                                                                                                                                                                                                                                                                     | BESCHREIBUNG                                                                                                                  |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DATABASE_TYPE_MASK"></span><span id="winbio_database_type_mask"></span><dl> <dt>**Winbio \_ Daten \_ Bank \_ typmaske**</dt> <dt>0X0000FFFF</dt> </dl>                | Stellt eine Maske für alle \_ \_ typbits dar.<br/>                                                                   |
| <span id="WINBIO_DATABASE_TYPE_FILE"></span><span id="winbio_database_type_file"></span><dl> <dt>**Winbio \_ \_ \_ Dateityp Datei**</dt> <dt>0x00000001</dt> </dl>                | Die Datenbank ist in einer Datei enthalten.<br/>                                                                              |
| <span id="WINBIO_DATABASE_TYPE_DBMS"></span><span id="winbio_database_type_dbms"></span><dl> <dt>**Winbio \_ Database \_ Type \_ DBMS**</dt> <dt>0x00000002</dt> </dl>                | Die Datenbank wird von einer externen DBMS-Komponente (Database Management System) verwaltet, z. b. Microsoft SQL Server.<br/> |
| <span id="WINBIO_DATABASE_TYPE_ONCHIP"></span><span id="winbio_database_type_onchip"></span><dl> <dt>**Winbio \_ Database \_ Type \_ Onchip**</dt> <dt>0x00000003</dt> </dl>          | Die Datenbank befindet sich auf dem biometrischen Sensor.<br/>                                                                     |
| <span id="WINBIO_DATABASE_TYPE_SMARTCARD"></span><span id="winbio_database_type_smartcard"></span><dl> <dt>**Winbio \_ Database \_ Type \_ Smartcard**</dt> <dt>0x00000004</dt> </dl> | Die Datenbank befindet sich auf einer Smartcard.<br/>                                                                             |
| <span id="WINBIO_DATABASE_FLAG_MASK"></span><span id="winbio_database_flag_mask"></span><dl> <dt>**Winbio \_ \_Datenbankflag- \_ Maske**</dt> <dt>0xFFFF0000</dt> </dl>                | Stellt eine Maske für alle \_ \_ Flagbits dar.<br/>                                                                   |
| <span id="WINBIO_DATABASE_FLAG_REMOVABLE"></span><span id="winbio_database_flag_removable"></span><dl> <dt>**Winbio \_ \_Datenbankflag \_**</dt> -Wechsel <dt>0x00010000 bis</dt> </dl> | Das Speichermedium mit der Datenbank kann physisch vom Computer entfernt werden.<br/>                           |
| <span id="WINBIO_DATABASE_FLAG_REMOTE"></span><span id="winbio_database_flag_remote"></span><dl> <dt>**Winbio \_ \_Datenbankflag \_ Remote**</dt> <dt>0x00020000</dt> </dl>          | Die Datenbank befindet sich auf einem Remote Computer.<br/>                                                                        |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                                                       |
| Header<br/>                   | <dl> <dt>Winbio \_ types. h (Include winbio. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Client Anwendungs Konstanten](client-application-constants.md)
</dt> </dl>

 

 





