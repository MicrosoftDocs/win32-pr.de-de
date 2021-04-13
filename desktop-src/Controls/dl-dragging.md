---
title: DL_DRAGGING Benachrichtigungs Code (kommctrl. h)
description: Signalisiert, dass der Benutzer beim Ziehen eines Elements die Maus bewegt hat.
ms.assetid: 87fc4c24-8e88-4e3c-8f54-ecc7f80de5d7
keywords:
- Windows-Steuerelemente für DL_DRAGGING Benachrichtigungs
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
ms.openlocfilehash: 0f5c9f3f6cec3ef95745eed88ec0208dff581ada
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519335"
---
# <a name="dl_dragging-notification-code"></a>DL- \_ Zieh Benachrichtigungs Code

Signalisiert, dass der Benutzer beim Ziehen eines Elements die Maus bewegt hat. \_Das Ziehen von DL wird auch in regelmäßigen Abständen beim Ziehen gesendet, auch wenn die Maus nicht bewegt wird. Ein Drag List Box-Element sendet diesen Benachrichtigungs Code in Form einer Drag List-Nachricht an das übergeordnete Fenster. Weitere Informationen finden Sie unter [Drag List Box Messages](about-list-boxes.md).


```C++
DL_DRAGGING

    pDragInfo = (LPARAM)(LPDRAGLISTINFO) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Steuerelement Bezeichner des Zieh Listen Felds.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**draglistinfo**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo) -Struktur, die den \_ Benachrichtigungs Code für die DL-Zieh Vorgänge, das Handle für das Zieh Listenfeld und die Cursorposition enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert bestimmt den Typ des Mauszeigers, der von der Zieh Liste festgelegt werden soll. Dabei kann es sich um den DL- \_ stopcursortyp, den DL- \_ copycursor-oder den DL- \_ Wert von "-" Wenn ein anderer Wert zurückgegeben wird, ändert sich der Cursor nicht.

## <a name="remarks"></a>Bemerkungen

Eine Fenster Prozedur verarbeitet in der Regel den \_ Benachrichtigungs Code für die DL-Zieh Vorgänge, indem Sie das Element unter dem Cursor bestimmt und dann ein Einfügesymbol Um das Element unter dem Cursor abzurufen, verwenden Sie die [**lbitemfrompt**](/windows/desktop/api/Commctrl/nf-commctrl-lbitemfrompt) -Funktion, und geben Sie **true** für den *bautescroll* -Parameter an. Diese Option bewirkt, dass das Zieh Listenfeld regelmäßig einen Bildlauf durchführen kann, wenn der Cursor oberhalb oder unterhalb des Client Bereichs liegt. Um das Einfügesymbol zu zeichnen, verwenden Sie die [**drawinsert**](/windows/desktop/api/Commctrl/nf-commctrl-drawinsert) -Funktion.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





