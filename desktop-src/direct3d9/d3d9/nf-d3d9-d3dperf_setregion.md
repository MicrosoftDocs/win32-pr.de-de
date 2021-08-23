---
title: D3DPERF_SetRegion-Funktion
description: Markieren Sie eine Reihe von Frames mit der angegebenen Farbe und dem angegebenen Namen in der PIXRun-Datei. Diese Funktion wird von PIX derzeit nicht unterstützt.
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
- D3DPERF_SetRegion
targetos: Windows
ms.openlocfilehash: 05884fe8a3b104588a941dcaf3089a1c0f6f8eab4f4a01e143470f73454ad4ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989260"
---
# <a name="d3dperf_setregion-function"></a>D3DPERF_SetRegion-Funktion

Markieren Sie eine Reihe von Frames mit der angegebenen Farbe und dem angegebenen Namen in der PIXRun-Datei. Diese Funktion wird von PIX derzeit nicht unterstützt.

## <a name="syntax"></a>Syntax

```cpp
void WINAPI D3DPERF_SetRegion(
  D3DCOLOR col,
  LPCWSTR wszName
);
```

## <a name="parameters"></a>Parameter

`col`

Ereignisfarbe. Dies ist die Farbe zum Anzeigen des Ereignisses in der Ereignisansicht.

`wszName`

Ereignisname.

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Um die Analyse zu vereinfachen, kann das Zielprogramm farbe verwenden, um jede Ebene eines Zielprogramms zu markieren.

## <a name="requirements"></a>Anforderungen
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Zielplattform** | Windows |
| **Header** | d3d9.h |
| **Bibliothek** | d3d9.lib |
| **Dll** | d3d9.dll |