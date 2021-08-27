---
description: Verwendet das Delta und die Quelle (als Puffer bereitgestellt), um eine neue Kopie der Zieldaten zu erstellen. Die Ausgabedaten werden in einem von MSDelta zugeordneten Puffer zurückgegeben.
title: ApplyDeltaB-Funktion
ms.topic: reference
ms.date: 12/03/2020
ms.keywords: ApplyDeltaB
req.header: msdelta.h
req.dll: msdelta.dll
topic_type:
- APIRef
- kbSyntax
api_name:
- ApplyDeltaB
api_type:
- DllExport
api_location:
- msdelta.dll
ms.openlocfilehash: 2a6034ca101a192be66db1b16a4ac7b27e7288d9453dfaaab5782e55e11d4c67
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079760"
---
# <a name="applydeltab-function"></a>ApplyDeltaB-Funktion

Verwendet das Delta und die Quelle (als Puffer bereitgestellt), um eine neue Kopie der Zieldaten zu erstellen. Die Ausgabedaten werden in einem von MSDelta zugeordneten Puffer zurückgegeben.

> [!NOTE]
> Sie müssen [DeltaFree aufrufen,](msdelta-deltafree.md) um den Ausgabepuffer frei zu geben, nachdem diese Funktion abgeschlossen wurde.

> [!NOTE]
> Wenn das angegebene Delta mit [PatchAPI](patchapi.md)erstellt wurde und das DELTA_APPLY_FLAG_ALLOW_PA19 festgelegt ist, wird PatchAPI von MSDelta zum Anwenden des Deltas aufruft. [](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags)

## <a name="syntax"></a>Syntax

```cpp
BOOL  WINAPI  ApplyDeltaB(
    DELTA_FLAG_TYPE  ApplyFlags,
    DELTA_INPUT      Source,
    DELTA_INPUT      Delta,
    LPDELTA_OUTPUT   lpTarget
   );
```

## <a name="parameters"></a>Parameter

*ApplyFlags*

[in] Entweder [DELTA_FLAG_NONE](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags) oder [DELTA_APPLY_FLAG_ALLOW_PA19](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags).

*Quelle*

[in] Eine [](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) DELTA_INPUT-Struktur, die einen Zeiger auf den Puffer enthält, der die Quelldaten enthält.

*Delta*

[in] Eine [](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) DELTA_INPUT-Struktur, die einen Zeiger auf den Puffer enthält, der die Deltadaten enthält.

*lpTarget*

[out] Zeiger auf [die](/previous-versions/bb417345(v=msdn.10)#delta-output-structure) DELTA_OUTPUT-Struktur, in die das Ziel geschrieben werden soll.

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

[DeltaFree](msdelta-deltafree.md)
