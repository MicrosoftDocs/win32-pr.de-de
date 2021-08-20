---
title: MP_REMOVAL_REASON-Enumeration (MpClient.h)
description: FastPath-Signaturentfernungsgrund.
ms.assetid: A09B4903-E53C-4DA1-BD0B-6DE0124FCAB3
keywords:
- MP_REMOVAL_REASON-Enumeration– Legacy-Windows-Umgebungsfeatures
- PMP_REMOVAL_REASON-Enumerationszeiger Legacy Windows-Umgebungsfeatures
topic_type:
- apiref
api_name:
- MP_REMOVAL_REASON
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bf4e0ad95ba67a1335ec6915d400b7a8ca219c37bb302036af0a5dca2cf7479
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117883760"
---
# <a name="mp_removal_reason-enumeration"></a>MP \_ REMOVAL \_ REASON-Enumeration

FastPath-Signaturentfernungsgrund.

## <a name="syntax"></a>Syntax


```C++
typedef enum tagMP_REMOVAL_REASON { 
  MP_REMOVAL_UNKNOWN    = 0,
  MP_REMOVAL_MANUAL     = 1,
  MP_REMOVAL_AUTOMATIC  = 2
} MP_REMOVAL_REASON, *PMP_REMOVAL_REASON;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="MP_REMOVAL_UNKNOWN"></span><span id="mp_removal_unknown"></span>**MP \_ REMOVAL \_ UNKNOWN**
</dt> <dd>

Unbekannt

</dd> <dt>

<span id="MP_REMOVAL_MANUAL"></span><span id="mp_removal_manual"></span>**MP \_ REMOVAL \_ MANUAL**
</dt> <dd>

Manuelle Aktion.

</dd> <dt>

<span id="MP_REMOVAL_AUTOMATIC"></span><span id="mp_removal_automatic"></span>**AUTOMATISCHE \_ MP-ENTFERNUNG \_**
</dt> <dd>

Automatisch.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



 

 





