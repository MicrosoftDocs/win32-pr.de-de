---
description: Die GetCaptureTotalFrames-Funktion gibt die Gesamtzahl der Frames in der Erfassung zurück.
ms.assetid: a2b7902c-b80f-4a0a-b12a-2a139df30fca
title: GetCaptureTotalFrames-Funktion (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCaptureTotalFrames
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 2a7cae78dd95521fa80dfd9b9637b332c72ed1c82b90ba1f6c932824181ef565
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119910780"
---
# <a name="getcapturetotalframes-function"></a>GetCaptureTotalFrames-Funktion

Die **GetCaptureTotalFrames-Funktion** gibt die Gesamtzahl der Frames in der Erfassung zurück.

## <a name="syntax"></a>Syntax


```C++
DWORD WINAPI GetCaptureTotalFrames(
  _In_ HCAPTURE hCapture
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hCapture* \[ In\]
</dt> <dd>

Handle für die Erfassung. Informationen zum Abrufen des Erfassungshandlers finden Sie im Abschnitt "Hinweise" dieses **Themas GetCaptureTotalFrames.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert die Gesamtzahl der Frames in der Erfassung.

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert 0.

## <a name="remarks"></a>Hinweise

[*Experten*](e.md) und [*Parser*](p.md) können die **GetCaptureTotalFrames-Funktion** aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Bibliothek<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




