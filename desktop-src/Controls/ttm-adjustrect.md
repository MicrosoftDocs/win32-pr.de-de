---
title: TTM_ADJUSTRECT Meldung (kommstrg. h)
description: Berechnet das Textanzeige Rechteck eines QuickInfo-Steuer Elements aus dem Fenster Rechteck oder das QuickInfo-Fenster Rechteck, das zum Anzeigen eines angegebenen Textanzeige Rechtecks erforderlich ist.
ms.assetid: b848c16f-9f41-4ed2-918a-9c03aebe535c
keywords:
- Windows-Steuerelemente für TTM_ADJUSTRECT Meldung
topic_type:
- apiref
api_name:
- TTM_ADJUSTRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af89374161d5e3f9d9ab6affc2b3b498a39cbf68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956492"
---
# <a name="ttm_adjustrect-message"></a>TTM- \_ Nachricht

Berechnet das Textanzeige Rechteck eines QuickInfo-Steuer Elements aus dem Fenster Rechteck oder das QuickInfo-Fenster Rechteck, das zum Anzeigen eines angegebenen Textanzeige Rechtecks erforderlich ist.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Wert, der angibt, welcher Vorgang durchgeführt werden soll. **True** gibt an, dass *LPARAM* zum Angeben eines Textanzeige Rechtecks verwendet wird und das entsprechende Fenster Rechteck empfängt. Wenn **false**, wird *LPARAM* zum Angeben eines Fenster Rechtecks verwendet, und das entsprechende Textanzeige Rechteck wird empfangen.

</dd> <dt>

*lParam* 
</dt> <dd>

**Rect** -Struktur, um entweder ein QuickInfo-Fenster Rechteck oder ein Textanzeige Rechteck zu halten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen Wert ungleich 0 (null) zurück, wenn das Rechteck erfolgreich angepasst wurde, und gibt NULL zurück, wenn ein Fehler auftritt.

## <a name="remarks"></a>Bemerkungen

Diese Meldung ist besonders nützlich, wenn Sie ein QuickInfo-Steuerelement verwenden möchten, um den vollständigen Text einer Zeichenfolge anzuzeigen, die in der Regel abgeschnitten wird. Sie wird häufig mit ListView-und TreeView-Steuerelementen verwendet. Normalerweise senden Sie diese Nachricht als Antwort auf einen TTN-Benachrichtigungs Code [ \_ anzeigen](ttn-show.md) , damit Sie das QuickInfo-Steuerelement ordnungsgemäß positionieren können.

Das QuickInfo-Fenster Rechteck ist etwas größer als das Textanzeige Rechteck, das die QuickInfo-Zeichenfolge umschließt. Der Fenster Ursprung wird auch nach links vom Ursprung des Textanzeige Rechtecks verschoben. Zum Positionieren des Textanzeige Rechtecks müssen Sie das entsprechende Fenster Rechteck berechnen und dieses Rechteck verwenden, um die QuickInfo zu positionieren. **TTM \_** "Anpassungen" verarbeitet diese Berechnung für Sie.

Wenn Sie " *wParam* " auf " **true**" festlegen, nimmt die Größe und Position des gewünschten QuickInfo-Textanzeige Rechtecks an, und die Größe und Position des QuickInfo-Fensters wird zurück **gegeben, um \_** den Text an der angegebenen Position anzuzeigen. Wenn Sie " *wParam* " auf " **false**" festlegen, können Sie ein QuickInfo-Fenster Rechteck angeben, und die Größe und Position des Text Rechtecks werden von **TTM \_** "-Wert-",

Das folgende Code Fragment veranschaulicht die Verwendung der **TTM- \_** Nachricht, um ein QuickInfo-Steuerelement zu positionieren, um den vollständigen Text der Zeichenfolge eines Steuer Elements anstelle einer abgeschnittene Zeichenfolge anzuzeigen. Die von der Anwendung definierte **getmyitemrect** -Funktion gibt das Text Rechteck zurück, das benötigt wird, um den QuickInfo-Text direkt über die abgeschnittene Zeichenfolge anzuzeigen. Die Details, wie diese Funktion implementiert wird, hängen vom jeweiligen Steuerelement ab. **TTM \_** Mithilfe von "" wird "" "" "" Er gibt ein entsprechend großes und positioniertes Fenster Rechteck zurück, das dann verwendet wird, um das QuickInfo-Fenster zu positionieren.


```
case TTN_SHOW:

if (MyStringIsTruncated) {
    RECT rc;
    
    GetMyItemRect(&rc);
    SendMessage(hwndToolTip, TTM_ADJUSTRECT, TRUE, (LPARAM)&rc);
    SetWindowPos(hwndToolTip,
                 NULL,
                 rc.left, rc.top,
                 0, 0,
                 SWP_NOSIZE|SWP_NOZORDER|SWP_NOACTIVATE);
} 
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





