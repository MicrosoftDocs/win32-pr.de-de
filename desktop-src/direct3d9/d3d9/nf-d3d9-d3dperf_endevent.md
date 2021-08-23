---
title: D3DPERF_EndEvent-Funktion
description: Markiert das Ende eines benutzerdefinierten Ereignisses. PIX kann dieses Ereignis verwenden, um eine Aktion auszulösen.
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
- D3DPERF_EndEvent
targetos: Windows
ms.openlocfilehash: bd12780dfdfcb86e83495ae877d8debf1e768517826329ccee8d40ffaa88fbbe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989250"
---
# <a name="d3dperf_endevent-function"></a>D3DPERF_EndEvent-Funktion

Markiert das Ende eines benutzerdefinierten Ereignisses. PIX kann dieses Ereignis verwenden, um eine Aktion auszulösen.

## <a name="syntax"></a>Syntax

```cpp
int WINAPI D3DPERF_EndEvent(void);
```

## <a name="return-value"></a>Rückgabewert

Die Ebene der Hierarchie, in der das Ereignis endet. Wenn ein Fehler auftritt, ist dieser Wert negativ.

## <a name="requirements"></a>Anforderungen
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Zielplattform** | Windows |
| **Header** | d3d9.h |
| **Bibliothek** | d3d9.lib |
| **Dll** | d3d9.dll |