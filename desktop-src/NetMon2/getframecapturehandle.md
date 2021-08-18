---
description: Die GetFrameCaptureHandle-Funktion gibt basierend auf einem bestimmten Frame ein Handle an die Erfassung zurück.
ms.assetid: 71b32799-194c-40f8-8438-36aebaba31c7
title: GetFrameCaptureHandle-Funktion (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameCaptureHandle
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 9e7bf14cd7eae73ac1e5c8e21f8036574628932032a1545f8ac1c653dbbf8adb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119910750"
---
# <a name="getframecapturehandle-function"></a>GetFrameCaptureHandle-Funktion

Die **GetFrameCaptureHandle-Funktion** gibt basierend auf einem bestimmten Frame ein Handle an die Erfassung zurück.

## <a name="syntax"></a>Syntax


```C++
HCAPTURE WINAPI GetFrameCaptureHandle(
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

Wenn die Funktion erfolgreich ist, ist der Rückgabewert ein Handle für die Erfassung.

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert 0.

## <a name="remarks"></a>Hinweise

[*Experten*](e.md) und [*Parser*](p.md) können die **GetFrameCaptureHandle-Funktion** aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Bibliothek<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




