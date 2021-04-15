---
title: WINBIO_ANTI_SPOOF_POLICY Struktur (winbio \_ types. h)
description: Stellt die Richtlinie für Antispoofing für einen Benutzer dar.
ms.assetid: 2B433AE8-21A0-4AF1-853C-9074527DB2E4
keywords:
- WINBIO_ANTI_SPOOF_POLICY Struktur Windows-Biometrieframework-API
- PWINBIO_ANTI_SPOOF_POLICY Struktur Zeiger Windows-Biometrieframework API
topic_type:
- apiref
api_name:
- WINBIO_ANTI_SPOOF_POLICY
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3da8b7811afb1de1ad464675125f125ef0ceab73
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477499"
---
# <a name="winbio_anti_spoof_policy-structure"></a>Struktur der winbio- \_ \_ antispoof- \_ Richtlinien

Stellt die Richtlinie für Antispoofing für einen Benutzer dar.

## <a name="syntax"></a>Syntax


```C++
typedef struct _WINBIO_ANTI_SPOOF_POLICY {
  WINBIO_ANTI_SPOOF_POLICY_ACTION Action;
  WINBIO_POLICY_SOURCE            Source;
} WINBIO_ANTI_SPOOF_POLICY, *PWINBIO_ANTI_SPOOF_POLICY;
```



## <a name="members"></a>Member

<dl> <dt>

**Aktion**
</dt> <dd>

Der Typ der Aktion, die für die Antispoofing-Richtlinie ausgeführt werden soll.

</dd> <dt>

**Quelle**
</dt> <dd>

Die Quelle für die Antispoofing-Richtlinie.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 10 \[ -Desktop-Apps\]<br/>                                                                                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2016 \[ -Desktop-Apps\]<br/>                                                                                                                     |
| Header<br/>                   | <dl> <dt>Winbio \_ types. h (Include winbio. h für Client Anwendungen oder winbio \_ Adapters. h für Adapter)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Aktion für winbio- \_ \_ antispoof- \_ Richtlinie \_**](winbio-anti-spoof-policy-action.md)
</dt> <dt>

[**Quelle der winbio- \_ Richtlinie \_**](winbio-policy-source.md)
</dt> <dt>

[**winbio \_ Async- \_ Ergebnis**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result)
</dt> <dt>

[**Winbiogetproperty**](/windows/desktop/api/Winbio/nf-winbio-winbiogetproperty)
</dt> <dt>

[**Winbiosetproperty**](/windows/desktop/api/winbio/nf-winbio-winbiosetproperty)
</dt> </dl>

 

 





