---
title: MPTHREAT_TYPE -Enumeration (MpClient.h)
description: Mögliche Bedrohungstypen.
ms.assetid: 56061F12-AA89-4203-BED4-99613E24002A
keywords:
- MPTHREAT_TYPE enumeration Legacy Windows Environment Features
- PMPTHREAT_TYPE enumeration pointer Legacy Windows Environment Features
topic_type:
- apiref
api_name:
- MPTHREAT_TYPE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b858501603b67451db9b565609d0c263040d2186cf44d91646e6df6ce3871ea1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118247141"
---
# <a name="mpthreat_type-enumeration"></a>MPTHREAT \_ TYPE-Enumeration

Mögliche Bedrohungstypen.

## <a name="syntax"></a>Syntax


```C++
typedef enum tagMPTHREAT_TYPE { 
  MPTHREAT_TYPE_KNOWNBAD   = 0,
  MPTHREAT_TYPE_BEHAVIOR   = 1,
  MPTHREAT_TYPE_UNKNOWN    = 2,
  MPTHREAT_TYPE_KNOWNGOOD  = 3,
  MPTHREAT_TYPE_NIS        = 4,
  MPTHREAT_TYPE_MAXVALUE   = 4
} MPTHREAT_TYPE, *PMPTHREAT_TYPE;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="MPTHREAT_TYPE_KNOWNBAD"></span><span id="mpthreat_type_knownbad"></span>**MPTHREAT-TYP \_ \_ KNOWNBAD**
</dt> <dd>

Bekannte fehlerhafte Bedrohung per Signatur erkannt.

</dd> <dt>

<span id="MPTHREAT_TYPE_BEHAVIOR"></span><span id="mpthreat_type_behavior"></span>**\_MPTHREAT-TYPVERHALTEN \_**
</dt> <dd>

Verdächtige Bedrohung durch Verhaltensüberwachung erkannt.

</dd> <dt>

<span id="MPTHREAT_TYPE_UNKNOWN"></span><span id="mpthreat_type_unknown"></span>**MPTHREAT-TYP \_ \_ UNBEKANNT**
</dt> <dd>

Unbekannte Bedrohungen (nicht klassifiziert).

</dd> <dt>

<span id="MPTHREAT_TYPE_KNOWNGOOD"></span><span id="mpthreat_type_knowngood"></span>**MPTHREAT-TYP \_ \_ KNOWNGOOD**
</dt> <dd>

Bekannte gute Bedrohung.

</dd> <dt>

<span id="MPTHREAT_TYPE_NIS"></span><span id="mpthreat_type_nis"></span>**MPTHREAT \_ TYPE \_ NIS**
</dt> <dd>

NIS-Bedrohungserkennung.

</dd> <dt>

<span id="MPTHREAT_TYPE_MAXVALUE"></span><span id="mpthreat_type_maxvalue"></span>**MPTHREAT-TYP \_ \_ MAXVALUE**
</dt> <dd>

Maximalwert möglich.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



 

 





