---
description: Die findpropertyinstance-Funktion sucht die erste Instanz der Eigenschaft, die durch den hproperty-Parameter angegeben wird.
ms.assetid: e994503d-2f32-4fa2-bba9-ff66c9d558dc
title: Findpropertyinstance-Funktion (Netmon. h)
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
ms.openlocfilehash: 21f94a3e4a1eb9619b39cff534a778235980a278
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344662"
---
# <a name="findpropertyinstance-function"></a>Findpropertyinstance-Funktion

Die **findpropertyinstance** -Funktion sucht die erste Instanz der Eigenschaft, die durch den *hproperty* -Parameter angegeben wird.

## <a name="syntax"></a>Syntax


```C++
LPPROPERTYINST WINAPI FindPropertyInstance(
  _In_ HFRAME    hFrame,
  _In_ HPROPERTY hProperty
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hframe* \[ in\]
</dt> <dd>

Handle für den Frame. Das Frame Handle kann durch einen Aufrufen der [GetFrame](getframe.md) -Funktion abgerufen werden.

</dd> <dt>

*hproperty* \[ in\]
</dt> <dd>

Handle für die Eigenschaft, die Sie suchen möchten. Das Eigenschafts Handle kann durch einen Aufrufen der [GetProperty](getproperty.md) -Funktion abgerufen werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist (d. h., wenn die-Eigenschaft gefunden wird), ist der Rückgabewert ein Zeiger auf die erste Instanz der-Eigenschaft.

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert **null**.

## <a name="remarks"></a>Bemerkungen

Rufen Sie zum Abrufen der nächsten Instanz der Eigenschaft [findpropertyinstancerestart](findpropertyinstancerestart.md)auf.

[*Experten*](e.md) und [*Parser*](p.md)können die **findpropertyinstance** -Funktion aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Bibliothek<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Findpropertyinstancerestart](findpropertyinstancerestart.md)
</dt> </dl>

 

 




