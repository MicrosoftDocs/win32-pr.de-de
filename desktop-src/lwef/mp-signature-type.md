---
title: MP_SIGNATURE_TYPE-Enumeration (MpClient.h)
description: Mögliche Signaturtypen.
ms.assetid: 44B195A8-866D-4B87-9576-54E00658F9B3
keywords:
- MP_SIGNATURE_TYPE-Enumeration– Legacy-Windows-Umgebungsfeatures
- PMP_SIGNATURE_TYPE-Enumerationszeiger Legacy Windows-Umgebungsfeatures
topic_type:
- apiref
api_name:
- MP_SIGNATURE_TYPE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3289f0cbc3eeb85f553adf97078b7d3c5c53a686e914f86a4edb80c5244f72af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117883713"
---
# <a name="mp_signature_type-enumeration"></a>MP \_ SIGNATURE \_ TYPE-Enumeration

Mögliche Signaturtypen.

## <a name="syntax"></a>Syntax


```C++
typedef enum tagMP_SIGNATURE_TYPE { 
  MP_SIGNATURE_ANTIMALWARE     = 0,
  MP_SIGNATURE_ANTIVIRUS       = 1,
  MP_SIGNATURE_ANTISPYWARE     = 2,
  MP_SIGNATURE_NIS             = 3,
  MP_SIGNATURE_TYPES_MAXVALUE  = 3
} MP_SIGNATURE_TYPE, *PMP_SIGNATURE_TYPE;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="MP_SIGNATURE_ANTIMALWARE"></span><span id="mp_signature_antimalware"></span>**MP \_ SIGNATURE \_ ANTIMALWARE**
</dt> <dd>

Sowohl Antiviren- als auch Antispywaresignaturen.

</dd> <dt>

<span id="MP_SIGNATURE_ANTIVIRUS"></span><span id="mp_signature_antivirus"></span>**MP \_ SIGNATURE \_ ANTIVIRUS**
</dt> <dd>

Nur Antivirensignaturen.

</dd> <dt>

<span id="MP_SIGNATURE_ANTISPYWARE"></span><span id="mp_signature_antispyware"></span>**MP \_ SIGNATURE \_ ANTISPYWARE**
</dt> <dd>

Nur Antispywaresignaturen.

</dd> <dt>

<span id="MP_SIGNATURE_NIS"></span><span id="mp_signature_nis"></span>**MP \_ SIGNATURE \_ NIS**
</dt> <dd>

NIS-Signaturen.

</dd> <dt>

<span id="MP_SIGNATURE_TYPES_MAXVALUE"></span><span id="mp_signature_types_maxvalue"></span>**\_MP-SIGNATURTYPEN \_ \_ MAXVALUE**
</dt> <dd></dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



 

 





