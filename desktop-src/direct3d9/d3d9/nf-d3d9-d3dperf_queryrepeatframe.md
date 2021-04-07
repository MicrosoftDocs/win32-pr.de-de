---
title: D3DPERF_QueryRepeatFrame-Funktion
description: Bestimmen Sie, ob ein leistungsprofiler anfordert, dass der aktuelle Frame zur Leistungsanalyse erneut an Direct3D übermittelt wird. Diese Funktion wird zurzeit von Pix nicht unterstützt.
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
ms.openlocfilehash: c4054a0704fd0258483ee0d3d3d555cb5eabe7f9
ms.sourcegitcommit: 517a888e0370b9ec64c451635f12d60245ff5ae3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/08/2020
ms.locfileid: "103723877"
---
# <a name="d3dperf_queryrepeatframe-function"></a>D3DPERF_QueryRepeatFrame-Funktion

Bestimmen Sie, ob ein leistungsprofiler anfordert, dass der aktuelle Frame zur Leistungsanalyse erneut an Direct3D übermittelt wird. Diese Funktion wird zurzeit von Pix nicht unterstützt.

## <a name="syntax"></a>Syntax

```cpp
BOOL WINAPI D3DPERF_QueryRepeatFrame( void );
```

## <a name="return-value"></a>Rückgabewert

Wenn der Rückgabewert true ist, sollte der Aufrufer dieselbe Aufruf Sequenz wiederholen. Wenn false, sollte der Aufrufer fortgesetzt werden.

## <a name="remarks"></a>Bemerkungen

Die-Funktion sollte unmittelbar nach IDirect3DDevice9 aufgerufen werden **::P Resent** aufgerufen wird.

## <a name="requirements"></a>Anforderungen
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Zielplattform** | Windows |
| **Header** | d3d9. h |
| **Bibliothek** | d3d9. lib |
| **DLL** | d3d9.dll |