---
description: Die GetFrame-Funktion gibt ein Handle für einen bestimmten Frame innerhalb einer Erfassung zurück.
ms.assetid: d40bc364-0028-4006-a6c2-6ee100366ba3
title: GetFrame-Funktion (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrame
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 5f6f992c0c61978e2de6f90755852c9e29d6ac51d7ae7f2405ef981ed695c4b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119779250"
---
# <a name="getframe-function"></a>GetFrame-Funktion

Die **GetFrame-Funktion** gibt ein Handle für einen bestimmten Frame innerhalb einer Erfassung zurück.

## <a name="syntax"></a>Syntax


```C++
HFRAME WINAPI GetFrame(
  _In_ HCAPTURE hCapture,
  _In_ DWORD    FrameNumber
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hCapture* \[ In\]
</dt> <dd>

Handle für eine Erfassung. Rufen Sie zum Abrufen des Erfassungshandles die [GetFrameCaptureHandle-Funktion](getframecapturehandle.md) auf.

</dd> <dt>

*FrameNumber* \[ In\]
</dt> <dd>

Zahl (nullbasiert) des Frames. Die Nummer des ersten Frames in einer Erfassung ist 0 (null).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert ein Handle für den Frame.

Wenn die Funktion nicht erfolgreich ist (d. h. wenn *hCapture* ungültig ist oder die Framenummer außerhalb des Bereichs liegt), ist der Rückgabewert **NULL.**

## <a name="remarks"></a>Hinweise

Verwenden Sie die **GetFrame-Funktion,** um das Framehandle abzurufen, das beim Suchen von Instanzen einer Eigenschaft erforderlich ist. Die Funktionen, die zum Suchen von Eigenschafteninstanzen verwendet werden, sind [FindPropertyInstance,](findpropertyinstance.md) die die erste Instanz sucht, und [FindPropertyInstanceRestart,](findpropertyinstancerestart.md) die die nächste Instanz sucht.

[*Experten*](e.md) und [*Parser*](p.md) können die **GetFrame-Funktion** aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Bibliothek<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[FindPropertyInstance](findpropertyinstance.md)
</dt> <dt>

[FindPropertyInstanceRestart](findpropertyinstancerestart.md)
</dt> </dl>

 

 




