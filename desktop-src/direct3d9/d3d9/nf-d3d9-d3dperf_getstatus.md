---
title: D3DPERF_GetStatus-Funktion
description: Bestimmen Sie den aktuellen Status des Profilers aus dem Zielprogramm.
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
- D3DPERF_GetStatus
targetos: Windows
ms.openlocfilehash: 626d56dd449b0a0aa92e85c82dabda119900680d
ms.sourcegitcommit: 517a888e0370b9ec64c451635f12d60245ff5ae3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/08/2020
ms.locfileid: "104314465"
---
# <a name="d3dperf_getstatus-function"></a>D3DPERF_GetStatus-Funktion

Bestimmen Sie den aktuellen Status des Profilers aus dem Zielprogramm.

## <a name="syntax"></a>Syntax

```cpp
DWORD WINAPI D3DPERF_GetStatus( void );
```

## <a name="return-value"></a>Rückgabewert

Ein Wert ungleich NULL, wenn pix die Profilerstellung für das Zielprogramm durchläuft. andernfalls 0 (null).

## <a name="requirements"></a>Anforderungen
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Zielplattform** | Windows |
| **Header** | d3d9. h |
| **Bibliothek** | d3d9. lib |
| **DLL** | d3d9.dll |