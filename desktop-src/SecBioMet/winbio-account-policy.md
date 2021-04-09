---
title: WINBIO_ACCOUNT_POLICY Struktur (winbio \_ Adapter. h)
description: Enthält entweder eine Standard-oder eine kontospezifische Antispoofing-Richtlinie.
ms.assetid: 7098FC53-E487-42B2-8B4B-EB7E2D296CB6
keywords:
- WINBIO_ACCOUNT_POLICY Struktur Windows-Biometrieframework-API
- PWINBIO_ACCOUNT_POLICY Struktur Zeiger Windows-Biometrieframework API
topic_type:
- apiref
api_name:
- WINBIO_ACCOUNT_POLICY
api_location:
- Winbio_adapter.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c734fa6d98615b7708a65ebad1dddc47cdc77cc2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956463"
---
# <a name="winbio_account_policy-structure"></a>Struktur der winbio- \_ Konto \_ Richtlinien

Die Struktur der **winbio- \_ Konto \_ Richtlinien** enthält entweder eine Standard-oder eine kontospezifische antispoofinganchtlinie.

## <a name="syntax"></a>Syntax


```C++
typedef struct _WINBIO_ACCOUNT_POLICY {
  WINBIO_IDENTITY                 Identity;
  WINBIO_ANTI_SPOOF_POLICY_ACTION AntiSpoofBehavior;
} WINBIO_ACCOUNT_POLICY, *PWINBIO_ACCOUNT_POLICY;
```



## <a name="members"></a>Member

<dl> <dt>

**Identität**
</dt> <dd>

Eine [**winbio- \_ Identitäts**](winbio-identity.md) Struktur, die die Kontoinformationen angibt.

</dd> <dt>

**Antispoofverhalten**
</dt> <dd>

Einer der [**winbio \_ Anti \_ Spoof \_ Policy \_ Action**](winbio-anti-spoof-policy-action.md) -Enumerationswerte, der angibt, welche Aktion für Antispoofing-Richtlinien für das Konto verwendet werden soll.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Eine Beschreibung der Verwendung dieser Struktur finden Sie in der Beschreibung der [**engineadaptersetaccountpolicy**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_account_policy_fn) -Methode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 10 \[ -Desktop-Apps\]<br/>                                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2016 \[ -Desktop-Apps\]<br/>                                                                     |
| Header<br/>                   | <dl> <dt>Winbio \_ Adapter. h (Include winbio \_ Adapter. h)</dt> </dl> |



 

 





