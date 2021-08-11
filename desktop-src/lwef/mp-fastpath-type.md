---
title: MP_FASTPATH_TYPE-Enumeration (MpClient.h)
description: FastPath-Typ.
ms.assetid: BD72228F-DCC0-435E-A408-BD7FB02E55E1
keywords:
- MP_FASTPATH_TYPE-Enumeration– Legacy-Windows-Umgebungsfeatures
- PMP_FASTPATH_TYPE-Enumerationszeiger Legacy Windows-Umgebungsfeatures
topic_type:
- apiref
api_name:
- MP_FASTPATH_TYPE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7bd9a8ce26f930a35c9c4fa547234b0d55b0b588b60881cf8aae31621e9a83a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118247445"
---
# <a name="mp_fastpath_type-enumeration"></a>MP \_ FASTPATH \_ TYPE-Enumeration

FastPath-Typ.

## <a name="syntax"></a>Syntax


```C++
typedef enum tagMP_FASTPATH_TYPE { 
  MP_FASTPATH_UNKNOWN   = 0,
  MP_FASTPATH_VDM       = 1,
  MP_FASTPATH_DISABLED  = 2
} MP_FASTPATH_TYPE, *PMP_FASTPATH_TYPE;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="MP_FASTPATH_UNKNOWN"></span><span id="mp_fastpath_unknown"></span>**MP \_ FASTPATH \_ UNKNOWN**
</dt> <dd>

Unbekannt

</dd> <dt>

<span id="MP_FASTPATH_VDM"></span><span id="mp_fastpath_vdm"></span>**MP \_ FASTPATH \_ VDM**
</dt> <dd>

VDM-Update.

</dd> <dt>

<span id="MP_FASTPATH_DISABLED"></span><span id="mp_fastpath_disabled"></span>**MP \_ FASTPATH \_ DEAKTIVIERT**
</dt> <dd>

Signatur-Deaktivierungsbenachrichtigung.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



 

 





