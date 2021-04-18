---
title: D3DPERF_SetRegion-Funktion
description: Markieren Sie in der Datei "pixrun" eine Reihe von Frames mit der angegebenen Farbe und dem angegebenen Namen. Diese Funktion wird zurzeit von Pix nicht unterstützt.
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
ms.openlocfilehash: 650cc6063865da5ce30b97ed1468c1718ace5da6
ms.sourcegitcommit: 517a888e0370b9ec64c451635f12d60245ff5ae3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/08/2020
ms.locfileid: "106340483"
---
# <a name="d3dperf_setregion-function"></a>D3DPERF_SetRegion-Funktion

Markieren Sie in der Datei "pixrun" eine Reihe von Frames mit der angegebenen Farbe und dem angegebenen Namen. Diese Funktion wird zurzeit von Pix nicht unterstützt.

## <a name="syntax"></a>Syntax

```cpp
void WINAPI D3DPERF_SetRegion(
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

Um die Analyse zu vereinfachen, kann das Zielprogramm Farben verwenden, um jede Ebene eines Zielprogramms zu markieren.

## <a name="requirements"></a>Anforderungen
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Zielplattform** | Windows |
| **Header** | d3d9. h |
| **Bibliothek** | d3d9. lib |
| **DLL** | d3d9.dll |