---
title: WINBIO_STORAGE_SCHEMA -Struktur (Winbio \_ types.h)
description: Beschreibt die Funktionen eines biometrischen Speicheradapters.
ms.assetid: e4924803-5a1b-4e0a-b2cb-01d018d27ba1
keywords:
- WINBIO_STORAGE_SCHEMA Struktur Windows Biometrieframework-API
- PWINBIO_STORAGE_SCHEMA Strukturzeiger für Windows Biometrieframework-API
topic_type:
- apiref
api_name:
- WINBIO_STORAGE_SCHEMA
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bc0bd0d61814b4133c3789b0c8119edcaf79945452cc26aa313504c055ac2f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118909257"
---
# <a name="winbio_storage_schema-structure"></a>WINBIO \_ STORAGE \_ SCHEMA-Struktur

Die **WINBIO \_ STORAGE \_ SCHEMA-Struktur** beschreibt die Funktionen eines biometrischen Speicheradapters. Diese Struktur wird von der [**WinBioEnumDatabases-Funktion**](/windows/desktop/api/Winbio/nf-winbio-winbioenumdatabases) verwendet.

## <a name="syntax"></a>Syntax


```C++
typedef struct _WINBIO_STORAGE_SCHEMA {
  WINBIO_BIOMETRIC_TYPE BiometricFactor;
  WINBIO_UUID           DatabaseId;
  WINBIO_UUID           DataFormat;
  ULONG                 Attributes;
  WINBIO_STRING         FilePath;
  WINBIO_STRING         ConnectionString;
} WINBIO_STORAGE_SCHEMA, *PWINBIO_STORAGE_SCHEMA;
```



## <a name="members"></a>Member

<dl> <dt>

**BiometricFactor**
</dt> <dd>

Der Typ der biometrischen Messung, die in der Datenbank gespeichert ist.

</dd> <dt>

**Databaseid**
</dt> <dd>

Eine GUID, die die Datenbank identifiziert.

</dd> <dt>

**Dataformat**
</dt> <dd>

Eine GUID, die das Format der Vorlagen in der Datenbank identifiziert.

</dd> <dt>

**Attribute**
</dt> <dd>

Informationen zu den Merkmalen der Datenbank. Dies kann ein **bitweises OR** der folgenden Konstanten sein.



| Wert                                                                                                                                                                                                                                                                              | Bedeutung                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <span id="WINBIO_DATABASE_FLAG_MASK"></span><span id="winbio_database_flag_mask"></span><dl> <dt>**WINBIO \_ DATABASE \_ FLAG \_ MASK**</dt> <dt>0xFFFF0000</dt> </dl>                | Stellt eine Maske für die Flagbits dar.<br/>                     |
| <span id="WINBIO_DATABASE_FLAG_REMOTE"></span><span id="winbio_database_flag_remote"></span><dl> <dt>**WINBIO \_ DATABASE \_ FLAG \_ REMOTE**</dt> <dt>0x00020000</dt> </dl>          | Die Datenbank befindet sich auf einem Remotecomputer.<br/>               |
| <span id="WINBIO_DATABASE_FLAG_REMOVABLE"></span><span id="winbio_database_flag_removable"></span><dl> <dt>**WINBIO \_ \_WECHSELDATENTRÄGER \_ MIT DATENBANKFLAG**</dt> <dt>0X00010000</dt> </dl> | Die Datenbank befindet sich auf einem Wechseldatenträger.<br/>               |
| <span id="WINBIO_DATABASE_TYPE_DBMS"></span><span id="winbio_database_type_dbms"></span><dl> <dt>**WINBIO \_ DATABASE \_ TYPE \_ DBMS**</dt> <dt>0x00000002</dt> </dl>                | Die Datenbank wird von einem Datenbank-Managementsystem verwaltet.<br/> |
| <span id="WINBIO_DATABASE_TYPE_FILE"></span><span id="winbio_database_type_file"></span><dl> <dt>**WINBIO \_ DATABASE \_ TYPE \_ FILE**</dt> <dt>0x00000001</dt> </dl>                | Die Datenbank ist in einer Datei enthalten.<br/>                     |
| <span id="WINBIO_DATABASE_TYPE_MASK"></span><span id="winbio_database_type_mask"></span><dl> <dt>**WINBIO \_ DATABASE \_ TYPE \_ MASK**</dt> <dt>0x0000FFFF</dt> </dl>                | Stellt eine Maske für die Typbits dar.<br/>                     |
| <span id="WINBIO_DATABASE_TYPE_ONCHIP"></span><span id="winbio_database_type_onchip"></span><dl> <dt>**WINBIO \_ DATENBANKTYP \_ \_ ONCHIP-0X00000003**</dt> <dt></dt> </dl>          | Die Datenbank befindet sich auf dem biometrischen Sensor.<br/>            |
| <span id="WINBIO_DATABASE_TYPE_SMARTCARD"></span><span id="winbio_database_type_smartcard"></span><dl> <dt>**WINBIO \_ \_ \_ SMARTCARD-0X00000004**</dt> <dt></dt> </dl> | Die Datenbank befindet sich auf einer Smartcard.<br/>                    |



 

</dd> <dt>

**Filepath**
</dt> <dd>

Der Pfad und dateiname der Datenbank, wenn sie sich auf dem Computerdatenträger befindet.

</dd> <dt>

**Connectionstring**
</dt> <dd>

Ein Zeichenfolgenwert, der zur Identifizierung der Datenbank an einen Datenbankserver gesendet werden kann.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                                                       |
| Header<br/>                   | <dl> <dt>Winbio \_ types.h (einschließlich Winbio.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Clientanwendungsstrukturen](client-application-structures.md)
</dt> <dt>

[**WinBioEnumDatabases**](/windows/desktop/api/Winbio/nf-winbio-winbioenumdatabases)
</dt> </dl>

 

 





