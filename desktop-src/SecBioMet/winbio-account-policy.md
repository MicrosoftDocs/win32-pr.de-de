---
title: WINBIO_ACCOUNT_POLICY -Struktur \_ (Winbio-Adapter.h)
description: Enthält entweder eine Standardrichtlinie oder eine kontospezifische Antipoofingrichtlinie.
ms.assetid: 7098FC53-E487-42B2-8B4B-EB7E2D296CB6
keywords:
- WINBIO_ACCOUNT_POLICY Struktur Windows Biometrieframework-API
- PWINBIO_ACCOUNT_POLICY Strukturzeiger für Windows Biometrieframework-API
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
ms.openlocfilehash: c30241f0e13528c8427367c61362b803caaa9fc8c0a15a0eefad72689517d40f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120035250"
---
# <a name="winbio_account_policy-structure"></a>\_ \_ WINBIO-KONTORICHTLINIENstruktur

Die **\_ WINBIO-KONTORICHTLINIENstruktur \_** enthält entweder eine Standardrichtlinie oder eine kontospezifische Antipoofingrichtlinie.

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

Eine [**WINBIO \_ IDENTITY-Struktur,**](winbio-identity.md) die die Kontoinformationen angibt.

</dd> <dt>

**AntiSpoofBehavior**
</dt> <dd>

Einer der [**WINBIO \_ ANTI \_ SPOOF POLICY \_ ACTION-Enumerationswerte, \_**](winbio-anti-spoof-policy-action.md) der angibt, welche Antispoofingrichtlinienaktion für das Konto verwendet werden soll.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Eine Beschreibung der Verwendung dieser Struktur finden Sie in der Beschreibung der [**EngineAdapterSetAccountPolicy-Methode.**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_account_policy_fn)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 10 Nur Desktop-Apps\]<br/>                                                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2016 Nur Desktop-Apps\]<br/>                                                                     |
| Header<br/>                   | <dl> <dt>Winbio \_ adapter.h (winbio \_ adapter.h enthalten)</dt> </dl> |



 

 





