---
title: WM_DPICHANGED Meldung (Winuser. h)
description: Wird gesendet, wenn sich der dpi-Code (Effective dots per inch) für ein Fenster geändert hat.
ms.assetid: 97C458F2-89CD-45FF-ABEE-F158A3BCE0B8
keywords:
- WM_DPICHANGED Message High dpi
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
ms.openlocfilehash: aafbce1e784e1f205f0d32e045785125c1fb5aaa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741833"
---
# <a name="wm_dpichanged-message"></a>\_Dpichanged-Meldung für WM

Wird gesendet, wenn sich der dpi-Code (Effective dots per inch) für ein Fenster geändert hat. Der dpi-Wert ist der Skalierungsfaktor für ein Fenster. Es gibt mehrere Ereignisse, die bewirken können, dass sich der dpi-Wert ändert. In der folgenden Liste sind die möglichen Ursachen für die Änderung in dpi angegeben.

-   Das Fenster wird in einen neuen Monitor mit einem anderen dpi-Wert verschoben.
-   Der dpi-Code des Monitors, der das Fenster gehostet, ändert sich.

Der aktuelle dpi-Code für ein Fenster gleicht immer dem letzten von **WM \_ dpichanged** gesendeten dpi. Dies ist der Skalierungsfaktor, auf den das Fenster für Threads skaliert werden soll, die von dpi-Änderungen abhängig sind.


```C++
#define WM_DPICHANGED       0x02E0
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) des *wParam* enthält den Y-Achsen-Wert des neuen dpi-Werts des Fensters. Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) des *wParam* enthält den Wert der X-Achse des neuen dpi-Werts des Fensters. Beispiel: 96, 120, 144 oder 192. Die Werte der X-Achse und der Y-Achse sind bei Windows-apps identisch.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**Rect**](/windows/desktop/api/windef/ns-windef-rect) -Struktur, die eine vorgeschlagene Größe und Position des aktuellen Fensters bereitstellt, das für den neuen dpi-Wert skaliert wird. Es wird erwartet, dass sich die apps auf der Grundlage der von *LPARAM* bereitgestellten Vorschläge bei der Verarbeitung dieser Nachricht neu positionieren und die Größe der Fenstergröße ändern.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.

## <a name="remarks"></a>Bemerkungen

Diese Meldung ist nur für Prozesse relevant, die **\_ \_ \_ dpi \_** -abhängige Anwendungen oder dpi-Informationen **\_ \_ pro \_ Monitor \_ erkennen** . Sie kann auf bestimmten dpi-Änderungen empfangen werden, wenn das Fenster oder der Prozess der obersten Ebene als **dpi** -Wert oder **System-dpi**-fähig ausgeführt wird. in diesen Fällen kann es jedoch problemlos ignoriert werden. Weitere Informationen zu den unterschiedlichen Arten von Informationen finden Sie unter [**Process \_ dpi \_ Awareness**](/windows/desktop/api/ShellScalingApi/ne-shellscalingapi-process_dpi_awareness) and [**dpi \_ Awareness**](/windows/desktop/api/windef/ne-windef-dpi_awareness). Ältere Versionen von Windows erforderten die dpi-Informationen, die auf der Ebene einer Anwendung gebunden werden mussten. Diese Apps verwenden **Prozess \_ - \_ dpi**-Informationen. Derzeit ist das dpi-Bewusstsein an Threads und einzelne Fenster gebunden, nicht an die gesamte Anwendung. Diese Apps verwenden **dpi \_**-Informationen.

Beim Skalieren der Anwendung müssen Sie nur den Wert der X-Achse oder der Y-Achse verwenden, da diese identisch sind.

Damit diese Nachricht ordnungsgemäß verarbeitet wird, müssen Sie die Größe des Fensters auf der Grundlage der von *LPARAM* bereitgestellten Vorschläge und der Verwendung von [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos)ändern. Wenn Sie dies nicht tun, vergrößert oder verkleinert sich das Fenster in Bezug auf alles andere auf dem neuen Monitor. Wenn ein Benutzer z. b. mehrere Monitore verwendet und das Fenster von einem 96-dpi-Monitor auf einen 192 dpi-Monitor zieht, wird das Fenster in Bezug auf andere Elemente im 192-dpi-Monitor in der Hälfte der Größe angezeigt.

Der Basiswert von dpi ist als **Benutzer \_ \_ Standardbildschirm \_ dpi** definiert, der auf 96 festgelegt ist. Um den Skalierungsfaktor für einen Monitor zu ermitteln, nehmen Sie den dpi-Wert an, und teilen Sie die **\_ Standard \_ Bildschirm \_ dpi des Benutzers**. In der folgenden Tabelle finden Sie einige Beispiel-dpi-Werte und zugeordnete Skalierungsfaktoren.



| DPI-Wert | Skalierung in Prozent |
|-----------|--------------------|
| 96        | 100 %               |
| 120       | 125%               |
| 144       | 150%               |
| 192       | 200 %               |



 

Im folgenden Beispiel wird ein Beispiel für einen dpi-Änderungs Handler bereitstellt.


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



Mit dem folgenden Code wird ein Wert von 100% (96 dpi) Linear auf einen beliebigen dpi-Wert skaliert, der durch *g \_ dpi* definiert ist.


```C++
    INT iBorderWidth100 = 5;
    iBorderWidth = MulDiv(iBorderWidth100, g_dpi, USER_DEFAULT_SCREEN_DPI);
```



Eine alternative Möglichkeit zum Skalieren eines Werts besteht darin, den dpi-Wert in einen Skalierungsfaktor zu konvertieren und diesen zu verwenden.


```C++
    INT iBorderWidth100 = 5;
    FLOAT fscale = (float) g_dpi / USER_DEFAULT_SCREEN_DPI;
    iBorderWidth = iBorderWidth100 * fscale;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Nur Desktop-Apps Windows 8.1\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 R2 \[ -Desktop-Apps\]<br/>                              |
| Header<br/>                   | <dl> <dt>Winuser. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**DPI \_ -Informationen**](/windows/desktop/api/windef/ne-windef-dpi_awareness)
</dt> <dt>

[**Prozess- \_ dpi- \_ Bewusstsein**](/windows/desktop/api/ShellScalingApi/ne-shellscalingapi-process_dpi_awareness)
</dt> </dl>

 

