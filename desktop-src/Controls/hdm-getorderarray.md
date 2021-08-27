---
title: HDM_GETORDERARRAY (Commctrl.h)
description: Ruft die aktuelle Reihenfolge von links nach rechts von Elementen in einem Headersteuerelementen ab. Sie können diese Nachricht explizit senden oder das \_ Header-GetOrderArray-Makro verwenden.
ms.assetid: b287d3c1-ae61-41a4-a884-dc008eb24ad8
keywords:
- HDM_GETORDERARRAY von Windows-Steuerelementen
topic_type:
- apiref
api_name:
- HDM_GETORDERARRAY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f374424fe3f1d84c4919c26948486a9bae1660072975556aecaac4b08b85b33b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062830"
---
# <a name="hdm_getorderarray-message"></a>HDM \_ GETORDERARRAY-Nachricht

Ruft die aktuelle Reihenfolge von links nach rechts von Elementen in einem Headersteuerelementen ab. Sie können diese Nachricht explizit senden oder das [**\_ Header-GetOrderArray-Makro**](/windows/desktop/api/Commctrl/nf-commctrl-header_getorderarray) verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Die Anzahl der ganzzahligen Elemente, die *lParam* enthalten kann. Dieser Wert muss gleich der Anzahl der Elemente im Steuerelement sein (siehe [**HDM \_ GETITEMCOUNT**](hdm-getitemcount.md)).

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf ein Array von ganzen Zahlen, die die Indexwerte für Elemente im Header empfangen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg einen Wert ungleich 0 (null) zurück, und der Puffer bei *lParam* empfängt die Elementnummer für jedes Element im Headersteuerelement in der Reihenfolge, in der sie von links nach rechts angezeigt werden. Andernfalls gibt die Meldung 0 (null) zurück.

## <a name="remarks"></a>Hinweise

Die Anzahl der Elemente in *lParam* wird in *wParam* angegeben und muss der Anzahl der Elemente im -Steuerelement entspricht. Das folgende Codefragment reservieren beispielsweise genügend Arbeitsspeicher, um die Indexwerte zu enthalten.


```
int iItems,

    *lpiArray;



// Get memory for buffer.

(iItems = SendMessage(hwndHD, HDM_GETITEMCOUNT, 0,0))!=-1)

    if(!(lpiArray = calloc(iItems,sizeof(int))))

MessageBox(hwnd, "Out of memory.","Error", MB_OK);
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





