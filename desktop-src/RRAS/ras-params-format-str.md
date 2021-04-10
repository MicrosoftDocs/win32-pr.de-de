---
title: RAS_PARAMS_FORMAT-Enumeration (rassapi. h)
description: Der \_ \_ Enumerationstyp "RAS-Parametertyp" wird in der Struktur der RAS- \_ Parameter verwendet, um den Datentyp anzugeben, der einem medienspezifischen Schlüssel zugeordnet ist.
ms.assetid: dd2c0110-1f27-4a8f-bc61-f15588ebc4ca
keywords:
- RAS_PARAMS_FORMAT-Enumeration RAS
topic_type:
- apiref
api_name:
- RAS_PARAMS_FORMAT
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00065f3781fd2ada420f67367e84e0863fe3b446
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104391"
---
# <a name="ras_params_format-enumeration"></a>RAS- \_ parametriams- \_ formatenumeration

\[Die **RAS- \_ parametriams- \_ formatenumeration** wird ab Windows Vista nicht unterstützt.\]

Der Enumerationstyp " **RAS \_ \_** -Parametertyp" wird in der Struktur der [**RAS- \_ Parameter**](ras-parameters-str.md) verwendet, um den Datentyp anzugeben, der einem medienspezifischen Schlüssel zugeordnet ist.

## <a name="syntax"></a>Syntax


```C++
typedef enum RAS_PARAMS_FORMAT { 
  ParamNumber  = 0,
  ParamString  = 1
} RAS_PARAMS_FORMAT;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="ParamNumber"></span><span id="paramnumber"></span><span id="PARAMNUMBER"></span>**Paramnumber**
</dt> <dd>

Gibt an, dass die dem Schlüssel zugeordneten Daten eine Zahl sind.

</dd> <dt>

<span id="ParamString"></span><span id="paramstring"></span><span id="PARAMSTRING"></span>**ParamString**
</dt> <dd>

Gibt an, dass die dem Schlüssel zugeordneten Daten eine Zeichenfolge sind.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                                                |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                       |
| Header<br/>                   | <dl> <dt>Rassapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Remote Zugriffs Dienst (RAS) (Übersicht)](about-remote-access-service.md)
</dt> <dt>

[RAS-Server-Administrations Enumerationen](ras-server-administration-enumerations.md)
</dt> <dt>

[**RAS- \_ Parameter**](ras-parameters-str.md)
</dt> </dl>

 

 





