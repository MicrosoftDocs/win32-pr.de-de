---
description: Die GetPreviousProtocolOffsetByName-Funktion gibt die vorherige Instanz eines bestimmten Protokolls zurück.
ms.assetid: 94f80776-564f-4089-9e3a-fdf38d9dfe8a
title: GetPreviousProtocolOffsetByName-Funktion (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPreviousProtocolOffsetByName
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 17b472bbdead74612ccc6d76f1059443ce6f62dd122f7933ae31c99fb82900a5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119743760"
---
# <a name="getpreviousprotocoloffsetbyname-function"></a>GetPreviousProtocolOffsetByName-Funktion

Die **GetPreviousProtocolOffsetByName-Funktion** gibt die vorherige Instanz eines bestimmten Protokolls zurück.

## <a name="syntax"></a>Syntax


```C++
DWORD WINAPI GetPreviousProtocolOffsetByName(
  _In_  HFRAME hFrame,
  _In_  DWORD  dwStartOffset,
  _In_  LPSTR  szProtocolName,
  _Out_ DWORD  *pdwPreviousOffset
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hFrame* \[ In\]
</dt> <dd>

Handle für den Frame.

</dd> <dt>

*dwStartOffset* \[ In\]
</dt> <dd>

Offset im Frame.

</dd> <dt>

*szProtocolName* \[ In\]
</dt> <dd>

Der Name des Protokolls, nach dem Sie suchen möchten.

</dd> <dt>

*pdwPreviousOffset* \[ out\]
</dt> <dd>

Zeiger auf ein **DWORD,** das den Offset zum vorherigen Protokoll enthält (wenn die Funktion erfolgreich ist).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert NMERR \_ SUCCESS.

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert NMERR \_ PROTOCOL \_ NOT \_ FOUND.

## <a name="remarks"></a>Hinweise

[*Experten*](e.md) und [*Parser*](p.md) können **GetPreviousProtocolOffsetByName aufrufen.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Bibliothek<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




