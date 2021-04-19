---
description: Verwendet das Delta und die Quelle (als Puffer bereitgestellt), um eine neue Kopie der Zieldaten zu erstellen. Die Ausgabedaten werden in einem von Msdelta zugewiesenen Puffer zurückgegeben.
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
ms.openlocfilehash: 368788ba894064aa8ac3f8c9711f987a32f306af
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359723"
---
# <a name="applydeltab-function"></a>ApplyDeltaB-Funktion

Verwendet das Delta und die Quelle (als Puffer bereitgestellt), um eine neue Kopie der Zieldaten zu erstellen. Die Ausgabedaten werden in einem von Msdelta zugewiesenen Puffer zurückgegeben.

> [!NOTE]
> Sie müssen [Delta Free](msdelta-deltafree.md) anrufen, um den Ausgabepuffer freizugeben, nachdem diese Funktion abgeschlossen wurde.

> [!NOTE]
> Wenn das angegebene Delta mithilfe von [PatchAPI](patchapi.md)erstellt wurde und das [DELTA_APPLY_FLAG_ALLOW_PA19](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags) -Flag festgelegt ist, ruft Msdelta PatchAPI auf, um das Delta anzuwenden.

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

*Applyflags*

in Entweder [DELTA_FLAG_NONE](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags) oder [DELTA_APPLY_FLAG_ALLOW_PA19](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags).

*Quelle*

in Eine [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) -Struktur mit einem Zeiger auf den Puffer, der die Quelldaten enthält.

*Delta*

in Eine [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) -Struktur mit einem Zeiger auf den Puffer, der die Delta Daten enthält.

*lptarget*

vorgenommen Ein Zeiger auf die [DELTA_OUTPUT](/previous-versions/bb417345(v=msdn.10)#delta-output-structure) Struktur, in der das Ziel geschrieben werden soll.

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

[Delta frei](msdelta-deltafree.md)
