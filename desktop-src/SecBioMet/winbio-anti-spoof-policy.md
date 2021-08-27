---
title: WINBIO_ANTI_SPOOF_POLICY struktur (Winbio \_ types.h)
description: Stellt die Antispoofingrichtlinie für einen Benutzer dar.
ms.assetid: 2B433AE8-21A0-4AF1-853C-9074527DB2E4
keywords:
- WINBIO_ANTI_SPOOF_POLICY Struktur Windows Biometrieframework-API
- PWINBIO_ANTI_SPOOF_POLICY Strukturzeiger Windows Biometrieframework-API
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
ms.openlocfilehash: 28ade20749b105cc3c7f8a92e0904aff1cea860f9175c8b3c6adb113f273f0fd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073250"
---
# <a name="winbio_anti_spoof_policy-structure"></a>WINBIO ANTI SPOOF POLICY structure (WINBIO \_ ANTI \_ SPOOF \_ POLICY-Struktur)

Stellt die Antispoofingrichtlinie für einen Benutzer dar.

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

Der Typ der Aktion, die für die Antispoofingrichtlinie ergriffen werden soll.

</dd> <dt>

**Quelle**
</dt> <dd>

Die Quelle für die Antispoofingrichtlinie.

</dd> </dl>

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 10 Nur Desktop-Apps\]<br/>                                                                                                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2016 Nur Desktop-Apps\]<br/>                                                                                                                     |
| Header<br/>                   | <dl> <dt>Winbio \_ types.h (winbio.h für Clientanwendungen oder Winbio \_ adapters.h für Adapter einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**WINBIO \_ ANTI \_ SPOOF \_ POLICY \_ ACTION**](winbio-anti-spoof-policy-action.md)
</dt> <dt>

[**\_WINBIO-RICHTLINIENQUELLE \_**](winbio-policy-source.md)
</dt> <dt>

[**WINBIO \_ \_ ASYNC-ERGEBNIS**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result)
</dt> <dt>

[**WinBioGetProperty**](/windows/desktop/api/Winbio/nf-winbio-winbiogetproperty)
</dt> <dt>

[**WinBioSetProperty**](/windows/desktop/api/winbio/nf-winbio-winbiosetproperty)
</dt> </dl>

 

 





