---
description: Die FindPropertyInstance-Funktion sucht die erste Instanz der Eigenschaft, die durch den hProperty-Parameter angegeben wird.
ms.assetid: e994503d-2f32-4fa2-bba9-ff66c9d558dc
title: FindPropertyInstance-Funktion (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FindPropertyInstance
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: ac8b7d34b33bb76bfffc26b3ae6fc455857fafb65a9a2aef7e91fd0c2763adc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118938581"
---
# <a name="findpropertyinstance-function"></a>FindPropertyInstance-Funktion

Die **FindPropertyInstance-Funktion** sucht die erste Instanz der Eigenschaft, die durch den *hProperty-Parameter angegeben* wird.

## <a name="syntax"></a>Syntax


```C++
LPPROPERTYINST WINAPI FindPropertyInstance(
  _In_ HFRAME    hFrame,
  _In_ HPROPERTY hProperty
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hFrame* \[ In\]
</dt> <dd>

Handle für den Frame. Das Framehand handle kann durch einen Aufruf der [GetFrame-Funktion abgerufen](getframe.md) werden.

</dd> <dt>

*hProperty* \[ In\]
</dt> <dd>

Handle für die Eigenschaft, die Sie suchen möchten. Das Eigenschaftenhand handle kann durch einen Aufruf der [GetProperty-Funktion abgerufen](getproperty.md) werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist (d. h., wenn die Eigenschaft gefunden wird), ist der Rückgabewert ein Zeiger auf die erste Instanz der Eigenschaft.

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert **NULL.**

## <a name="remarks"></a>Hinweise

Um die nächste Instanz der -Eigenschaft abzurufen, rufen [Sie FindPropertyInstanceRestart auf.](findpropertyinstancerestart.md)

[*Experten*](e.md) und [*Parser*](p.md)können die **Funktion FindPropertyInstance** aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Bibliothek<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[FindPropertyInstanceRestart](findpropertyinstancerestart.md)
</dt> </dl>

 

 




