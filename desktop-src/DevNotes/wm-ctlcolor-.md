---
description: Die "WM \_ CtlColor"-Meldung wird in 16-Bit-Versionen von Windows verwendet, um das Farbschema von Listenfeldern, die Listenfelder von Kombinations Feldern, Meldungs Feldern, Schaltflächen Steuerelementen, Bearbeitungs Steuerelemente, statische Steuerelemente und Dialogfelder zu ändern. Hinweis Informationen zu dieser Nachricht und 32-Bit-Versionen von Windows finden Sie unter "Hinweise".
ms.assetid: e654cf48-550f-4210-9952-20470b9a397a
title: WM_CTLCOLOR Meldung (WINDOWSX. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8166979c17b7d2eef50af062e5df13712e9d32ae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370131"
---
# <a name="wm_ctlcolor-message"></a>WM- \_ CtlColor-Meldung

Die " **WM \_ CtlColor** "-Meldung wird in 16-Bit-Versionen von Windows verwendet, um das Farbschema von Listenfeldern, die Listenfelder von Kombinations Feldern, Meldungs Feldern, Schaltflächen Steuerelementen, Bearbeitungs Steuerelemente, statische Steuerelemente und Dialogfelder zu ändern.

> [!Note]  
> Informationen im Zusammenhang mit dieser Nachricht und 32-Bit-Versionen von Windows finden Sie unter "Hinweise".

 


```C++
  WM_CTLCOLOR

  WPARAM wParam;
  LPARAM lParam;
    
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*HWND* 
</dt> <dd>

Ein Handle für das Zielfenster.

</dd> <dt>

*wParam* 
</dt> <dd>

Ein Handle für einen Anzeige Kontext (DC).

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Handle für ein untergeordnetes Fenster (-Steuerelement).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn eine Anwendung diese Nachricht verarbeitet, wird ein Handle für einen Pinsel zurückgegeben. Das System verwendet den Pinsel, um den Hintergrund des Steuer Elements zu zeichnen.

## <a name="remarks"></a>Bemerkungen

Die **WM \_ CtlColor** -Meldung von 16-Bit-Fenstern wurde durch spezifischere Benachrichtigungen ersetzt. Diese Ersetzungen umfassen Folgendes:

-   [**WM \_ ctlcolorbtn**](../controls/wm-ctlcolorbtn.md)
-   [**WM \_ ctlcoloredit**](../controls/wm-ctlcoloredit.md)
-   [**WM \_ ctlcolordlg**](../dlgbox/wm-ctlcolordlg.md)
-   [**WM \_ ctlcolorlistbox**](../controls/wm-ctlcolorlistbox.md)
-   [**WM \_ ctlcolorscrollbar**](../controls/wm-ctlcolorscrollbar.md)
-   [**WM \_ ctlcolorstatic**](../controls/wm-ctlcolorstatic.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>WINDOWSX. h</dt> </dl> |



 

 
