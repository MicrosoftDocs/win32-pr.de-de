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
ms.openlocfilehash: 606b8d91d20c74f7dd56ff4e09986abec3eef547989990a38bd8b4e3a27382c2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079730"
---
# <a name="deltafree-function"></a>DeltaFree-Funktion

Gibt den angegebenen Speicherblock frei. Sie müssen diese Funktion nach erfolgreichen Aufrufen von [CreateDeltaB](msdelta-createdeltab.md) und [ApplyDeltaB](msdelta-applydeltab.md) aufrufen, um den von MSDelta zugeordneten Speicherpuffer frei zu geben.

## <a name="syntax"></a>Syntax

```cpp
BOOL  WINAPI  DeltaFree(
    LPVOID  lpMemory
    );
```

## <a name="parameters"></a>Parameter

*lpMemory*

[in] Speicherblock, der frei werden soll.

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt **TRUE zurück,** wenn sie erfolgreich ist. andernfalls wird **FALSE zurückgegeben.** Wenn die Funktion **FALSE zurückgibt,** können Sie [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) aufrufen, um den entsprechenden Win32-Systemfehlercode zu erhalten.

## <a name="requirements"></a>Requirements (Anforderungen)

| Anforderung | Wert |
|----------------|---------------------------------------------------------------------------------------|
| Header | msdelta.h |
| DLL | msdelta.dll |
| Unicode | Nicht zutreffend |

## <a name="see-also"></a>Siehe auch

[MSDelta](msdelta.md)

[CreateDeltaB](msdelta-createdeltab.md)

[ApplyDeltaB](msdelta-applydeltab.md)
