---
description: Ruft die freigegebene DirectX-Oberfläche ab, die ein bestimmtes Fenster unterstützt. Diese Oberfläche kann in geschrieben werden, um den Inhalt des Fensters zu aktualisieren.
ms.assetid: 500CF5B4-0D56-4201-91F4-7333E45DACEE
title: DwmDxGetWindowSharedSurface-Funktion
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
ms.openlocfilehash: 47f8c75ee55521c0f1da4151f5161cf44a63dc51aab5658edbca288cb8edce24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118280130"
---
# <a name="dwmdxgetwindowsharedsurface-function"></a>DwmDxGetWindowSharedSurface-Funktion

Ruft die freigegebene DirectX-Oberfläche ab, die ein bestimmtes Fenster unterstützt. Diese Oberfläche kann in geschrieben werden, um den Inhalt des Fensters zu aktualisieren.

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

Ein [**HWND,**](/windows/desktop/winprog/windows-data-types) der das zu aktualisierende Fenster angibt.

`luidAdapter`

Die [**LUID**](/previous-versions/bb401655(v%3dmsdn.10)) des Adapters, in dem sich die Oberfläche befinden soll.

`hmonitorAssociation`

Reserviert.

`dwFlags`

Dieser Parameter kann einer der folgenden Werte oder ggf. eine bitweise OR-Kombination aus mehreren Werten sein.

| Wert | Bedeutung |
|-|-|
| <span id="DWM_REDIRECTION_FLAG_WAIT"></span><span id="dwm_redirection_flag_wait"></span><dl> <dt>**DWM \_ \_UMLEITUNGSFLAG \_ WARTE**</dt> <dt>0</dt> </dl> | Bewirkt, dass die Funktion blockiert wird, bis eine vertikale Synchronisierung (VSync) seit dem letzten erfolgreichen Aufruf der Funktion vergangen ist. |
| <span id="DWM_REDIRECTION_FLAG_SUPPORT_PRESENT_TO_GDI_SURFACE"></span><span id="dwm_redirection_flag_support_present_to_gdi_surface"></span><dl> <dt>**DWM \_ UNTERSTÜTZUNG DES \_ UMLEITUNGSFLAGS \_ FÜR \_ \_ \_ GDI \_ SURFACE**</dt> <dt>0x10</dt> </dl> | Gibt an, dass die aufrufende Anwendung in der Lage ist, auf einer freigegebenen GDI-Oberfläche darzustellen. |

`pfmtWindow`

Bei eingabe das gewünschte Format der Oberfläche. Bei der Ausgabe das tatsächliche Format der zurückgegebenen Oberfläche.

`phDxSurface`

Bei der Ausgabe das freigegebene Handle für die Oberfläche.

`puiUpdateId`

Bei der Ausgabe die ID des Updates.

## <a name="return-value"></a>Rückgabewert

Diese Funktion kann einen dieser Werte zurückgeben.

| Rückgabecode | Beschreibung |
|-|-|
| **S \_ OK** | Der Aufruf war erfolgreich, und Sie sollten die Oberfläche aktualisieren. Achten Sie darauf, die Update-ID an [D3DKMTRender](/windows-hardware/drivers/ddi/content/d3dkmthk/nf-d3dkmthk-d3dkmtrender) zu übergeben (im **PresentHistoryToken-Element** der **D3DKMT-RENDER-Struktur, \_** wenn das Update übermittelt wird, und dann sollte [**DwmDxUpdateWindowSharedSurface**](dwmdxupdatewindowsharedsurface.md) mit der gleichen Update-ID aufgerufen werden. Beachten Sie, dass **DwmDxUpdateWindowSharedSurface** unabhängig davon aufgerufen werden sollte, ob die Oberfläche tatsächlich aktualisiert wurde oder nicht. |
| **DWM \_ S \_ GDI \_ REDIRECTION \_ SURFACE** | Der Aufruf war erfolgreich, und Sie sollten die Oberfläche aktualisieren, indem Sie [D3DKMTPresent](/windows-hardware/drivers/ddi/content/d3dkmthk/nf-d3dkmthk-d3dkmtpresent)aufrufen und das Modell des **PresentHistoryToken-Elements** auf **D3DKMT \_ PM \_ REDIRECTED \_ BLT** festlegen und die Update-ID im **Blt-Member** der Union bereitstellen.  Dieser Wert wird nur zurückgegeben, wenn **DWM \_ REDIRECTION \_ FLAG SUPPORT PRESENT TO \_ \_ \_ \_ GDI \_ SURFACE** in *dwFlags* angegeben wurde. |
| **DWM \_ \_ E-ADAPTER \_ NICHT \_ GEFUNDEN** | Der Wert von *luidAdapter* ist ungültig. |
| **DWM \_ E \_ COMPOSITIONDISABLED** | DWM ist derzeit nicht aktiviert, und die Anwendung muss eine andere Möglichkeit bieten. |

## <a name="remarks"></a>Hinweise

Diese API ist für die Implementierung eines Grafiktreibers oder einer Runtime vorgesehen. Eine Anwendung ruft diese Methode möglicherweise nicht auf. Diese Dokumentation gilt nur für Windows 7, und es ist nicht garantiert, dass diese API in anderen Versionen von Windows vorhanden ist oder sich auf ähnliche Weise verhält. Diese Funktion ist in keinem Header oder in einer statischen Linkbibliothek vorhanden und befindet sich unter der Ordnungszahl 100 in dwmapi.dll.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-|-|
| Unterstützte Mindestversion (Client) | nur Windows 7 \[ Desktop-Apps\] |
| Unterstützte Mindestversion (Server) | Nicht unterstützt |
| Ende des Supports (Client) | Windows 7 |
| Header | N/V |
| DLL | Dwmapi.dll |
