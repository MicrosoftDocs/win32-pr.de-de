---
description: Diese Funktion aktiviert oder deaktiviert die Unterstützung für Endbenutzer definierte Zeichen (EUDC).
ms.assetid: 9e531d8c-6008-4189-ae25-cda707be5e2c
title: Enableeudc-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnableEUDC
api_type:
- DllExport
api_location:
- Gdi32.dll
ms.openlocfilehash: 755ce2e0a659593b17487e86e28f5d454e48122c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978632"
---
# <a name="enableeudc-function"></a>Enableeudc-Funktion

Diese Funktion aktiviert oder deaktiviert die Unterstützung für Endbenutzer definierte Zeichen (EUDC).

## <a name="syntax"></a>Syntax


```C++
BOOL EnableEUDC(
  _In_ HDC BOOL fEnableEUDC
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*fenableeudc* \[ in\]
</dt> <dd>

Boolescher Wert, der auf **true** festgelegt ist, um EUDC zu aktivieren, und auf **false** , um EUDC zu deaktivieren.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert ungleich Null.

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.

## <a name="remarks"></a>Bemerkungen

Wenn EUDC deaktiviert ist, führt der Versuch, EUDC-Zeichen anzuzeigen, zu fehlenden oder ungültigen Symbolen.

Während der mehrfach Sitzung wirkt sich diese Funktion nur auf die aktuelle Sitzung aus.

Es wird empfohlen, diese Funktion mit Windows XP SP2 oder höher zu verwenden.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Bibliothek<br/>                  | <dl> <dt>Gdi32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Gdi32.dll</dt> </dl> |



 

 




