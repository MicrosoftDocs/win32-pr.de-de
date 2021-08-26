---
description: Bestimmt, ob ein Freigabename die richtige Syntax verwendet.
ms.assetid: 4ffcff5d-0db5-4761-a31a-acefd2b8d9e2
title: NDdeIsValidShareName-Funktion (Nddeapi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeIsValidShareName
- NDdeIsValidShareNameA
- NDdeIsValidShareNameW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 3e289429047d8d1cee4f525a9f45a9abe1dd8eb51bcf57e83e39876fba9a5a89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119964000"
---
# <a name="nddeisvalidsharename-function"></a>NDdeIsValidShareName-Funktion

\[Netzwerk-DDE wird nicht mehr unterstützt. Nddeapi.dll ist auf Windows Vista vorhanden, aber alle Funktionsaufrufe geben NDDE \_ NOT \_ IMPLEMENTED zurück.\]

Bestimmt, ob ein Freigabename die richtige Syntax verwendet.

## <a name="syntax"></a>Syntax


```C++
BOOL NDdeIsValidShareName(
  _In_ LPTSTR shareName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*shareName* \[ In\]
</dt> <dd>

Der zu validierte Freigabename. Dieser Parameter darf nicht **NULL** sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn der Freigabename eine gültige Syntax aufweist, ist der Rückgabewert ungleich 0 (null).

Wenn der Freigabename keine gültige Syntax aufweist, ist der Rückgabewert 0 (null).

## <a name="remarks"></a>Hinweise

Diese Funktion wird auch von [**NDdeShareAdd**](nddeshareadd.md) aufgerufen, wenn sie die DDE-Freigabe erstellt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                             |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Nddeapi.h</dt> </dl>   |
| Bibliothek<br/>                  | <dl> <dt>Nddeapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **NDdeIsValidShareNameW** (Unicode) und **NDdeIsValidShareNameA** (ANSI)<br/>    |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Network dynamische Daten Exchange Overview (Übersicht über Netzwerk-dynamische Daten Exchange)](network-dynamic-data-exchange.md)
</dt> <dt>

[Netzwerk-DDE-Funktionen](network-dde-functions.md)
</dt> <dt>

[**NDdeShareAdd**](nddeshareadd.md)
</dt> </dl>

 

 




