---
description: Die GetFrameMacType-Funktion gibt den MAC-Typ des Frames zurück.
ms.assetid: 8d3da770-1392-4638-a267-32c2dae289b0
title: GetFrameMacType-Funktion (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameMacType
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 4202e05d6820718166b4eb2e66fc0c37e7e4e3461b235069278f2128278cc7ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117982368"
---
# <a name="getframemactype-function"></a>GetFrameMacType-Funktion

Die **GetFrameMacType-Funktion** gibt den MAC-Typ des Frames zurück.

## <a name="syntax"></a>Syntax


```C++
DWORD WINAPI GetFrameMacType(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hFrame* \[ In\]
</dt> <dd>

Handle für den Frame.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Funktion gibt den MAC-Typ des Frames zurück, der einen der folgenden Werte aufweisen kann.

-   \_MAC-TYP \_ UNBEKANNT
-   \_ \_ MAC-TYP ETHERNET
-   MAC \_ TYPE \_ TOKENRING
-   MAC \_ TYPE \_ FDDI

## <a name="remarks"></a>Hinweise

[*Experten*](e.md) und [*Parser*](p.md) können die **GetFrameMacType-Funktion** aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Bibliothek<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




