---
title: D3DPERF_SetOptions-Funktion
description: Festlegen der vom Zielprogramm angegebenen Profiler-Optionen.
ms.localizationpriority: low
ms.topic: reference
ms.date: 04/06/2020
req.lib: d3d9.lib
req.dll: d3d9.dll
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- d3d9.dll
api_name:
- D3DPERF_SetOptions
targetos: Windows
ms.openlocfilehash: 8bd877469864ccdaa833ce80d00eb06ae5fc18de
ms.sourcegitcommit: 517a888e0370b9ec64c451635f12d60245ff5ae3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/08/2020
ms.locfileid: "104472333"
---
# <a name="d3dperf_setoptions-function"></a>D3DPERF_SetOptions-Funktion

Festlegen der vom Zielprogramm angegebenen Profiler-Optionen.

## <a name="syntax"></a>Syntax

```cpp
int WINAPI D3DPERF_SetOptions(
  DWORD dwOptions
);
```

## <a name="parameters"></a>Parameter

`dwOptions`

Benutzeroptionen, die von Pix erkannt werden. Legen Sie diese Einstellung auf 1 fest, um pix zu benachrichtigen, dass das Zielprogramm keine Berechtigung für die Profilerstellung erteilt.

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Zielplattform** | Windows |
| **Header** | d3d9. h |
| **Bibliothek** | d3d9. lib |
| **DLL** | d3d9.dll |