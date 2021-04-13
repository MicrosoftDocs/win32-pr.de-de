---
title: D3DPERF_SetMarker-Funktion
description: Markieren Sie ein sofortiges Ereignis. Pix kann dieses Ereignis verwenden, um eine Aktion zu initiieren.
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
- D3DPERF_SetMarker
targetos: Windows
ms.openlocfilehash: 8eef59b9914ce30b95751641c16becf1963b19e0
ms.sourcegitcommit: 517a888e0370b9ec64c451635f12d60245ff5ae3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/08/2020
ms.locfileid: "104390005"
---
# <a name="d3dperf_setmarker-function"></a>D3DPERF_SetMarker-Funktion

Markieren Sie ein sofortiges Ereignis. Pix kann dieses Ereignis verwenden, um eine Aktion zu initiieren.

## <a name="syntax"></a>Syntax

```cpp
void WINAPI D3DPERF_SetMarker(
  D3DCOLOR col,
  LPCWSTR wszName
);
```

## <a name="parameters"></a>Parameter

`col`

Ereignis Farbe. Dies ist die Farbe, um das Ereignis in der Ereignisansicht anzuzeigen.

`wszName`

Ereignisname.

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Bei sofortigen Benutzer Ereignissen werden andere Ereignisse nicht in eckige Klammern oder gruppiert. Wenn der Benutzer z. b. eine Waffe in einem Spiel auslöst, könnte ein Ereignis vom Typ " *shot* " ausgelöst werden, indem ein **D3DPERF_SetMarker** aufgerufen wird. Wenn Sie mehrere Ereignisse unter einem einzelnen benutzerdefinierten Namen gruppieren möchten, verwenden Sie **D3DPERF_BeginEvent** und **D3DPERF_EndEvent** anstelle von **D3DPERF_SetMarker**.

## <a name="requirements"></a>Anforderungen
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Zielplattform** | Windows |
| **Header** | d3d9. h |
| **Bibliothek** | d3d9. lib |
| **DLL** | d3d9.dll |