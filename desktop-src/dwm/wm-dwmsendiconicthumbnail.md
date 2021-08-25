---
title: WM_DWMSENDICONICTHUMBNAIL Nachricht (Dwmapi.h)
description: Weist ein Fenster an, eine statische Bitmap bereitzustellen, die als Miniaturansichtsdarstellung dieses Fensters verwendet werden soll.
ms.assetid: 476c2542-f4d0-4777-93d3-bf50da26d94f
keywords:
- WM_DWMSENDICONICTHUMBNAIL Desktopfenster-Manager
topic_type:
- apiref
api_name:
- WM_DWMSENDICONICTHUMBNAIL
api_location:
- Dwmapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3263f34cd59ba68ee895e5d5c77e297144cbadd6c8d8bbaa49ca6272248c2024
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119842650"
---
# <a name="wm_dwmsendiconicthumbnail-message"></a>WM \_ DWMSENDICONICTHUMBNAIL-Nachricht

Weist ein Fenster an, eine statische Bitmap bereitzustellen, die als Miniaturansichtsdarstellung dieses Fensters verwendet werden soll.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Wird nicht verwendet.

</dd> <dt>

*lParam* 
</dt> <dd>

[**HiWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) dieses Werts ist die maximale x-Koordinate der Miniaturansicht. [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) ist die maximale y-Koordinate. Wenn eine Miniaturansicht eine Dimension aufweist, die einen oder beide dieser Werte überschreitet, akzeptiert dwm die Miniaturansicht nicht.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn eine Anwendung diese Nachricht verarbeitet, sollte sie 0 (null) zurückgeben.

## <a name="remarks"></a>Hinweise

DWM sendet diese Nachricht an ein Fenster, wenn alle der folgenden Situationen zutreffen:

-   DWM zeigt eine repräsentative Darstellung des Fensters an.
-   Das [**\_ \_ BITMAP-Attribut \_ DWMWA HAS BITMAP**](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmwindowattribute) ist im Fenster festgelegt.
-   Im Fenster wurde keine zwischengespeicherte Bitmap festgelegt.
-   Im Cache ist Platz für eine andere Bitmap.

Das Fenster, das diese Nachricht empfängt, sollte reagieren, indem eine Bitmap generiert wird, die nicht größer als die in den Nachrichtenparametern angeforderte Größe ist. Das Fenster ruft dann die [**DwmSetIconicThumbnail-Funktion**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticonicthumbnail) auf, um die Standardminiaturansicht zu überschreiben. Wenn das Fenster in einem bestimmten Zeitraum keine Bitmap liefert, verwendet DWM eine eigene Standarddarstellung für das Fenster.

Das Fenster muss zum aufrufenden Prozess gehören.

## <a name="examples"></a>Beispiele

Das folgende Codebeispiel zeigt, wie sie auf die **WM-Nachricht \_ DWMSENDICONICTHUMBNAIL** reagieren. Im Beispiel wird [**DwmSetIconicThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticonicthumbnail)mit einem Handle für eine benutzerdefinierte, geräteunabhängige Bitmap zur Verwendung als Darstellung des Fensters verwendet.


```C++
        case WM_DWMSENDICONICTHUMBNAIL:
        {    
            // This window is being asked to provide its iconic bitmap. This indicates
            // a thumbnail is being drawn.
            hbm = CreateDIB(HIWORD(lParam), LOWORD(lParam)); 
            if (hbm)
            {
                hr = DwmSetIconicThumbnail(hwnd, hbm, 0);
                DeleteObject(hbm);
            }
        }
        break;
```



Das vollständige Beispiel finden Sie im Beispiel [Customize an Thumbnail Thumbnail and a Live Preview Bitmap (Anpassen einer miniaturisierten Miniaturansicht und einer Livevorschaubitmap).](dwm-sample-customizethumbnail.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>Dwmapi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**DwmInvalidateIconicBitmaps**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwminvalidateiconicbitmaps)
</dt> <dt>

[**WM \_ DWMSENDICONICLIVEPREVIEWBITMAP**](wm-dwmsendiconiclivepreviewbitmap.md)
</dt> </dl>

 

