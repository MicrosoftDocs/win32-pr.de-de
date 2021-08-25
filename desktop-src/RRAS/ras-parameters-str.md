---
title: RAS_PARAMETERS -Struktur (Rassapi.h)
description: Die RAS PARAMETERS-Struktur wird von der RasAdminPortGetInfo-Funktion verwendet, um den Namen und Wert eines medienspezifischen Parameters zurückgibt, der einem Port auf einem \_ RAS-Server zugeordnet ist.
ms.assetid: b46b6176-9a0c-4d9b-b961-b20fdc41653b
keywords:
- RAS_PARAMETERS-Struktur
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
ms.openlocfilehash: e38ec1a8febbca4319a9c098eafee3705fe59602af81b3ec94e4e974892be771
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119909670"
---
# <a name="ras_parameters-structure"></a>RAS \_ PARAMETERS-Struktur

\[Die **\_ RAS-PARAMETER-Struktur** wird ab Windows Vista nicht mehr unterstützt.\]

Die **RAS \_ PARAMETERS-Struktur** wird von der [**RasAdminPortGetInfo-Funktion**](rasadminportgetinfo.md) verwendet, um den Namen und Wert eines medienspezifischen Parameters zurückgibt, der einem Port auf einem RAS-Server zugeordnet ist.

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

**\_P-Taste**
</dt> <dd>

Gibt den Namen des Schlüssels an, der den medienspezifischen Parameter darstellt, z. B. MAXCONNECTBPS.

</dd> <dt>

**\_P-Typ**
</dt> <dd>

Identifiziert den Datentyp, der dem Parameter zugeordnet ist. Dieser Member kann einer der folgenden Werte aus der [**RAS \_ PARAMS \_ FORMAT-Enumeration**](ras-params-format-str.md) sein.



| Wert                                                                                                                                                                                | Bedeutung                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <span id="ParamNumber"></span><span id="paramnumber"></span><span id="PARAMNUMBER"></span><dl> <dt>**ParamNumber**</dt> </dl> | Gibt an, dass die dem Schlüssel zugeordneten Daten eine Zahl sind.<br/> |
| <span id="ParamString"></span><span id="paramstring"></span><span id="PARAMSTRING"></span><dl> <dt>**ParamString**</dt> </dl> | Gibt an, dass die dem Schlüssel zugeordneten Daten eine Zeichenfolge sind.<br/> |



 

</dd> <dt>

**\_P-Attribute**
</dt> <dd>

Reserviert.

</dd> <dt>

**\_P-Wert**
</dt> <dd>

Gibt den Wert an, der dem Parameter zugeordnet ist. Dieser Member ist eine [**RAS \_ PARAMS \_ VALUE-Union.**](ras-params-value-str.md) Wenn das **P \_ Type-Member** ParamNumber ist, enthält **das Number-Member** der Union den Wert. Wenn **P \_ Type** paramString ist, enthält das **String-Member** der Union den Wert.

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

[Ras-Dienst (RAS): Übersicht](about-remote-access-service.md)
</dt> <dt>

[RAS-Serververwaltungsstrukturen](ras-server-administration-structures.md)
</dt> <dt>

[**RasAdminAcceptNewConnection**](rasadminacceptnewconnection.md)
</dt> <dt>

[**RasAdminConnectionHangupNotification**](rasadminconnectionhangupnotification.md)
</dt> <dt>

[**RasAdminPortGetInfo**](rasadminportgetinfo.md)
</dt> </dl>

 

 





