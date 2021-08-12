---
description: Benachrichtigt den DWM über ein eingehendes Update an einer freigegebenen Fensteroberfläche.
ms.assetid: 8357D977-E501-47D7-85BC-7C8954C6D166
title: DwmDxUpdateWindowSharedSurface-Funktion
ms.topic: reference
ms.date: 11/27/2018
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Dwmapi.dll
api_name:
- DwmDxUpdateWindowSharedSurface
ms.openlocfilehash: 9eac390cd6ccf79ed3f916f4c9605b938ab9fd338df3643301d7f5e5c900c0d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118280120"
---
# <a name="dwmdxupdatewindowsharedsurface-function"></a>DwmDxUpdateWindowSharedSurface-Funktion

Benachrichtigt den DWM über ein eingehendes Update an einer freigegebenen Fensteroberfläche.

## <a name="syntax"></a>Syntax

```C++
HRESULT WINAPI DwmDxUpdateWindowSharedSurface(
  _In_     HWND     hwnd,
  _In_     UINT64   uiUpdateId,
  _In_     DWORD    dwFlags,
  _In_opt_ HMONITOR hmonitorAssociation,
  _In_     RECT     *prc
);
```

## <a name="parameters"></a>Parameter

`hwnd`

Ein [**HWND,**](/windows/desktop/winprog/windows-data-types) der das zu aktualisierende Fenster angibt.

`uiUpdateId`

Die Update-ID, die von [**DwmDxGetWindowSharedSurface**](dwmdxgetwindowsharedsurface.md)abgerufen wurde.

`dwFlags`

Reserviert.

`hmonitorAssociation`

Reserviert.

`prc`

Der Rect des zu aktualisierenden Fensters im Fensterkoordinatenraum. Ein NULL-Rechteck gibt an, dass kein Bereich aktualisiert wurde.

## <a name="return-value"></a>Rückgabewert

**S \_ OK,** wenn erfolgreich, andernfalls ein FAILED **HRESULT.**

## <a name="remarks"></a>Hinweise

Diese API ist für die Implementierung eines Grafiktreibers oder einer Runtime vorgesehen. Eine Anwendung ruft diese Methode möglicherweise nicht auf. Diese Dokumentation gilt nur für Windows 7, und es ist nicht garantiert, dass diese API in anderen Versionen von Windows vorhanden ist oder sich auf ähnliche Weise verhält. Diese Funktion ist in keinem Header oder in einer statischen Linkbibliothek vorhanden und befindet sich unter der Ordnungszahl 101 in dwmapi.dll.

Diese Methode sollte immer nur aufgerufen werden, nachdem [**DwmDxGetWindowSharedSurface**](dwmdxgetwindowsharedsurface.md) **S \_ OK** zurückgibt, und muss in diesem Szenario aufgerufen werden, unabhängig davon, ob die Oberfläche aktualisiert wird oder nicht.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-|-|
| Unterstützte Mindestversion (Client) | nur Windows 7 \[ Desktop-Apps\] |
| Unterstützte Mindestversion (Server) | Nicht unterstützt |
| Ende des Supports (Client) | Windows 7 |
| Header | N/V |
| DLL | Dwmapi.dll |
