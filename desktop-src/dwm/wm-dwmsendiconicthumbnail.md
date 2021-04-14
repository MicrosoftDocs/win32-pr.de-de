---
title: WM_DWMSENDICONICTHUMBNAIL Meldung (dwmapi. h)
description: Weist ein Fenster an, ein statisches Bitmap bereitzustellen, das als Miniaturansicht dieses Fensters verwendet werden soll.
ms.assetid: 476c2542-f4d0-4777-93d3-bf50da26d94f
keywords:
- WM_DWMSENDICONICTHUMBNAIL Meldung Desktopfenster-Manager
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
ms.openlocfilehash: ded5b734278973afe35f5ed3d9fbb5b0aec9242b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478765"
---
# <a name="wm_dwmsendiconicthumbnail-message"></a>WM \_ dwmsendiimimanthumbnail-Meldung

Weist ein Fenster an, ein statisches Bitmap bereitzustellen, das als Miniaturansicht dieses Fensters verwendet werden soll.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Nicht verwendet.

</dd> <dt>

*lParam* 
</dt> <dd>

Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) dieses Werts ist die maximale x-Koordinate der Miniaturansicht. Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) ist die maximale y-Koordinate. Wenn eine Miniaturansicht eine Dimension aufweist, die einen oder beide dieser Werte überschreitet, akzeptiert die DWM die Miniaturansicht nicht.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.

## <a name="remarks"></a>Bemerkungen

DWM sendet diese Nachricht an ein Fenster, wenn alle der folgenden Situationen zutreffen:

-   DWM zeigt eine Darstellung des Fensters an.
-   Das [**dwmwa-Attribut \_ enthält ein \_ berühmtes \_ Bitmap**](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmwindowattribute) -Attribut, das im Fenster festgelegt ist.
-   Das Fenster hat keine zwischengespeicherte Bitmap festgelegt.
-   Es ist Platz im Cache für eine andere Bitmap vorhanden.

Das Fenster, das diese Nachricht empfängt, sollte Antworten, indem Sie eine Bitmap erzeugen, die nicht größer als die in den Nachrichten Parametern angeforderte Größe ist. Das Fenster ruft dann die Funktion " [**dwmsetticonfiguration**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticonicthumbnail) " auf, um die Standard Miniaturansicht zu überschreiben. Wenn das Fenster keine Bitmap in einem bestimmten Zeitraum bereitstellt, verwendet DWM eine eigene Standarddarstellung für das Fenster.

Das Fenster muss dem aufrufenden Prozess angehören.

## <a name="examples"></a>Beispiele

Im folgenden Codebeispiel wird gezeigt, wie auf die **WM- \_ dwmsendiimc-Meldung** reagiert wird. Im Beispiel wird [**dwmtarticonfiguration**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticonicthumbnail)mit einem Handle für eine angepasste, geräteunabhängige Bitmap aufgerufen, die als Windows-Darstellung verwendet werden soll.


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



Das komplette Beispiel finden Sie im Beispiel [Anpassen einer Miniaturansicht und Live Vorschau Bitmap](dwm-sample-customizethumbnail.md) .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>Dwmapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Dwminvalidateiconfiguration**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwminvalidateiconicbitmaps)
</dt> <dt>

[**WM \_ dwmsendiconiclivepreviewbitmap**](wm-dwmsendiconiclivepreviewbitmap.md)
</dt> </dl>

 

