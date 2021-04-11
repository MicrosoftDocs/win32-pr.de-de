---
description: Die GetFrame-Funktion gibt ein Handle für einen angegebenen Frame in einer Erfassung zurück.
ms.assetid: d40bc364-0028-4006-a6c2-6ee100366ba3
title: GetFrame-Funktion (Netmon. h)
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
ms.openlocfilehash: 3f79e7fa6fc4e79f4dea804769cc9d51b8096860
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128341"
---
# <a name="getframe-function"></a>GetFrame-Funktion

Die **GetFrame** -Funktion gibt ein Handle für einen angegebenen Frame in einer Erfassung zurück.

## <a name="syntax"></a>Syntax


```C++
HFRAME WINAPI GetFrame(
  _In_ HCAPTURE hCapture,
  _In_ DWORD    FrameNumber
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hcapture* \[ in\]
</dt> <dd>

Handle für eine Erfassung. Um das Erfassungs Handle abzurufen, rufen Sie die [getframecapturehandle](getframecapturehandle.md) -Funktion auf.

</dd> <dt>

*Framengegen ber* \[ in\]
</dt> <dd>

Die Zahl (null basiert) des Frames. Die Nummer des ersten Frames in einer Erfassung ist 0 (null).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert ein Handle für den Frame.

Wenn die Funktion nicht erfolgreich ist (d. h., wenn *hcapture* ungültig ist oder die Frame Nummer außerhalb des gültigen Bereichs liegt), ist der Rückgabewert **null**.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie die **GetFrame** -Funktion zum Abrufen des Frame Handles, das beim Suchen von Instanzen einer Eigenschaft erforderlich ist. Die Funktionen, die zum Suchen von Eigenschafts Instanzen verwendet werden, sind [findpropertyinstance](findpropertyinstance.md) , das die erste Instanz sucht, und [findpropertyinstancerestart](findpropertyinstancerestart.md) , die die nächste Instanz sucht.

[*Experten*](e.md) und [*Parser*](p.md) können die **GetFrame** -Funktion aufrufen.

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

[Findpropertyinstance](findpropertyinstance.md)
</dt> <dt>

[Findpropertyinstancerestart](findpropertyinstancerestart.md)
</dt> </dl>

 

 




