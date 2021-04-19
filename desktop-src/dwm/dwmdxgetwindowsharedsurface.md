---
description: Ruft die freigegebene DirectX-Oberfläche ab, die ein bestimmtes Fenster sichert. Diese Oberfläche kann geschrieben werden, um den Inhalt des Fensters zu aktualisieren.
ms.assetid: 500CF5B4-0D56-4201-91F4-7333E45DACEE
title: Dwmdxgetwindowsharedsurface-Funktion
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
- DwmDxGetWindowSharedSurface
ms.openlocfilehash: 15e7829383ce23e5bc06bb61ab9c0c224ab18182
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350542"
---
# <a name="dwmdxgetwindowsharedsurface-function"></a>Dwmdxgetwindowsharedsurface-Funktion

Ruft die freigegebene DirectX-Oberfläche ab, die ein bestimmtes Fenster sichert. Diese Oberfläche kann geschrieben werden, um den Inhalt des Fensters zu aktualisieren.

## <a name="syntax"></a>Syntax

```C++
HRESULT WINAPI DwmDxGetWindowSharedSurface(
  _In_     HWND        hwnd,
  _In_     LUID        luidAdapter,
  _In_opt_ HMONITOR    hmonitorAssociation,
  _In_     DWORD       dwFlags,
  _Inout_  DXGI_FORMAT *pfmtWindow,
  _Out_    HANDLE      *phDxSurface,
  _Out_    UINT64      *puiUpdateId
);
```

## <a name="parameters"></a>Parameter

`hwnd`

Ein [**HWND**](/windows/desktop/winprog/windows-data-types) , das das zu Aktualisier Ende Fenster angibt.

`luidAdapter`

Die [**LUID**](/previous-versions/bb401655(v%3dmsdn.10)) des Adapters, auf dem sich die Oberfläche befinden soll.

`hmonitorAssociation`

Reserviert.

`dwFlags`

Bei diesem Parameter kann es sich um einen der folgenden Werte oder eine bitweise OR-Kombination mehrerer Werte handeln.

| Wert | Bedeutung |
|-|-|
| <span id="DWM_REDIRECTION_FLAG_WAIT"></span><span id="dwm_redirection_flag_wait"></span><dl> <dt>**DWM \_ Umleitungs Kennzeichen, \_ \_ Wartezeit**</dt> <dt>0</dt> </dl> | Bewirkt, dass die-Funktion blockiert wird, bis eine vertikale Synchronisierung (VSYNC) seit dem letzten Aufruf der Funktion erfolgreich war. |
| <span id="DWM_REDIRECTION_FLAG_SUPPORT_PRESENT_TO_GDI_SURFACE"></span><span id="dwm_redirection_flag_support_present_to_gdi_surface"></span><dl> <dt>**DWM \_ \_ \_ Unterstützung für Umleitungs Kennzeichen \_ \_ für \_ GDI- \_ Oberfläche**</dt> <dt>0x10</dt> vorhanden </dl> | Gibt an, dass die aufrufenden Anwendung eine freigegebene GDI-Oberfläche darstellen kann. |

`pfmtWindow`

Bei Eingabe das gewünschte Format der-Oberfläche. Bei Ausgabe das tatsächliche Format der zurückgegebenen Oberfläche.

`phDxSurface`

Bei der Ausgabe das freigegebene Handle für die-Oberfläche.

`puiUpdateId`

Bei Ausgabe die ID des Updates.

## <a name="return-value"></a>Rückgabewert

Diese Funktion kann einen dieser Werte zurückgeben.

| Rückgabecode | Beschreibung |
|-|-|
| **S \_ OK** | Der Aufruf war erfolgreich, und Sie sollten die Oberfläche aktualisieren und dabei sicherstellen, dass die Update-ID an [D3DKMTRender](/windows-hardware/drivers/ddi/content/d3dkmthk/nf-d3dkmthk-d3dkmtrender) übergeben wird (im Element " **presenthistorytoken** " der **D3DKMT- \_ Renderstruktur** , wenn das Update übermittelt wird, und " [**dwmdxupdatewindowsharedsurface**](dwmdxupdatewindowsharedsurface.md) " sollte mit derselben Update-ID aufgerufen werden. Beachten Sie, dass **dwmdxupdatewindowsharedsurface** unabhängig davon aufgerufen werden sollte, ob die Oberfläche tatsächlich aktualisiert wurde. |
| **DWM \_ S- \_ GDI- \_ Umleitungs \_ Oberfläche** | Der Aufruf war erfolgreich, und Sie sollten die Oberfläche durch Aufrufen von [D3DKMTPresent](/windows-hardware/drivers/ddi/content/d3dkmthk/nf-d3dkmthk-d3dkmtpresent)aktualisieren und das **Modell** des **presenthistorytoken** -Members auf **D3DKMT \_ PM \_ umgeleitete \_ blt** festlegen und die Update-ID im **blt** -Member der Union angeben. Dieser Wert wird nur zurückgegeben **, wenn \_ die Unterstützung von DWM-Umleitungs Kennzeichen \_ \_ \_ \_ für \_ GDI- \_ Oberfläche** in *dwFlags* angegeben wurde. |
| **der DWM \_ E- \_ Adapter wurde \_ nicht \_ gefunden.** | Der Wert von *luidadapter* ist ungültig. |
| **DWM \_ E \_ compositiondeaktiviert** | DWM ist zurzeit nicht aktiviert, und die Anwendung muss eine andere Möglichkeit darstellen. |

## <a name="remarks"></a>Bemerkungen

Diese API ist für die Implementierung eines Grafik Treibers oder einer Laufzeit vorgesehen. Eine Anwendung ruft diese Methode möglicherweise nicht auf. Diese Dokumentation ist nur für Windows 7 gültig, und diese API ist nicht garantiert vorhanden und verhält sich in anderen Versionen von Windows nicht auf ähnliche Weise. Diese Funktion ist in keiner Header-oder statischen Link Bibliothek vorhanden und befindet sich in dwmapi.dll in der Ordnungszahl 100.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-|-|
| Unterstützte Mindestversion (Client) | Nur Windows 7 \[ -Desktop-Apps\] |
| Unterstützte Mindestversion (Server) | Nicht unterstützt |
| Ende des Supports (Client) | Windows 7 |
| Header | N/V |
| DLL | Dwmapi.dll |
