---
title: WINBIO_DATABASE_TYPE Konstanten (Winbio \_ types.h)
description: Flags, die für den Attributes-Member der WINBIO \_ STORAGE \_ SCHEMA-Struktur verwendet werden können.
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
ms.openlocfilehash: ba06dcd8809e53c5cfdf552a2c2c80b4d51faa5b80594b72ea1b50e2e7a2c0a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118910732"
---
# <a name="winbio_database_type-constants"></a>WINBIO \_ DATABASE \_ TYPE-Konstanten

Die folgenden Flags können für den **Attributes-Member** der [**WINBIO \_ STORAGE \_ SCHEMA-Struktur verwendet**](winbio-storage-schema.md) werden.



| Konstante/Wert                                                                                                                                                                                                                                                                     | Beschreibung                                                                                                                  |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DATABASE_TYPE_MASK"></span><span id="winbio_database_type_mask"></span><dl> <dt>**WINBIO \_ DATABASE \_ TYPE \_ MASK**</dt> <dt>0x0000FFFF</dt> </dl>                | Stellt eine Maske für alle \_ \_ TYPE-Bits dar.<br/>                                                                   |
| <span id="WINBIO_DATABASE_TYPE_FILE"></span><span id="winbio_database_type_file"></span><dl> <dt>**WINBIO \_ DATABASE \_ TYPE \_ FILE**</dt> <dt>0x00000001</dt> </dl>                | Die Datenbank ist in einer Datei enthalten.<br/>                                                                              |
| <span id="WINBIO_DATABASE_TYPE_DBMS"></span><span id="winbio_database_type_dbms"></span><dl> <dt>**WINBIO \_ DATABASE \_ TYPE \_ DBMS**</dt> <dt>0x00000002</dt> </dl>                | Die Datenbank wird von einer externen DbMS-Komponente (Database Management System) verwaltet, z. B. Microsoft SQL Server.<br/> |
| <span id="WINBIO_DATABASE_TYPE_ONCHIP"></span><span id="winbio_database_type_onchip"></span><dl> <dt>**WINBIO \_ DATENBANKTYP \_ \_ ONCHIP-0X00000003**</dt> <dt></dt> </dl>          | Die Datenbank befindet sich auf dem biometrischen Sensor.<br/>                                                                     |
| <span id="WINBIO_DATABASE_TYPE_SMARTCARD"></span><span id="winbio_database_type_smartcard"></span><dl> <dt>**WINBIO \_ \_ \_ SMARTCARD-0X00000004**</dt> <dt></dt> </dl> | Die Datenbank befindet sich auf einer Smartcard.<br/>                                                                             |
| <span id="WINBIO_DATABASE_FLAG_MASK"></span><span id="winbio_database_flag_mask"></span><dl> <dt>**WINBIO \_ DATABASE \_ FLAG \_ MASK**</dt> <dt>0xFFFF0000</dt> </dl>                | Stellt eine Maske für alle \_ \_ FLAG-Bits dar.<br/>                                                                   |
| <span id="WINBIO_DATABASE_FLAG_REMOVABLE"></span><span id="winbio_database_flag_removable"></span><dl> <dt>**WINBIO \_ \_WECHSELDATENTRÄGER \_ MIT DATENBANKFLAG**</dt> <dt>0X00010000</dt> </dl> | Das Speichermedium, das die Datenbank enthält, kann physisch vom Computer entfernt werden.<br/>                           |
| <span id="WINBIO_DATABASE_FLAG_REMOTE"></span><span id="winbio_database_flag_remote"></span><dl> <dt>**WINBIO \_ DATABASE \_ FLAG \_ REMOTE**</dt> <dt>0x00020000</dt> </dl>          | Die Datenbank befindet sich auf einem Remotecomputer.<br/>                                                                        |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                                                       |
| Header<br/>                   | <dl> <dt>Winbio \_ types.h (einschließlich Winbio.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Clientanwendungskonst constants](client-application-constants.md)
</dt> </dl>

 

 





