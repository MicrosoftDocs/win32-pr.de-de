---
title: WINBIO_STORAGE_SCHEMA Struktur (winbio \_ types. h)
description: Beschreibt die Funktionen eines biometrischen Speicher Adapters.
ms.assetid: e4924803-5a1b-4e0a-b2cb-01d018d27ba1
keywords:
- WINBIO_STORAGE_SCHEMA Struktur Windows-Biometrieframework-API
- PWINBIO_STORAGE_SCHEMA Struktur Zeiger Windows-Biometrieframework API
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
ms.openlocfilehash: 28db23d55a7b3e43caaae5a88ca4bbf32fdf1178
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346762"
---
# <a name="winbio_storage_schema-structure"></a>Struktur des winbio- \_ Speicher \_ Schemas

In der Struktur des **winbio- \_ Speicher \_ Schemas** werden die Funktionen eines biometrischen Speicher Adapters beschrieben. Diese Struktur wird von der Funktion [**winbioenumdatenbanken**](/windows/desktop/api/Winbio/nf-winbio-winbioenumdatabases) verwendet.

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

**Biometricfactor**
</dt> <dd>

Der Typ der in der Datenbank gespeicherten biometrischen Messung.

</dd> <dt>

**DatabaseID**
</dt> <dd>

Eine GUID, die die Datenbank identifiziert.

</dd> <dt>

**DataFormat**
</dt> <dd>

Eine GUID, die das Format der Vorlagen in der Datenbank identifiziert.

</dd> <dt>

**Attribute**
</dt> <dd>

Informationen zu den Merkmalen der Datenbank. Hierbei kann es sich um ein bitweises **or** der folgenden Konstanten handeln.



| Wert                                                                                                                                                                                                                                                                              | Bedeutung                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <span id="WINBIO_DATABASE_FLAG_MASK"></span><span id="winbio_database_flag_mask"></span><dl> <dt>**Winbio \_ \_Datenbankflag- \_ Maske**</dt> <dt>0xFFFF0000</dt> </dl>                | Stellt eine Maske für die Flagbits dar.<br/>                     |
| <span id="WINBIO_DATABASE_FLAG_REMOTE"></span><span id="winbio_database_flag_remote"></span><dl> <dt>**Winbio \_ \_Datenbankflag \_ Remote**</dt> <dt>0x00020000</dt> </dl>          | Die Datenbank befindet sich auf einem Remote Computer.<br/>               |
| <span id="WINBIO_DATABASE_FLAG_REMOVABLE"></span><span id="winbio_database_flag_removable"></span><dl> <dt>**Winbio \_ \_Datenbankflag \_**</dt> -Wechsel <dt>0x00010000 bis</dt> </dl> | Die Datenbank befindet sich auf einem Wechsel Datenträger.<br/>               |
| <span id="WINBIO_DATABASE_TYPE_DBMS"></span><span id="winbio_database_type_dbms"></span><dl> <dt>**Winbio \_ Database \_ Type \_ DBMS**</dt> <dt>0x00000002</dt> </dl>                | Die Datenbank wird von einem Datenbankverwaltungssystem verwaltet.<br/> |
| <span id="WINBIO_DATABASE_TYPE_FILE"></span><span id="winbio_database_type_file"></span><dl> <dt>**Winbio \_ \_ \_ Dateityp Datei**</dt> <dt>0x00000001</dt> </dl>                | Die Datenbank ist in einer Datei enthalten.<br/>                     |
| <span id="WINBIO_DATABASE_TYPE_MASK"></span><span id="winbio_database_type_mask"></span><dl> <dt>**Winbio \_ Daten \_ Bank \_ typmaske**</dt> <dt>0X0000FFFF</dt> </dl>                | Stellt eine Maske für die typbits dar.<br/>                     |
| <span id="WINBIO_DATABASE_TYPE_ONCHIP"></span><span id="winbio_database_type_onchip"></span><dl> <dt>**Winbio \_ Database \_ Type \_ Onchip**</dt> <dt>0x00000003</dt> </dl>          | Die Datenbank befindet sich auf dem biometrischen Sensor.<br/>            |
| <span id="WINBIO_DATABASE_TYPE_SMARTCARD"></span><span id="winbio_database_type_smartcard"></span><dl> <dt>**Winbio \_ Database \_ Type \_ Smartcard**</dt> <dt>0x00000004</dt> </dl> | Die Datenbank befindet sich auf einer Smartcard.<br/>                    |



 

</dd> <dt>

**FilePath**
</dt> <dd>

Der Pfad und der Dateiname der Datenbank, wenn Sie sich auf dem Computer Datenträger befindet.

</dd> <dt>

**ConnectionString**
</dt> <dd>

Ein Zeichen folgen Wert, der an einen Datenbankserver gesendet werden kann, um die Datenbank zu identifizieren.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                                                       |
| Header<br/>                   | <dl> <dt>Winbio \_ types. h (Include winbio. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Client Anwendungs Strukturen](client-application-structures.md)
</dt> <dt>

[**Winbioenumdatenbanken**](/windows/desktop/api/Winbio/nf-winbio-winbioenumdatabases)
</dt> </dl>

 

 





