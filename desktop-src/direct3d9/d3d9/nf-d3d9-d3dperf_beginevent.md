---
title: D3DPERF_BeginEvent-Funktion
description: Markiert den Anfang eines benutzerdefinierten Ereignisses. Pix kann dieses Ereignis verwenden, um eine Aktion zu initiieren.
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
- D3DPERF_BeginEvent
targetos: Windows
ms.openlocfilehash: f6732d4ce969cbd26cdb32f4750654c7baacd324
ms.sourcegitcommit: 517a888e0370b9ec64c451635f12d60245ff5ae3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/08/2020
ms.locfileid: "104390004"
---
# <a name="d3dperf_beginevent-function"></a>D3DPERF_BeginEvent-Funktion

Markiert den Anfang eines benutzerdefinierten Ereignisses. Pix kann dieses Ereignis verwenden, um eine Aktion zu initiieren.

## <a name="syntax"></a>Syntax

```cpp
int WINAPI D3DPERF_BeginEvent(
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

Die null basierte Ebene der Hierarchie, in der dieses Ereignis beginnt. Wenn ein Fehler auftritt, wird der Rückgabewert negativ sein.

## <a name="remarks"></a>Bemerkungen

Benutzerdefinierte Ereignisse gruppieren andere Ereignisse auf eine Weise, die für das Zielprogramm sinnvoll ist, damit Sie in Leistungsprofil Erstellungs Tools besser dargestellt werden können. Beispielsweise kann ein *Draw-Spaceship* -Ereignis eine Reihe von Direct3D-aufrufen Klammern, die das Zeichnen eines-Spaceship in einem Spiel verarbeiten. Ereignisse können eingebettet werden.

Jeder **D3DPERF_BeginEvent** -aufrufsbefehl sollte über einen passenden **D3DPERF_EndEvent** aufgerufen werden. Sofortige Ereignisse (bei denen andere Ereignisse nicht eckige Klammern sind) sollten mithilfe von **D3DPERF_SetMarker** und nicht durch **D3DPERF_BeginEvent** und **D3DPERF_EndEvent** gekennzeichnet werden.

## <a name="requirements"></a>Anforderungen
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Zielplattform** | Windows |
| **Header** | d3d9. h |
| **Bibliothek** | d3d9. lib |
| **DLL** | d3d9.dll |