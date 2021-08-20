---
description: Diese Funktion aktiviert oder deaktiviert die Unterstützung für endbenutzerdefinierte Zeichen (EUDC).
ms.assetid: 9e531d8c-6008-4189-ae25-cda707be5e2c
title: EnableEUDC-Funktion
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
ms.openlocfilehash: 5767be62d23e992223500bf7192fc89efe04f03288280c73445378e083cc1613
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117699475"
---
# <a name="enableeudc-function"></a>EnableEUDC-Funktion

Diese Funktion aktiviert oder deaktiviert die Unterstützung für endbenutzerdefinierte Zeichen (EUDC).

## <a name="syntax"></a>Syntax


```C++
BOOL EnableEUDC(
  _In_ HDC BOOL fEnableEUDC
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*fEnableEUDC* \[ In\]
</dt> <dd>

Boolescher Wert, der auf **TRUE** festgelegt ist, um EUDC zu aktivieren, und **false,** um EUDC zu deaktivieren.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert ungleich Null.

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.

## <a name="remarks"></a>Hinweise

Wenn EUDC deaktiviert ist, führt der Versuch, EUDC-Zeichen anzuzeigen, zu fehlenden oder fehlerhaften Glyphen.

Während der Mehrsitzung wirkt sich diese Funktion nur auf die aktuelle Sitzung aus.

Es wird empfohlen, diese Funktion mit Windows XP SP2 oder höher zu verwenden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Bibliothek<br/>                  | <dl> <dt>Gdi32.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Gdi32.dll</dt> </dl> |



 

 




