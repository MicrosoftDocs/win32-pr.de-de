---
description: Die GetFrameLength-Funktion gibt die Länge des Frames zurück.
ms.assetid: 30be1f5c-9b13-42ad-944a-92b1aee8a6bc
title: GetFrameLength-Funktion (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameLength
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 2344f2401995af3bac2e8245f48824dfb992076113eb8c27dcb9eff0a54eae04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117795702"
---
# <a name="getframelength-function"></a>GetFrameLength-Funktion

Die **GetFrameLength-Funktion** gibt die Länge des Frames zurück.

## <a name="syntax"></a>Syntax


```C++
DWORD WINAPI GetFrameLength(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hFrame* \[ In\]
</dt> <dd>

Handle für einen Frame.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, entspricht der Rückgabewert der Länge des Frames in Bytes.

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert 0 (null).

## <a name="remarks"></a>Hinweise

[*Experten*](e.md) und [*Parser*](p.md) können die **GetFrameLength-Funktion** aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Bibliothek<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




