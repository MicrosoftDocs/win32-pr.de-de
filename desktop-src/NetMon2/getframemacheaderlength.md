---
description: Die GetFrameMacHeaderLength-Funktion gibt die Länge des MAC-Headers des Frames in Bytes zurück.
ms.assetid: 4a0f6a8c-04e0-47cb-abd1-b4011cd2d062
title: GetFrameMacHeaderLength-Funktion (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameMacHeaderLength
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 0e6c4abe859cd4c307d8ade586b9371b69b5c171681006cf4aa1634ef815d794
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119743900"
---
# <a name="getframemacheaderlength-function"></a>GetFrameMacHeaderLength-Funktion

Die **GetFrameMacHeaderLength-Funktion** gibt die Länge des MAC-Headers des Frames in Bytes zurück.

## <a name="syntax"></a>Syntax


```C++
DWORD WINAPI GetFrameMacHeaderLength(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hFrame* \[ In\]
</dt> <dd>

Handle für den Frame.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, entspricht der Rückgabewert der Länge des MAC-Headers in Bytes.

Wenn die Funktion nicht erfolgreich ist oder ein unbekannter MAC-Typ gefunden wird, ist der Rückgabewert 0 (null).

## <a name="remarks"></a>Hinweise

[*Experten*](e.md) und [*Parser*](p.md) können die **GetFrameMacHeaderLength-Funktion** aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Bibliothek<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




