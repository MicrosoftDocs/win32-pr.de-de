---
description: Die GetFrameNumber-Funktion gibt die Nummer eines Frames zurück.
ms.assetid: 97d343a3-2a1e-47d7-bfc2-b63f8d84b29d
title: GetFrameNumber-Funktion (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameNumber
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: a92f5818c9b7f89c73179abb70aa53e3639de9ab8da533489a1fdd7a5a05ddfd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117795648"
---
# <a name="getframenumber-function"></a>GetFrameNumber-Funktion

Die **GetFrameNumber-Funktion** gibt die Nummer eines Frames zurück.

## <a name="syntax"></a>Syntax


```C++
DWORD WINAPI GetFrameNumber(
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

Wenn die Funktion erfolgreich ist, ist der Rückgabewert eine nullbasierte Framenummer.

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert minus 1 (-1).

## <a name="remarks"></a>Hinweise

[*Experten*](e.md) und [*Parser*](p.md) können die **GetFrameNumber-Funktion** aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Bibliothek<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




