---
title: RAS_PARAMS_FORMAT-Enumeration (Rassapi.h)
description: Der RAS \_ PARAMS \_ FORMAT-Enumerationstyp wird in der RAS \_ PARAMETERS-Struktur verwendet, um den Datentyp anzugeben, der einem medienspezifischen Schlüssel zugeordnet ist.
ms.assetid: dd2c0110-1f27-4a8f-bc61-f15588ebc4ca
keywords:
- RAS_PARAMS_FORMAT-Enumerations-RAS
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
ms.openlocfilehash: 92b798ef8a5257afcb4e4ad653801bda0d21691057abad970d6e8158f592146e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119673180"
---
# <a name="ras_params_format-enumeration"></a>RAS \_ PARAMS \_ FORMAT-Enumeration

\[Die **RAS \_ PARAMS \_ FORMAT-Enumeration** wird ab Windows Vista nicht unterstützt.\]

Der **RAS \_ PARAMS FORMAT-Enumerationstyp \_** wird in der RAS [**\_ PARAMETERS-Struktur**](ras-parameters-str.md) verwendet, um den Datentyp anzugeben, der einem medienspezifischen Schlüssel zugeordnet ist.

## <a name="syntax"></a>Syntax


```C++
typedef enum RAS_PARAMS_FORMAT { 
  ParamNumber  = 0,
  ParamString  = 1
} RAS_PARAMS_FORMAT;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="ParamNumber"></span><span id="paramnumber"></span><span id="PARAMNUMBER"></span>**ParamNumber**
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
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                       |
| Header<br/>                   | <dl> <dt>Rassapi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Remotezugriffsdienst (RAS) – Übersicht](about-remote-access-service.md)
</dt> <dt>

[RAS-Serververwaltungsenumerationen](ras-server-administration-enumerations.md)
</dt> <dt>

[**\_RAS-PARAMETER**](ras-parameters-str.md)
</dt> </dl>

 

 





