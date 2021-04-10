---
description: Die getcapturetotalframes-Funktion gibt die Gesamtzahl der Frames in der Erfassung zurück.
ms.assetid: a2b7902c-b80f-4a0a-b12a-2a139df30fca
title: Getcapturetotalframes-Funktion (Netmon. h)
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
ms.openlocfilehash: aa7c81e690e9f7eab258c832ae374f18f9b7afc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862015"
---
# <a name="getcapturetotalframes-function"></a>Getcapturetotalframes-Funktion

Die **getcapturetotalframes** -Funktion gibt die Gesamtzahl der Frames in der Erfassung zurück.

## <a name="syntax"></a>Syntax


```C++
DWORD WINAPI GetCaptureTotalFrames(
  _In_ HCAPTURE hCapture
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hcapture* \[ in\]
</dt> <dd>

Handle für die Erfassung. Weitere Informationen zum Abrufen des Aufzeichnungs Handles finden Sie im Abschnitt "Hinweise" in diesem Thema zu **getcapturetotalframes** .

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert die Gesamtzahl der Frames in der Erfassung.

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert 0.

## <a name="remarks"></a>Bemerkungen

[*Experten*](e.md) und [*Parser*](p.md) können die **getcapturetotalframes** -Funktion aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Bibliothek<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




