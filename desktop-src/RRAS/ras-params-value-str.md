---
title: RAS_PARAMS_VALUE Union (rassapi. h)
description: Die RAS- \_ \_ Parameterwert-Union wird in der Struktur der RAS- \_ Parameter verwendet, um die Daten zu speichern, die mit einem medienspezifischen Parameter verknüpft sind.
ms.assetid: 43284ee4-9bd4-4019-860f-0fb7ff3f38ee
keywords:
- RAS_PARAMS_VALUE Union RAS
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
ms.openlocfilehash: b6f8cc6d693b32b1bbe6f05e8d32ca31a48cfb29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102831"
---
# <a name="ras_params_value-union"></a>RAS-Parameter \_ \_ Wert Union

\[Die **RAS- \_ parametriams- \_ Wert** Union wird ab Windows Vista nicht unterstützt.\]

Die **RAS- \_ \_ Parameterwert** -Union wird in der Struktur der [**RAS- \_ Parameter**](ras-parameters-str.md) verwendet, um die Daten zu speichern, die mit einem medienspezifischen Parameter verknüpft sind. Der P-Typmember der **RAS \_ -Parameter** Struktur verwendet einen Wert aus der RAS- **\_ parameterformatenumeration** , um den Typ des Werts anzugeben, der derzeit in einem RAS-Parameter **\_ \_ Wert** gespeichert wird. [**\_ \_**](ras-params-format-str.md)

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

Wenn der **P- \_ Typmember** der [**RAS- \_ Parameter**](ras-parameters-str.md) Struktur paramnumber ist, enthält der **Number** -Member den Wert des medienspezifischen Parameters. Beispielsweise ist der maxconnectbps-Parameter vom Typ paramnumber, und der Wert kann 19200 lauten.

Wenn der **P- \_ Typmember** der [**RAS- \_ Parameter**](ras-parameters-str.md) Struktur paramnumber ist, enthält der **Number** -Member den Wert des medienspezifischen Parameters. Beispielsweise ist der maxconnectbps-Parameter vom Typ paramnumber, und der Wert kann 19200 lauten.

</dd> <dt>

**String**
</dt> <dd>

Wenn der **P- \_ Typmember** der [**RAS- \_ Parameter**](ras-parameters-str.md) Struktur paramString ist, enthält der **Zeichen** folgen Member den Wert des medienspezifischen Parameters.

<dl> <dt>

**Länge**
</dt> <dd>

Gibt die Länge der Zeichenfolge, auf die vom **Datenmember** verwiesen wird, in Zeichen an.

</dd> <dt>

**Daten**
</dt> <dd>

Ein Zeiger auf einen Puffer, der den Zeichen folgen Wert eines medienspezifischen Parameters enthält.

</dd> </dl> </dd> </dl>

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

[RAS-Server Verwaltung (Union)](ras-server-administration-union.md)
</dt> <dt>

[**RAS- \_ Parameter**](ras-parameters-str.md)
</dt> <dt>

[**Format des RAS- \_ Parametern \_**](ras-params-format-str.md)
</dt> </dl>

 

 





