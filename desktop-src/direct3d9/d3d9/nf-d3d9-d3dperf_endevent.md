---
title: D3DPERF_EndEvent-Funktion
description: Markiert das Ende eines benutzerdefinierten Ereignisses. Pix kann dieses Ereignis verwenden, um eine Aktion zu initiieren.
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
ms.openlocfilehash: 91c2a6a19b926cd9f5549fae084ce8973432b0f2
ms.sourcegitcommit: 517a888e0370b9ec64c451635f12d60245ff5ae3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/08/2020
ms.locfileid: "104390006"
---
# <a name="d3dperf_endevent-function"></a>D3DPERF_EndEvent-Funktion

Markiert das Ende eines benutzerdefinierten Ereignisses. Pix kann dieses Ereignis verwenden, um eine Aktion zu initiieren.

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
| **Header** | d3d9. h |
| **Bibliothek** | d3d9. lib |
| **DLL** | d3d9.dll |