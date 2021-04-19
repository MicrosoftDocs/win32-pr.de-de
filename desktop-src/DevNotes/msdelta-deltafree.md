---
description: Gibt den angegebenen Speicherblock frei.
title: DeltaFree-Funktion
ms.topic: reference
ms.date: 12/03/2020
ms.keywords: DeltaFree
req.header: msdelta.h
req.dll: msdelta.dll
topic_type:
- APIRef
- kbSyntax
api_name:
- DeltaFree
api_type:
- DllExport
api_location:
- msdelta.dll
ms.openlocfilehash: 15885cfa3e879ed6a1e85b2f9553af92d436ca71
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370119"
---
# <a name="deltafree-function"></a>DeltaFree-Funktion

Gibt den angegebenen Speicherblock frei. Sie müssen diese Funktion nach erfolgreichen Aufrufen von " [anatedeltab](msdelta-createdeltab.md) " und " [applydeltab](msdelta-applydeltab.md) " aufrufen, um den von Msdelta zugewiesenen Speicherpuffer freizugeben.

## <a name="syntax"></a>Syntax

```cpp
BOOL  WINAPI  DeltaFree(
    LPVOID  lpMemory
    );
```

## <a name="parameters"></a>Parameter

*lpmemory*

in Der Speicherblock, der freigegeben werden soll.

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt **true** zurück, wenn Sie erfolgreich ist. Andernfalls wird **false** zurückgegeben. Wenn die Funktion " **false**" zurückgibt, können Sie " [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) " aufrufen, um den entsprechenden Win32-Systemfehler Code zu erhalten.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|----------------|---------------------------------------------------------------------------------------|
| Header | Msdelta. h |
| DLL | msdelta.dll |
| Unicode | Nicht verfügbar |

## <a name="see-also"></a>Siehe auch

[Msdelta](msdelta.md)

["Kreatedeltab"](msdelta-createdeltab.md)

[ApplyDelta Tab](msdelta-applydeltab.md)
