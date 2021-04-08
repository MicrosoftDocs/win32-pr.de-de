---
description: Die getframecapturehandle-Funktion gibt ein Handle für die Erfassung basierend auf einem angegebenen Frame zurück.
ms.assetid: 71b32799-194c-40f8-8438-36aebaba31c7
title: Getframecapturehandle-Funktion (Netmon. h)
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
ms.openlocfilehash: 3770ad0fd3db7d1c076b5d1f286c1fdbdc2707a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862011"
---
# <a name="getframecapturehandle-function"></a>Getframecapturehandle-Funktion

Die **getframecapturehandle** -Funktion gibt ein Handle für die Erfassung basierend auf einem angegebenen Frame zurück.

## <a name="syntax"></a>Syntax


```C++
HCAPTURE WINAPI GetFrameCaptureHandle(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hframe* \[ in\]
</dt> <dd>

Handle für einen Frame.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert ein Handle für die Erfassung.

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert 0.

## <a name="remarks"></a>Bemerkungen

[*Experten*](e.md) und [*Parser*](p.md) können die **getframecapturehandle** -Funktion aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Bibliothek<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




