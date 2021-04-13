---
description: Benachrichtigt den DWM-Code über ein eingehender Update für eine freigegebene Fenster Oberfläche.
ms.assetid: 8357D977-E501-47D7-85BC-7C8954C6D166
title: Dwmdxupdatewindowsharedsurface-Funktion
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
ms.openlocfilehash: 7649e96fb3a16458b518d0fc2c6dd09725a4b0ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528130"
---
# <a name="dwmdxupdatewindowsharedsurface-function"></a>Dwmdxupdatewindowsharedsurface-Funktion

Benachrichtigt den DWM-Code über ein eingehender Update für eine freigegebene Fenster Oberfläche.

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

Ein [**HWND**](/windows/desktop/winprog/windows-data-types) , das das zu Aktualisier Ende Fenster angibt.

`uiUpdateId`

Die Update-ID, die von [**dwmdxgetwindowsharedsurface**](dwmdxgetwindowsharedsurface.md)abgerufen wird.

`dwFlags`

Reserviert.

`hmonitorAssociation`

Reserviert.

`prc`

Der Rect des zu aktualisierenden Fensters im Fenster Koordinaten Bereich. Ein NULL-Rechteck gibt an, dass keine Region aktualisiert wurde.

## <a name="return-value"></a>Rückgabewert

**S \_ OK** , wenn erfolgreich, andernfalls ein **HRESULT** mit Fehlern.

## <a name="remarks"></a>Bemerkungen

Diese API ist für die Implementierung eines Grafik Treibers oder einer Laufzeit vorgesehen. Eine Anwendung ruft diese Methode möglicherweise nicht auf. Diese Dokumentation ist nur für Windows 7 gültig, und diese API ist nicht garantiert vorhanden und verhält sich in anderen Versionen von Windows nicht auf ähnliche Weise. Diese Funktion ist in keiner Header-oder statischen Link Bibliothek vorhanden und befindet sich in dwmapi.dll in der Ordnungszahl 101.

Diese Methode sollte nur aufgerufen werden, nachdem " [**dwmdxgetwindowsharedsurface**](dwmdxgetwindowsharedsurface.md) " den Wert " **\_ OK**" zurückgegeben hat und in diesem Szenario aufgerufen werden muss, unabhängig davon, ob die Oberfläche aktualisiert wurde oder nicht.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-|-|
| Unterstützte Mindestversion (Client) | Nur Windows 7 \[ -Desktop-Apps\] |
| Unterstützte Mindestversion (Server) | Nicht unterstützt |
| Ende des Supports (Client) | Windows 7 |
| Header | N/V |
| DLL | Dwmapi.dll |
