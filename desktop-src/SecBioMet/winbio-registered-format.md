---
title: WINBIO_REGISTERED_FORMAT-Struktur (Winbio \_ types.h)
description: Gibt ein registriertes Datenformat als Besitzer-/Formatpaar an.
ms.assetid: a178840e-81cc-4dd3-9d80-a181fa7fa888
keywords:
- WINBIO_REGISTERED_FORMAT Struktur Windows Biometrieframework-API
- PWINBIO_REGISTERED_FORMAT Strukturzeiger Windows Biometrieframework-API
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
ms.openlocfilehash: 2fcf871f3fc5f258de22e033e8a388968ab58c1a35e19829bf3d02a97ca60c53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118909368"
---
# <a name="winbio_registered_format-structure"></a>WINBIO \_ REGISTERED \_ FORMAT-Struktur

Die **WINBIO \_ REGISTERED \_ FORMAT-Struktur** gibt ein registriertes Datenformat als Besitzer-/Formatpaar an.

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

Ein IBIA (International Biometric Industry Association) zugewiesener Besitzerwert.

</dd> <dt>

**Typ**
</dt> <dd>

Ein vom Besitzer zugewiesenes Format.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Da Windows derzeit nur Fingerabdruckleser unterstützt, sollten die folgenden Werte in der **WINBIO \_ REGISTERED \_ FORMAT-Struktur** verwendet werden.



| Konstante                                    | Bedeutung                                                                                                               |
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| WINBIO \_ ANSI \_ 381 \_ FORMAT \_ OWNER<br/> | Inter National Committee for Information Technology Standards (INCITS) Technical Committee M1 (biometrics).<br/> |
| WINBIO \_ ANSI \_ 381-FORMATTYP \_ \_<br/>  | ANSI INCITS 381 Fingerbild-basiertes Datenaustauschformat.<br/>                                                |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                                                       |
| Header<br/>                   | <dl> <dt>Winbio \_ types.h (winbio.h einschließen)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Clientanwendungsstrukturen](client-application-structures.md)
</dt> <dt>

[**WINBIO \_ ANSI \_ 381 \_ FORMAT-Konstanten**](winbio-ansi-381-format-constants.md)
</dt> <dt>

[**WINBIO \_ BDB \_ ANSI \_ 381 \_ HEADER**](winbio-bdb-ansi-381-header.md)
</dt> <dt>

[**WINBIO \_ \_ BIR-HEADER**](winbio-bir-header.md)
</dt> </dl>

 

 





