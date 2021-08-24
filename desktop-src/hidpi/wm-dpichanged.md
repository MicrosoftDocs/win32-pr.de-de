---
title: WM_DPICHANGED (WinUser.h)
description: Wird gesendet, wenn sich die effektiven Punkte pro Zoll (dpi) für ein Fenster geändert haben.
ms.assetid: 97C458F2-89CD-45FF-ABEE-F158A3BCE0B8
keywords:
- WM_DPICHANGED meldung High DPI
topic_type:
- apiref
api_name:
- WM_DPICHANGED
api_location:
- WinUser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d77a7d7608e9facc1e0fc6973b19a3d9db36900fa8d550896cc3058389f367bc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119666380"
---
# <a name="wm_dpichanged-message"></a>WM \_ DPICHANGED-Nachricht

Wird gesendet, wenn sich die effektiven Punkte pro Zoll (dpi) für ein Fenster geändert haben. Der DPI ist der Skalierungsfaktor für ein Fenster. Es gibt mehrere Ereignisse, die dazu führen können, dass sich der DPI ändert. Die folgende Liste gibt die möglichen Ursachen für die Änderung des DPI an.

-   Das Fenster wird auf einen neuen Monitor mit einem anderen DPI verschoben.
-   Die DPI des Monitors, der das Fenster hosten soll, ändert sich.

Der aktuelle DPI für ein Fenster entspricht immer dem letzten DPI, der von **WM \_ DPICHANGED gesendet wurde.** Dies ist der Skalierungsfaktor, auf den das Fenster für Threads skaliert werden soll, die DPI-Änderungen kennen.


```C++
#define WM_DPICHANGED       0x02E0
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) des *wParam-Werts* enthält den Wert der Y-Achse des neuen dpi-Werts des Fensters. Das [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) des *wParam-Werts* enthält den X-Achsenwert des neuen DPI des Fensters. Beispiel: 96, 120, 144 oder 192. Die Werte der X-Achse und der Y-Achse sind für Windows identisch.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**RECT-Struktur,**](/windows/desktop/api/windef/ns-windef-rect) der eine vorgeschlagene Größe und Position des aktuellen Fensters bietet, das für den neuen DPI skaliert wird. Es wird erwartet, dass Apps Fenster basierend auf den Vorschlägen von *lParam* neu positionieren und ihre Größe ändern, wenn sie diese Nachricht behandeln.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn eine Anwendung diese Nachricht verarbeitet, sollte sie 0 (null) zurückgeben.

## <a name="remarks"></a>Hinweise

Diese Meldung ist nur für **PROCESS \_ PER MONITOR \_ \_ DPI \_ AWARE-Anwendungen** oder **DPI AWARENESS PER \_ MONITOR \_ \_ \_ AWARE-Threads** relevant. Sie kann bei bestimmten DPI-Änderungen empfangen werden, wenn Das Fenster oder der Prozess der obersten Ebene als **DPI-nicht** bekannt oder **system-DPI-bewusst** ausgeführt wird, aber in diesen Situationen kann er sicher ignoriert werden. Weitere Informationen zu den verschiedenen Arten von Bewusstsein finden Sie unter [**PROCESS \_ DPI \_ AWARENESS**](/windows/desktop/api/ShellScalingApi/ne-shellscalingapi-process_dpi_awareness) und [**DPI \_ AWARENESS**](/windows/desktop/api/windef/ne-windef-dpi_awareness). Ältere Versionen von Windows DPI-Kenntnis erforderlich, um an die Ebene einer Anwendung gebunden zu sein. Diese Apps verwenden **PROCESS \_ DPI \_ AWARENESS**. Derzeit ist das DPI-Bewusstsein nicht an die gesamte Anwendung, sondern an Threads und einzelne Fenster gebunden. Diese Apps verwenden **DPI \_ AWARENESS**.

Sie müssen beim Skalieren Ihrer Anwendung nur die X-Achse oder den Wert der Y-Achse verwenden, da sie identisch sind.

Um diese Nachricht ordnungsgemäß zu behandeln, müssen Sie die Größe Ihres Fensters basierend auf den Vorschlägen von *lParam* und mithilfe von [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos)ändern und neu positionieren. Wenn Sie dies nicht tun, wird Ihr Fenster in Bezug auf alle anderen Funktionen des neuen Monitors verkleinert oder verkleinert. Wenn ein Benutzer beispielsweise mehrere Monitore verwendet und Ihr Fenster von einem 96-DPI-Monitor auf einen Monitor mit 192 DPI zieht, scheint ihr Fenster im Hinblick auf andere Elemente des 192-DPI-Monitors halb so groß zu sein.

Der Basiswert von DPI ist als **USER \_ DEFAULT SCREEN \_ \_ DPI** definiert, der auf 96 festgelegt ist. Um den Skalierungsfaktor für einen Monitor zu bestimmen, verwenden Sie den DPI-Wert, und dividieren Sie durch **USER \_ DEFAULT SCREEN \_ \_ DPI**. Die folgende Tabelle enthält einige DPI-Beispielwerte und zugehörige Skalierungsfaktoren.



| DPI-Wert | Skalierungsprozentsatz |
|-----------|--------------------|
| 96        | 100%               |
| 120       | 125%               |
| 144       | 150%               |
| 192       | 200 %               |



 

Das folgende Beispiel enthält einen Beispiel-DPI-Änderungshandler.


```C++
    case WM_DPICHANGED:
    {
        g_dpi = HIWORD(wParam);
        UpdateDpiDependentFontsAndResources();

        RECT* const prcNewWindow = (RECT*)lParam;
        SetWindowPos(hWnd,
            NULL,
            prcNewWindow ->left,
            prcNewWindow ->top,
            prcNewWindow->right - prcNewWindow->left,
            prcNewWindow->bottom - prcNewWindow->top,
            SWP_NOZORDER | SWP_NOACTIVATE);
        break;
    }
```



Der folgende Code skaliert einen Wert linear von 100 % (96 DPI) auf einen beliebigen DPI-Wert, der durch *g \_ dpi definiert wird.*


```C++
    INT iBorderWidth100 = 5;
    iBorderWidth = MulDiv(iBorderWidth100, g_dpi, USER_DEFAULT_SCREEN_DPI);
```



Eine alternative Möglichkeit zum Skalieren eines Werts besteht in der Konvertierung des DPI-Werts in einen Skalierungsfaktor und deren Verwendung.


```C++
    INT iBorderWidth100 = 5;
    FLOAT fscale = (float) g_dpi / USER_DEFAULT_SCREEN_DPI;
    iBorderWidth = iBorderWidth100 * fscale;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8.1 Nur Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 Nur \[ R2-Desktop-Apps\]<br/>                              |
| Header<br/>                   | <dl> <dt>WinUser.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**DPI \_ AWARENESS**](/windows/desktop/api/windef/ne-windef-dpi_awareness)
</dt> <dt>

[**\_PROZESS-DPI-BEWUSSTSEIN \_**](/windows/desktop/api/ShellScalingApi/ne-shellscalingapi-process_dpi_awareness)
</dt> </dl>

 

