---
title: D3DPERF_SetOptions-Funktion
description: Legen Sie profiler-Optionen fest, die vom Zielprogramm angegeben werden.
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
ms.openlocfilehash: 579c07d8f93696e4e3c83b1e61c1ff5fca65e12b5a7cf0a5937a254ecc6dc306
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118805735"
---
# <a name="d3dperf_setoptions-function"></a>D3DPERF_SetOptions-Funktion

Legen Sie profiler-Optionen fest, die vom Zielprogramm angegeben werden.

## <a name="syntax"></a>Syntax

```cpp
int WINAPI D3DPERF_SetOptions(
  DWORD dwOptions
);
```

## <a name="parameters"></a>Parameter

`dwOptions`

Benutzeroptionen, die von PIX erkannt werden können. Legen Sie diesen Aufsatz auf 1 fest, um PIX zu benachrichtigen, dass das Zielprogramm keine Berechtigung zum Profilieren erteilt.

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Zielplattform** | Windows |
| **Header** | d3d9.h |
| **Bibliothek** | d3d9.lib |
| **Dll** | d3d9.dll |