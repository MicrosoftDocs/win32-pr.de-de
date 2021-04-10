---
title: HDM_GETORDERARRAY Meldung (kommstrg. h)
description: Ruft die aktuelle Reihenfolge der Elemente in einem Header Steuerelement von links nach rechts ab. Sie können diese Nachricht explizit senden oder das gesenderarray-Header-Header verwenden \_ .
ms.assetid: b287d3c1-ae61-41a4-a884-dc008eb24ad8
keywords:
- Windows-Steuerelemente für HDM_GETORDERARRAY Meldung
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
ms.openlocfilehash: e334b0023ad3441c20048273e9bc58c1b25622b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103772"
---
# <a name="hdm_getorderarray-message"></a>HDM \_ getor Array-Meldung

Ruft die aktuelle Reihenfolge der Elemente in einem Header Steuerelement von links nach rechts ab. Sie können diese Nachricht explizit senden oder das [**\_ gesenderarray-Header-Header**](/windows/desktop/api/Commctrl/nf-commctrl-header_getorderarray) verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Die Anzahl der ganzzahligen Elemente, die *LPARAM* enthalten kann. Dieser Wert muss gleich der Anzahl der Elemente im-Steuerelement sein (siehe [**HDM \_ GetItemCount**](hdm-getitemcount.md)).

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf ein Array von ganzen Zahlen, die die Indexwerte für Elemente in der Kopfzeile empfangen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg einen Wert ungleich 0 (null) zurück, und der Puffer bei *LPARAM* empfängt die Element Nummer für jedes Element im Header-Steuerelement in der Reihenfolge, in der Sie von links nach rechts angezeigt werden. Andernfalls gibt die Meldung 0 (null) zurück.

## <a name="remarks"></a>Bemerkungen

Die Anzahl der Elemente in *LPARAM* wird in *wParam* angegeben und muss gleich der Anzahl der Elemente im Steuerelement sein. Im folgenden Code Fragment wird z. b. genügend Arbeitsspeicher für die Indexwerte reserviert.


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
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





