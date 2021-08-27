---
title: D3DPERF_GetStatus-Funktion
description: Bestimmen Sie den aktuellen Zustand des Profilers aus dem Zielprogramm.
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
ms.openlocfilehash: 78ff9eda9ab224faf4b2a117f6230e3361664bbfea35d8b2a8484ba7f5ab764a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118805745"
---
# <a name="d3dperf_getstatus-function"></a>D3DPERF_GetStatus-Funktion

Bestimmen Sie den aktuellen Zustand des Profilers aus dem Zielprogramm.

## <a name="syntax"></a>Syntax

```cpp
DWORD WINAPI D3DPERF_GetStatus( void );
```

## <a name="return-value"></a>Rückgabewert

Ein Wert, der nicht 0 (null) ist, wenn PIX eine Profilerstellung für das Zielprogramm erstellt. andernfalls 0 (null).

## <a name="requirements"></a>Anforderungen
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Zielplattform** | Windows |
| **Header** | d3d9.h |
| **Bibliothek** | d3d9.lib |
| **Dll** | d3d9.dll |