---
title: WM_DWMSENDICONICLIVEPREVIEWBITMAP Meldung (dwmapi. h)
description: Weist ein Fenster an, eine statische Bitmap bereitzustellen, die als Live Vorschau (auch als Vorschau Vorschau bezeichnet) dieses Fensters verwendet werden soll.
ms.assetid: 24bf3b42-a850-4aa5-966a-29baab6b4d21
keywords:
- WM_DWMSENDICONICLIVEPREVIEWBITMAP Meldung Desktopfenster-Manager
topic_type:
- apiref
api_name:
- WM_DWMSENDICONICLIVEPREVIEWBITMAP
api_location:
- Dwmapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21f73076ab313da66171bc8265f7f4e7d068f93e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477001"
---
# <a name="wm_dwmsendiconiclivepreviewbitmap-message"></a>WM \_ dwmsendiconiclivepreviewbitmap-Meldung

Weist ein Fenster an, eine statische Bitmap bereitzustellen, die als *Live Vorschau* (auch als *Vorschau Vorschau* bezeichnet) dieses Fensters verwendet werden soll.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Nicht verwendet.

</dd> <dt>

*lParam* 
</dt> <dd>

Nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.

## <a name="remarks"></a>Bemerkungen

Eine *Live Vorschau* (auch als *Vorschau Vorschau* bezeichnet) eines Fensters wird angezeigt, wenn ein Benutzer den Mauszeiger über die Miniaturansicht des Fensters in der Taskleiste bewegt oder den Miniatur Ansichts Fokus im Alt + Tab-Fenster verschiebt. Diese Ansicht ist eine Vorschau des Fensters in voller Größen und kann eine Live Momentaufnahme oder eine Darstellung darstellen.

Desktopfenster-Manager (DWM) sendet diese Nachricht an ein Fenster, wenn alle der folgenden Situationen zutreffen:

-   Die Live Vorschau wurde im Fenster aufgerufen.
-   Das [**dwmwa-Attribut \_ enthält ein \_ berühmtes \_ Bitmap**](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmwindowattribute) -Attribut, das im Fenster festgelegt ist.
-   Eine legendäre Darstellung ist die einzige, die für dieses Fenster vorhanden ist.

Das Fenster, in dem diese Meldung empfangen wird, sollte durch das Erstellen einer Bitmap mit vollständigem skalieren Antworten. Das Fenster ruft dann die [**dwmseticoniclivepreviewbitmap**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap) -Funktion auf, um die Live Vorschau festzulegen. Wenn im Fenster keine Bitmap in einem bestimmten Zeitraum festgelegt wird, verwendet DWM eine eigene Standarddarstellung für das Fenster.

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt eine Antwort auf die **WM- \_ dwmsendiconiclivepreviewbitmap** -Nachricht. Im Beispiel wird die [**dwmtarticoniclivepreviewbitmap**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap) -Funktion mit einem Handle für eine angepasste, geräteunabhängige Bitmap aufgerufen, die als Darstellung des Fensters verwendet werden soll.


```C++
        case WM_DWMSENDICONICLIVEPREVIEWBITMAP:
        {
            // This window is being asked to provide a bitmap to show in Peek preview.
            // This indicates the thumbnail in the taskbar is being previewed.
            RECT rectWindow = {0, 0, 0, 0};
            if (GetClientRect(hwnd, &rectWindow))
            {
                nWidth = rectWindow.right - rectWindow.left;
                nHeight = rectWindow.bottom - rectWindow.top;
            }

            hbm = CreateDIB(nWidth, nHeight);
            if (hbm)
            {
                hr = DwmSetIconicLivePreviewBitmap(hwnd, hbm, NULL, DWM_SIT_DISPLAYFRAME);
                DeleteObject(hbm);
            }
        }
        break;
```



Den gesamten Code finden Sie im Beispiel [Anpassen einer Miniaturansicht und Live Vorschau Bitmap](dwm-sample-customizethumbnail.md) .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>Dwmapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**WM \_ dwmsendianicminiatur**](wm-dwmsendiconicthumbnail.md)
</dt> <dt>

[**Dwminvalidateiconfiguration**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwminvalidateiconicbitmaps)
</dt> </dl>

 

 





