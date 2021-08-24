---
title: TTM_ADJUSTRECT-Nachricht (Commctrl.h)
description: Berechnet das Textanzeigerechteck eines QuickInfo-Steuerelements aus seinem Fensterrechteck oder das QuickInfo-Fensterrechteck, das zum Anzeigen eines angegebenen Textanzeigerechtecks benötigt wird.
ms.assetid: b848c16f-9f41-4ed2-918a-9c03aebe535c
keywords:
- TTM_ADJUSTRECT Windows-Steuerelemente für Nachrichten
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
ms.openlocfilehash: bba5a6719bcbd820d94b6d736a12644f8b2539cc81064f942616c62bce55823f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119769530"
---
# <a name="ttm_adjustrect-message"></a>TTM \_ ADJUSTRECT-Nachricht

Berechnet das Textanzeigerechteck eines QuickInfo-Steuerelements aus seinem Fensterrechteck oder das QuickInfo-Fensterrechteck, das zum Anzeigen eines angegebenen Textanzeigerechtecks benötigt wird.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Wert, der angibt, welcher Vorgang ausgeführt werden soll. True gibt an, dass *lParam* zum Angeben eines Textanzeigerechtecks verwendet wird und das entsprechende Fensterrechteck empfängt. **False** gibt an, dass *lParam* zum Angeben eines Fensterrechtecks verwendet wird und das entsprechende Textanzeigerechteck empfängt.

</dd> <dt>

*lParam* 
</dt> <dd>

**RECT-Struktur** zum Speichern eines QuickInfo-Fensterrechtecks oder eines Rechtecks für die Textanzeige.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen Wert ungleich 0 (null) zurück, wenn das Rechteck erfolgreich angepasst wurde, und gibt 0 (null) zurück, wenn ein Fehler auftritt.

## <a name="remarks"></a>Hinweise

Diese Meldung ist besonders nützlich, wenn Sie ein QuickInfo-Steuerelement verwenden möchten, um den Volltext einer Zeichenfolge anzuzeigen, die normalerweise abgeschnitten wird. Es wird häufig mit ListView- und Treeview-Steuerelementen verwendet. In der Regel senden Sie diese Nachricht als Reaktion auf einen [TTN \_ SHOW-Benachrichtigungscode,](ttn-show.md) damit Sie das QuickInfo-Steuerelement ordnungsgemäß positionieren können.

Das QuickInfo-Fensterrechteck ist etwas größer als das Textanzeigerechteck, das die QuickInfo-Zeichenfolge umgrenzt. Der Fensterursprung wird auch nach oben und links vom Ursprung des Rechtecks für die Textanzeige versetzt. Um das Textanzeigerechteck zu positionieren, müssen Sie das entsprechende Fensterrechteck berechnen und dieses Rechteck verwenden, um die QuickInfo zu positionieren. **TTM \_ ADJUSTRECT** übernimmt diese Berechnung für Sie.

Wenn Sie *wParam* auf **TRUE** festlegen, übernimmt **TTM \_ ADJUSTRECT** die Größe und Position des gewünschten QuickInfo-Textanzeigerechtecks und übergibt die Größe und Position des QuickInfo-Fensters zurück, das zum Anzeigen des Texts an der angegebenen Position erforderlich ist. Wenn Sie *wParam* auf **FALSE** festlegen, können Sie ein QuickInfo-Fensterrechteck angeben, und **TTM \_ ADJUSTRECT** gibt die Größe und Position des Textrechtecks zurück.

Das folgende Codefragment veranschaulicht die Verwendung der **TTM \_ ADJUSTRECT-Nachricht** zum Positionieren eines QuickInfo-Steuerelements, um den Volltext der Zeichenfolge eines Steuerelements anstelle einer abgeschnittenen Zeichenfolge anzuzeigen. Die anwendungsdefinierte **GetMyItemRect-Funktion** gibt das Textrechteck zurück, das benötigt wird, um den QuickInfo-Text direkt über der abgeschnittenen Zeichenfolge anzuzeigen. Die Details zur Implementierung dieser Funktion hängen vom jeweiligen Steuerelement ab. **TTM \_ ADJUSTRECT** wird verwendet, um dieses Textrechteck an das QuickInfo-Steuerelement zu senden. Sie gibt ein entsprechend dimensioniertes und positioniertes Fensterrechteck zurück, das dann zum Positionieren des QuickInfo-Fensters verwendet wird.


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
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





