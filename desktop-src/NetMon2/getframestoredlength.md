---
description: Die getframestoredlength-Funktion gibt die Länge des Frames zurück.
ms.assetid: 7ac0e528-a45a-4c36-a99d-647347bdd143
title: Getframestoredlength-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameStoredLength
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: e48f1d357645a9f50a85da4aba79d72baba4e4bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356925"
---
# <a name="getframestoredlength-function"></a>Getframestoredlength-Funktion

Die **getframestoredlength** -Funktion gibt die Länge des Frames zurück.

## <a name="syntax"></a>Syntax


```C++
DWORD WINAPI GetFrameStoredLength(
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

Wenn die Funktion erfolgreich ist, ist der Rückgabewert die Länge des Frames als gespeichert.

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert 0 (null).

## <a name="remarks"></a>Bemerkungen

[*Experten*](e.md) und [*Parser*](p.md) können die **getframestoredlength** -Funktion aufrufen.

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

[GetFrameLength](getframelength.md)
</dt> </dl>

 

 




