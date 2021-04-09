---
description: Die getframenumber-Funktion gibt die Anzahl von Frames zurück.
ms.assetid: 97d343a3-2a1e-47d7-bfc2-b63f8d84b29d
title: Getframenumschlag-Funktion (Netmon. h)
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
ms.openlocfilehash: de04fa513fab98b1a82d036f6f40a6c67cdda3ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958716"
---
# <a name="getframenumber-function"></a>Getframenumschlag-Funktion

Die **getframenumber** -Funktion gibt die Anzahl von Frames zurück.

## <a name="syntax"></a>Syntax


```C++
DWORD WINAPI GetFrameNumber(
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

Wenn die Funktion erfolgreich ist, ist der Rückgabewert eine Null basierte Frame Nummer.

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert minus eins (-1).

## <a name="remarks"></a>Bemerkungen

[*Experten*](e.md) und [*Parser*](p.md) können die **getframenumschlag** -Funktion aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Bibliothek<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




