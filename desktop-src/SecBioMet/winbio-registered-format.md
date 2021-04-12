---
title: WINBIO_REGISTERED_FORMAT Struktur (winbio \_ types. h)
description: Gibt ein registriertes Datenformat als Besitzer/Format-Paar an.
ms.assetid: a178840e-81cc-4dd3-9d80-a181fa7fa888
keywords:
- WINBIO_REGISTERED_FORMAT Struktur Windows-Biometrieframework-API
- PWINBIO_REGISTERED_FORMAT Struktur Zeiger Windows-Biometrieframework API
topic_type:
- apiref
api_name:
- WINBIO_REGISTERED_FORMAT
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f45293fe95627c7dfad4c9c51eb7fa74ad1738c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517807"
---
# <a name="winbio_registered_format-structure"></a>Winbio- \_ registrierte \_ Format Struktur

Die Struktur " **winbio- \_ registrierter \_ Format** " gibt ein registriertes Datenformat als Besitzer/Format-Paar an.

## <a name="syntax"></a>Syntax


```C++
typedef struct _WINBIO_REGISTERED_FORMAT {
  USHORT Owner;
  USHORT Type;
} WINBIO_REGISTERED_FORMAT, *PWINBIO_REGISTERED_FORMAT;
```



## <a name="members"></a>Member

<dl> <dt>

**Besitzer**
</dt> <dd>

Einen von IBIA (International biometrische Industry Association) zugewiesenen Besitzer Wert.

</dd> <dt>

**Type**
</dt> <dd>

Ein vom Besitzer zugewiesenes Format.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Da Windows derzeit nur Fingerabdruckleser unterstützt, sollten die folgenden Werte in der Struktur der im **winbio \_ registrierten \_ Format** verwendet werden.



| Konstante                                    | Bedeutung                                                                                                               |
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| Winbio \_ ANSI \_ 381- \_ Format \_ Besitzer<br/> | International Committee for Information Technology Standards (INCITS) Technical Committee M1 (Biometrics).<br/> |
| Winbio \_ ANSI \_ 381 \_ - \_ Formattyp<br/>  | ANSI-Datenaustausch (381 fingerbild-basiertes Datenaustauschformat).<br/>                                                |



 

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

[**Winbio \_ ANSI \_ 381- \_ Format Konstanten**](winbio-ansi-381-format-constants.md)
</dt> <dt>

[**Winbio \_ BDB \_ ANSI \_ 381- \_ Header**](winbio-bdb-ansi-381-header.md)
</dt> <dt>

[**winbio- \_ Bir- \_ Header**](winbio-bir-header.md)
</dt> </dl>

 

 





