---
title: D3DPERF_QueryRepeatFrame-Funktion
description: Bestimmen Sie, ob ein Leistungsprofiler an fordert, dass der aktuelle Frame zur Leistungsanalyse erneut an Direct3D ausgegeben wird. Diese Funktion wird derzeit von PIX nicht unterstützt.
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
- D3DPERF_QueryRepeatFrame
targetos: Windows
ms.openlocfilehash: dbc46ff05b6fa1846bb0e1ffc1fca928ca1d68ee38a43708c77a109b61a405da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119751240"
---
# <a name="d3dperf_queryrepeatframe-function"></a>D3DPERF_QueryRepeatFrame-Funktion

Bestimmen Sie, ob ein Leistungsprofiler an fordert, dass der aktuelle Frame zur Leistungsanalyse erneut an Direct3D ausgegeben wird. Diese Funktion wird derzeit von PIX nicht unterstützt.

## <a name="syntax"></a>Syntax

```cpp
BOOL WINAPI D3DPERF_QueryRepeatFrame( void );
```

## <a name="return-value"></a>Rückgabewert

Wenn der Rückgabewert TRUE ist, sollte der Aufrufer dieselbe Sequenz von Aufrufen wiederholen. False gibt an, dass der Aufrufer fortfahren sollte.

## <a name="remarks"></a>Hinweise

Die Funktion sollte sofort aufgerufen werden, nachdem **IDirect3DDevice9::P resent** aufgerufen wurde.

## <a name="requirements"></a>Anforderungen
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Zielplattform** | Windows |
| **Header** | d3d9.h |
| **Bibliothek** | d3d9.lib |
| **Dll** | d3d9.dll |