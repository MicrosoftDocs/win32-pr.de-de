---
description: Die GetProperty-Funktion gibt ein Handle für eine bestimmte Eigenschaft zurück.
ms.assetid: e77ca20a-55df-4d31-aa6d-2c00695f1d6e
title: GetProperty-Funktion (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetProperty
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 07bd5a88017ee16f3bdb1773973283d9ad0f7bc6a942fa4441fb134b5f1930da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118365973"
---
# <a name="getproperty-function"></a>GetProperty-Funktion

Die **GetProperty-Funktion** gibt ein Handle für eine bestimmte Eigenschaft zurück.

## <a name="syntax"></a>Syntax


```C++
HPROPERTY WINAPI GetProperty(
  _In_ HPROTOCOL hProtocol,
  _In_ LPSTR     PropertyName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hProtocol* \[ In\]
</dt> <dd>

Handle für das Protokoll.

</dd> <dt>

*PropertyName* \[ In\]
</dt> <dd>

Name der Eigenschaft (z. B. **Checksum**).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert das Handle für die -Eigenschaft.

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert **NULL.**

## <a name="remarks"></a>Hinweise

Die **GetProperty-Funktion** kann verwendet werden, um das Eigenschaftenhandle abzurufen, das zum Suchen von Instanzen der Eigenschaft erforderlich ist. Die Funktionen, die zum Suchen von Eigenschafteninstanzen verwendet werden, sind [FindPropertyInstance](findpropertyinstance.md) (die die erste Instanz sucht) und [FindPropertyInstanceRestart](findpropertyinstancerestart.md) (die die nächste Instanz sucht).

[*Experten*](e.md) und [*Parser*](p.md) können die **GetProperty-Funktion** aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Bibliothek<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[FindPropertyInstance](findpropertyinstance.md)
</dt> <dt>

[FindPropertyInstanceRestart](findpropertyinstancerestart.md)
</dt> </dl>

 

 




