---
title: RAS_PARAMETERS Struktur (rassapi. h)
description: Die Struktur der RAS- \_ Parameter wird von der rasadminportgetinfo-Funktion verwendet, um den Namen und den Wert eines medienspezifischen Parameters zurückzugeben, der einem Port auf einem RAS-Server zugeordnet ist.
ms.assetid: b46b6176-9a0c-4d9b-b961-b20fdc41653b
keywords:
- RAS_PARAMETERS Struktur-RAS
topic_type:
- apiref
api_name:
- RAS_PARAMETERS
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fffaefa8a6f2cffb895cc18882ed8fc0c382a4bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518521"
---
# <a name="ras_parameters-structure"></a>Struktur der RAS- \_ Parameter

\[Die Struktur der **RAS- \_ Parameter** wird ab Windows Vista nicht unterstützt.\]

Die Struktur der **RAS- \_ Parameter** wird von der [**rasadminportgetinfo**](rasadminportgetinfo.md) -Funktion verwendet, um den Namen und den Wert eines medienspezifischen Parameters zurückzugeben, der einem Port auf einem RAS-Server zugeordnet ist.

## <a name="syntax"></a>Syntax


```C++
typedef struct RAS_PARAMETERS {
  CHAR              P_Key[RASSAPI_MAX_PARAM_KEY_SIZE];
  RAS_PARAMS_FORMAT P_Type;
  BYTE              P_Attributes;
  RAS_PARAMS_VALUE  P_Value;
} RAS_PARAMETERS;
```



## <a name="members"></a>Member

<dl> <dt>

**P- \_ Taste**
</dt> <dd>

Gibt den Namen des Schlüssels an, der den medienspezifischen Parameter darstellt, z. b. maxconnectbit/s.

</dd> <dt>

**P- \_ Typ**
</dt> <dd>

Identifiziert den Typ der Daten, die dem-Parameter zugeordnet sind. Dieser Member kann einer der folgenden Werte aus der RAS- [**\_ parametriams- \_ formatenumeration**](ras-params-format-str.md) sein.



| Wert                                                                                                                                                                                | Bedeutung                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <span id="ParamNumber"></span><span id="paramnumber"></span><span id="PARAMNUMBER"></span><dl> <dt>**ParamNumber**</dt> </dl> | Gibt an, dass die dem Schlüssel zugeordneten Daten eine Zahl sind.<br/> |
| <span id="ParamString"></span><span id="paramstring"></span><span id="PARAMSTRING"></span><dl> <dt>**ParamString**</dt> </dl> | Gibt an, dass die dem Schlüssel zugeordneten Daten eine Zeichenfolge sind.<br/> |



 

</dd> <dt>

**P- \_ Attribute**
</dt> <dd>

Reserviert.

</dd> <dt>

**P- \_ Wert**
</dt> <dd>

Gibt den Wert an, der dem Parameter zugeordnet ist. Dieser Member ist ein [**RAS-Parameter \_ \_ Wert**](ras-params-value-str.md) Union. Wenn der **P- \_ Typmember** eine paramnumber ist, enthält der **Number** -Member der Union den Wert. Wenn der **P- \_ Typ** paramString ist, enthält der **Zeichen** folgen Member der Union den Wert.

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

[RAS-Server-Verwaltungsstrukturen](ras-server-administration-structures.md)
</dt> <dt>

[**Rasadminakzeptnewconnection**](rasadminacceptnewconnection.md)
</dt> <dt>

[**Rasadminconnectionhangupnotification**](rasadminconnectionhangupnotification.md)
</dt> <dt>

[**Rasadminportgetinfo**](rasadminportgetinfo.md)
</dt> </dl>

 

 





