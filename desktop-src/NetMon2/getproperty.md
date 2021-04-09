---
description: Die GetProperty-Funktion gibt ein Handle für eine angegebene Eigenschaft zurück.
ms.assetid: e77ca20a-55df-4d31-aa6d-2c00695f1d6e
title: GetProperty-Funktion (Netmon. h)
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
ms.openlocfilehash: 297d68d68731181ed56324a4e1d174467f622e13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958711"
---
# <a name="getproperty-function"></a>GetProperty-Funktion

Die **GetProperty** -Funktion gibt ein Handle für eine angegebene Eigenschaft zurück.

## <a name="syntax"></a>Syntax


```C++
HPROPERTY WINAPI GetProperty(
  _In_ HPROTOCOL hProtocol,
  _In_ LPSTR     PropertyName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hprotocol* \[ in\]
</dt> <dd>

Handle für das Protokoll.

</dd> <dt>

*PropertyName* \[ in\]
</dt> <dd>

Der Name der Eigenschaft (z. b. **Checksum**).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert das Handle für die Eigenschaft.

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert **null**.

## <a name="remarks"></a>Bemerkungen

Die **GetProperty** -Funktion kann verwendet werden, um das Eigenschafts Handle abzurufen, das erforderlich ist, um Instanzen der Eigenschaft zu suchen. Die Funktionen, die zum Auffinden von Eigenschafts Instanzen verwendet werden, sind [findpropertyinstance](findpropertyinstance.md) (das die erste Instanz sucht) und [findpropertyinstancerestart](findpropertyinstancerestart.md) (die die nächste Instanz findet).

[*Experten*](e.md) und [*Parser*](p.md) können die **GetProperty** -Funktion aufrufen.

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

[Findpropertyinstance](findpropertyinstance.md)
</dt> <dt>

[Findpropertyinstancerestart](findpropertyinstancerestart.md)
</dt> </dl>

 

 




