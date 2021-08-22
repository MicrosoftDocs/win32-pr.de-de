---
description: Die ModifyFrame-Funktion ändert einen vorhandenen Frame mit neuen Daten.
ms.assetid: ebd248e4-b248-4f4a-8b94-a6d1c331d12a
title: ModifyFrame-Funktion (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ModifyFrame
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 04bc22af11d83078ecf98d0386b061b520fbf9a8dcab6f6beb360c45b1c6fe96
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119555820"
---
# <a name="modifyframe-function"></a>ModifyFrame-Funktion

Die **ModifyFrame-Funktion** ändert einen vorhandenen Frame mit neuen Daten.

## <a name="syntax"></a>Syntax


```C++
HFRAME WINAPI ModifyFrame(
  _In_  HCAPTURE hCapture,
  _In_  DWORD    FrameNumber,
  _In_  LPBYTE   FrameData,
  _In_  DWORD    FrameLength,
  _Out_ __int64  TimeStamp
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hCapture* \[ In\]
</dt> <dd>

Handle für die Erfassung. Informationen zum Abrufen des Erfassungshandle finden Sie im Abschnitt "Hinweise" dieses **ModifyFrame-Themas.**

</dd> <dt>

*FrameNumber* \[ In\]
</dt> <dd>

Frameindexnummer.

</dd> <dt>

*FrameData* \[ In\]
</dt> <dd>

Zeiger auf ein Bytearray, das die neuen Framedaten enthält.

</dd> <dt>

*FrameLength* \[ In\]
</dt> <dd>

Länge der neuen Daten in Bytes.

</dd> <dt>

*TimeStamp* \[ out\]
</dt> <dd>

Zeitstempel, der angibt, wann der Frame geändert wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert ein Handle für einen neuen Frame.

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert **NULL.**

## <a name="remarks"></a>Hinweise

Wenn der Aufruf erfolgreich ist, zerstört die **ModifyFrame-Funktion** den ursprünglichen Frame.

[*Experten*](e.md) und [*Parser*](p.md) können die **ModifyFrame-Funktion** aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Bibliothek<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




