---
title: WINBIO_ANTI_SPOOF_POLICY_ACTION-Enumeration (Winbio \_ types.h)
description: Gibt die Arten von Aktionen an, die Sie für die Antispoofingrichtlinie eines Benutzers ausführen.
ms.assetid: 846C0725-1796-49E4-883C-44AC7D618317
keywords:
- WINBIO_ANTI_SPOOF_POLICY_ACTION enumeration Windows Biometric Framework-API
- PWINBIO_ANTI_SPOOF_POLICY Enumerationszeiger Windows Biometrieframework-API
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
ms.openlocfilehash: f65fec198a0784bf076eb90224318bd36a88ba3ed96258ffd2014a27da5c8f8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118911269"
---
# <a name="winbio_anti_spoof_policy_action-enumeration"></a>WINBIO \_ ANTI \_ SPOOF POLICY \_ \_ ACTION-Enumeration

Gibt die Arten von Aktionen an, die Sie für die Antispoofingrichtlinie eines Benutzers ausführen.

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

<span id="WINBIO_ANTI_SPOOF_DISABLE"></span><span id="winbio_anti_spoof_disable"></span>**WINBIO \_ ANTI \_ SPOOF \_ DISABLE**
</dt> <dd>

Deaktiviert die Erkennung von Spoofing für einen biometrischen Faktor.

</dd> <dt>

<span id="WINBIO_ANTI_SPOOF_ENABLE"></span><span id="winbio_anti_spoof_enable"></span>**WINBIO \_ ANTI \_ SPOOF \_ ENABLE**
</dt> <dd>

Aktiviert die Erkennung von Spoofing für einen biometrischen Faktor.

</dd> <dt>

<span id="WINBIO_ANTI_SPOOF_REMOVE"></span><span id="winbio_anti_spoof_remove"></span>**WINBIO \_ ANTI \_ SPOOF \_ REMOVE**
</dt> <dd>

Entfernt die gesamte Antispoofingrichtlinie für den biometrischen Faktor aus dem Konto.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 10 Nur Desktop-Apps\]<br/>                                                                                                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2016 Nur Desktop-Apps\]<br/>                                                                                                                     |
| Header<br/>                   | <dl> <dt>Winbio \_ types.h (winbio.h für Clientanwendungen oder Winbio \_ adapters.h für Adapter einschließen)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**WINBIO \_ ANTI \_ SPOOF \_ POLICY \_ ACTION**](winbio-anti-spoof-policy-action.md)
</dt> <dt>

[**\_WINBIO-RICHTLINIENQUELLE \_**](winbio-policy-source.md)
</dt> </dl>

 

 





