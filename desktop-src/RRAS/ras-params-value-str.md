---
title: RAS_PARAMS_VALUE Union (Rassapi.h)
description: Die RAS \_ PARAMS VALUE-Union wird in der RAS PARAMETERS-Struktur verwendet, um die Daten zu speichern, \_ \_ die einem medienspezifischen Parameter zugeordnet sind.
ms.assetid: 43284ee4-9bd4-4019-860f-0fb7ff3f38ee
keywords:
- RAS_PARAMS_VALUE union RAS
topic_type:
- apiref
api_name:
- RAS_PARAMS_VALUE
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07453b707012c966fc298cc61973cb056b42d741d861a22204c17eec5265317f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119909600"
---
# <a name="ras_params_value-union"></a>RAS \_ PARAMS \_ VALUE union

\[Die **RAS \_ PARAMS \_ VALUE-Union** wird ab Windows Vista nicht mehr unterstützt.\]

Die **RAS \_ PARAMS \_ VALUE-Union** wird in der [**RAS \_ PARAMETERS-Struktur**](ras-parameters-str.md) verwendet, um die Daten zu speichern, die einem medienspezifischen Parameter zugeordnet sind. Der **\_ P-Typmember** der **RAS \_ PARAMETERS-Struktur** verwendet einen Wert aus der [**RAS \_ PARAMS \_ FORMAT-Enumeration,**](ras-params-format-str.md) um den Typ des Werts anzugeben, der derzeit in RAS **\_ PARAMS VALUE gespeichert \_ ist.**

## <a name="syntax"></a>Syntax


```C++
typedef union RAS_PARAMS_VALUE {
  DWORD  Number;
  struct {
    DWORD Length;
    PCHAR Data;
  } String;
} RAS_PARAMS_VALUE;
```



## <a name="members"></a>Member

<dl> <dt>

**Number**
</dt> <dd>

Wenn das **P \_ Type-Member** der [**RAS \_ PARAMETERS-Struktur**](ras-parameters-str.md) ParamNumber ist, enthält das **Number-Member** den Wert des medienspezifischen Parameters. Beispielsweise ist der MAXCONNECTBPS-Parameter vom Typ ParamNumber, und der Wert kann 19200 sein.

Wenn das **P \_ Type-Member** der [**RAS \_ PARAMETERS-Struktur**](ras-parameters-str.md) ParamNumber ist, enthält das **Number-Member** den Wert des medienspezifischen Parameters. Beispielsweise ist der MAXCONNECTBPS-Parameter vom Typ ParamNumber, und der Wert kann 19200 sein.

</dd> <dt>

**String**
</dt> <dd>

Wenn der **P \_ Type-Member** der [**RAS \_ PARAMETERS-Struktur**](ras-parameters-str.md) ParamString ist, enthält das **String-Member** den Wert des medienspezifischen Parameters.

<dl> <dt>

**Länge**
</dt> <dd>

Gibt die Länge der Zeichenfolge in Zeichen an, auf die das **Data-Element** zeigt.

</dd> <dt>

**Daten**
</dt> <dd>

Zeiger auf einen Puffer, der den Zeichenfolgenwert eines medienspezifischen Parameters enthält.

</dd> </dl> </dd> </dl>

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

[RAS Server Administration Union](ras-server-administration-union.md)
</dt> <dt>

[**\_RAS-PARAMETER**](ras-parameters-str.md)
</dt> <dt>

[**\_ \_ RAS-PARAMS-FORMAT**](ras-params-format-str.md)
</dt> </dl>

 

 





