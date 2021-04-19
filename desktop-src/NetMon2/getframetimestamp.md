---
description: Die getframetimestamp-Funktion gibt den Zeitstempel eines angegebenen Frames zurück.
ms.assetid: 4ac50400-6674-40fa-9a69-9c0ccb55b92c
title: Getframetimestamp-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameTimeStamp
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 37a75f946a5fc0ddb2b32d99334368a272fdf2e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106348643"
---
# <a name="getframetimestamp-function"></a>Getframetimestamp-Funktion

Die **getframetimestamp** -Funktion gibt den Zeitstempel eines angegebenen Frames zurück.

## <a name="syntax"></a>Syntax


```C++
__int64 WINAPI GetFrameTimeStamp(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hframe* \[ in\]
</dt> <dd>

Handle für den Frame.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert der Zeitstempel des Frames in Mikrosekunden.

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert minus eins (-1).

## <a name="remarks"></a>Bemerkungen

Die **getframetimestamp** -Funktion gibt einen Zeitstempel zurück, der die verstrichene Zeit zwischen dem Start des Aufzeichnungsprozesses und der Aufzeichnung des Frames anzeigt.

[*Experten*](e.md) und [*Parser*](p.md) können die **getframetimestamp** -Funktion aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Bibliothek<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




