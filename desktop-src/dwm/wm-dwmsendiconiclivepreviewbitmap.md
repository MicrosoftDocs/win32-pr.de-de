---
title: WM_DWMSENDICONICLIVEPREVIEWBITMAP Meldung (Dwmapi.h)
description: Weist ein Fenster an, eine statische Bitmap bereitzustellen, die als Livevorschau (auch als Vorschauversion bezeichnet) dieses Fensters verwendet werden kann.
ms.assetid: 24bf3b42-a850-4aa5-966a-29baab6b4d21
keywords:
- WM_DWMSENDICONICLIVEPREVIEWBITMAP Desktopfenster-Manager
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
ms.openlocfilehash: a7742b70afad62a42378e50a06a6e40e503bee72309f5f233f9cf8bf62cf41d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118985246"
---
# <a name="wm_dwmsendiconiclivepreviewbitmap-message"></a>WM \_ DWMSENDICONICLIVEPREVIEWBITMAP-Meldung

Weist ein Fenster an, eine statische Bitmap bereitzustellen, die als *Livevorschau* (auch als *Vorschauversion* bezeichnet) dieses Fensters verwendet werden soll.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Wird nicht verwendet.

</dd> <dt>

*lParam* 
</dt> <dd>

Wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn eine Anwendung diese Nachricht verarbeitet, sollte sie 0 (null) zurückgeben.

## <a name="remarks"></a>Hinweise

Eine *Livevorschau* (auch als *Vorschauvorschau einsehen* bezeichnet) eines Fensters wird angezeigt, wenn ein Benutzer den Mauszeiger über die Miniaturansicht des Fensters in der Taskleiste bewegt oder den Miniaturansichtsfokus im ALT+TAB-Fenster erhält. Diese Ansicht ist eine Vorschau des Fensters in voller Größe und kann eine Livemomentaufnahme oder eine repräsentative Darstellung sein.

Desktopfenster-Manager (DWM) sendet diese Nachricht an ein Fenster, wenn alle der folgenden Situationen zutreffen:

-   Die Livevorschau wurde im Fenster aufgerufen.
-   Das [**\_ \_ BITMAP-Attribut \_ DWMWA HAS BITMAP**](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmwindowattribute) ist im Fenster festgelegt.
-   Eine Symboldarstellung ist die einzige darstellung, die für dieses Fenster vorhanden ist.

Das Fenster, das diese Nachricht empfängt, sollte durch Generieren einer vollständigen Bitmap reagieren. Das Fenster ruft dann die [**DwmSetIconicLivePreviewBitmap-Funktion**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap) auf, um die Livevorschau festzulegen. Wenn im Fenster in einem bestimmten Zeitraum keine Bitmap festgelegt wird, verwendet DWM eine eigene Standarddarstellung für das Fenster.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird eine Antwort auf die **WM \_ DWMSENDICONICLIVEPREVIEWBITMAP-Meldung** veranschaulicht. Das Beispiel ruft die [**DwmSetIconicLivePreviewBitmap-Funktion**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap) mit einem Handle für eine benutzerdefinierte, geräteunabhängige Bitmap auf, die als Darstellung des Fensters verwendet werden soll.


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



Den vollständigen Code finden Sie im [Beispiel Customize an Thumbnail Thumbnail and a Live Preview Bitmap (Anpassen einer miniaturisierten Miniaturansicht und einer Bitmap mit Livevorschau).](dwm-sample-customizethumbnail.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>Dwmapi.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**WM \_ DWMSENDICONICTHUMBNAIL**](wm-dwmsendiconicthumbnail.md)
</dt> <dt>

[**DwmInvalidateIconicBitmaps**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwminvalidateiconicbitmaps)
</dt> </dl>

 

 





