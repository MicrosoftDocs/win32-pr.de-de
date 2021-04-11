---
title: WINBIO_ANTI_SPOOF_POLICY_ACTION-Enumeration (winbio \_ types. h)
description: Gibt die Typen von Aktionen an, die Sie für die Antispoofing-Richtlinie eines Benutzers durchführen.
ms.assetid: 846C0725-1796-49E4-883C-44AC7D618317
keywords:
- WINBIO_ANTI_SPOOF_POLICY_ACTION Enumeration Windows-Biometrieframework-API
- PWINBIO_ANTI_SPOOF_POLICY enumerationszeiger Windows-Biometrieframework-API
topic_type:
- apiref
api_name:
- WINBIO_ANTI_SPOOF_POLICY_ACTION
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5905624bad252475cdde12c003f31a734e64dd2e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956691"
---
# <a name="winbio_anti_spoof_policy_action-enumeration"></a>\_ \_ \_ Aktions Enumeration für winbio Anti Spoof-Richtlinie \_

Gibt die Typen von Aktionen an, die Sie für die Antispoofing-Richtlinie eines Benutzers durchführen.

## <a name="syntax"></a>Syntax


```C++
typedef enum _WINBIO_ANTI_SPOOF_POLICY_ACTION { 
  WINBIO_ANTI_SPOOF_DISABLE  = 0x00000000,
  WINBIO_ANTI_SPOOF_ENABLE   = 0x00000001,
  WINBIO_ANTI_SPOOF_REMOVE   = 0x00000002
} WINBIO_ANTI_SPOOF_POLICY_ACTION, *PWINBIO_ANTI_SPOOF_POLICY;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="WINBIO_ANTI_SPOOF_DISABLE"></span><span id="winbio_anti_spoof_disable"></span>**winbio \_ - \_ antispoof \_ Deaktivieren**
</dt> <dd>

Deaktiviert die Erkennung des Spoofing für einen biometrischen Faktor.

</dd> <dt>

<span id="WINBIO_ANTI_SPOOF_ENABLE"></span><span id="winbio_anti_spoof_enable"></span>**winbio \_ - \_ antispoof \_ aktivieren**
</dt> <dd>

Schaltet die Erkennung von Spoofing für einen biometrischen Faktor ein.

</dd> <dt>

<span id="WINBIO_ANTI_SPOOF_REMOVE"></span><span id="winbio_anti_spoof_remove"></span>**winbio \_ Anti \_ Spoof \_ Entfernen**
</dt> <dd>

Entfernt die gesamte Antispoofing-Richtlinie für den biometrischen Faktor aus dem Konto.

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
</dt> </dl>

 

 





