---
title: DL_DRAGGING Benachrichtigungscode (Commctrl.h)
description: Signalisiert, dass der Benutzer beim Ziehen eines Elements die Maus bewegt hat.
ms.assetid: 87fc4c24-8e88-4e3c-8f54-ecc7f80de5d7
keywords:
- DL_DRAGGING Benachrichtigungscode Windows Controls
topic_type:
- apiref
api_name:
- DL_DRAGGING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfe07cbf2cce3ad639af94055a2d1eab1f4fc3d6ce576c1c5467310809858843
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119878520"
---
# <a name="dl_dragging-notification-code"></a>DL \_ DRAGGING-Benachrichtigungscode

Signalisiert, dass der Benutzer beim Ziehen eines Elements die Maus bewegt hat. DL \_ DRAGING wird auch regelmäßig während des Ziehens gesendet, auch wenn die Maus nicht bewegt wird. Ein Ziehlistenfeld sendet diesen Benachrichtigungscode in Form einer Ziehlistenmeldung an das übergeordnete Fenster. Weitere Informationen finden Sie unter [Drag List Box Messages](about-list-boxes.md).


```C++
DL_DRAGGING

    pDragInfo = (LPARAM)(LPDRAGLISTINFO) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Steuerelementbezeichner des Ziehlistenfelds.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**DRAGLISTINFO-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo) die den DL \_ DRAGING-Benachrichtigungscode, das Handle für das Ziehlistenfeld und die Cursorposition enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert bestimmt den Typ des Mauszeigers, den die Ziehliste festlegen soll. dies kann der DL \_ STOPCURSOR-, DL \_ COPYCURSOR- oder DL \_ MOVECURSOR-Wert sein. Wenn ein anderer Wert zurückgegeben wird, ändert sich der Cursor nicht.

## <a name="remarks"></a>Hinweise

Eine Fensterprozedur verarbeitet in der Regel den DL \_ DRAGGING-Benachrichtigungscode, indem das Element unter dem Cursor bestimmt und dann ein Einfügesymbol gezeichnet wird. Um das Element unter dem Cursor abzurufen, verwenden Sie die [**LBItemFromPt-Funktion,**](/windows/desktop/api/Commctrl/nf-commctrl-lbitemfrompt) und geben Sie **TRUE** für den *bAutoScroll-Parameter* an. Diese Option bewirkt, dass das Ziehlistenfeld regelmäßig scrollt, wenn sich der Cursor über oder unter seinem Clientbereich befindet. Verwenden Sie zum Zeichnen des Einfügesymbols die [**DrawInsert-Funktion.**](/windows/desktop/api/Commctrl/nf-commctrl-drawinsert)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





