---
title: MP_PERSISTENCE_LIMIT_TYPE -Enumeration (MpClient.h)
description: Persistenzlimittyp.
ms.assetid: 57423110-7966-4240-8B15-1859D3D9EA4C
keywords:
- MP_PERSISTENCE_LIMIT_TYPE enumeration Legacy Windows Environment Features
- PMP_PERSISTENCE_LIMIT_TYPE-Enumerationszeiger Legacy Windows Umgebungsfeatures
topic_type:
- apiref
api_name:
- MP_PERSISTENCE_LIMIT_TYPE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2a56d4962467abe0ad338af257aca2581e612c100468fbdf2853aa4d71290ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119609000"
---
# <a name="mp_persistence_limit_type-enumeration"></a>MP \_ PERSISTENCE \_ LIMIT \_ TYPE-Enumeration

Persistenzlimittyp.

## <a name="syntax"></a>Syntax


```C++
typedef enum tagMP_PERSISTENCE_LIMIT_TYPE { 
  MP_PERSISTENCE_UNKNOWN      = 0,
  MP_PERSISTENCE_NO_LIMIT     = 1,
  MP_PERSISTENCE_DURATION     = 2,
  MP_PERSISTENCE_VDM_VERSION  = 3,
  MP_PERSISTENCE_TIMESTAMP    = 4,
  MP_PERSISTENCE_FORCED       = 5
} MP_PERSISTENCE_LIMIT_TYPE, *PMP_PERSISTENCE_LIMIT_TYPE;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="MP_PERSISTENCE_UNKNOWN"></span><span id="mp_persistence_unknown"></span>**MP \_ PERSISTENCE \_ UNKNOWN**
</dt> <dd>

Unbekannt

</dd> <dt>

<span id="MP_PERSISTENCE_NO_LIMIT"></span><span id="mp_persistence_no_limit"></span>**MP \_ PERSISTENCE \_ NO \_ LIMIT**
</dt> <dd>

Keine Begrenzung

</dd> <dt>

<span id="MP_PERSISTENCE_DURATION"></span><span id="mp_persistence_duration"></span>**DAUER DER \_ \_ MP-PERSISTENZ**
</dt> <dd>

Dauer.

</dd> <dt>

<span id="MP_PERSISTENCE_VDM_VERSION"></span><span id="mp_persistence_vdm_version"></span>**MP \_ \_ PERSISTENCE-VERSION \_**
</dt> <dd>

DIE VERSION.

</dd> <dt>

<span id="MP_PERSISTENCE_TIMESTAMP"></span><span id="mp_persistence_timestamp"></span>**MP \_ PERSISTENCE \_ TIMESTAMP**
</dt> <dd>

Timestamp.

</dd> <dt>

<span id="MP_PERSISTENCE_FORCED"></span><span id="mp_persistence_forced"></span>**MP \_ PERSISTENCE \_ FORCED**
</dt> <dd>

Gezwungen.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



 

 





