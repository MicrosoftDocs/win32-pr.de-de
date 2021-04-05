---
title: DL_BEGINDRAG Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster des Zieh Listen Felds, dass der Benutzer mit der linken Maustaste auf ein Element geklickt hat. Ein Drag-Listenfeld sendet diesen Benachrichtigungs Code in Form einer Drag List-Nachricht. Weitere Informationen finden Sie unter Drag List Box Messages.
ms.assetid: ccf66818-e5f7-4165-8d0d-4d279944f70e
keywords:
- Windows-Steuerelemente für DL_BEGINDRAG Benachrichtigungs
topic_type:
- apiref
api_name:
- DL_BEGINDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f2d3ee211641c5b5e02482f914145fdf2e119f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859355"
---
# <a name="dl_begindrag-notification-code"></a>DL \_ BeginDrag-Benachrichtigungs Code

Benachrichtigt das übergeordnete Fenster des Zieh Listen Felds, dass der Benutzer mit der linken Maustaste auf ein Element geklickt hat. Ein Drag-Listenfeld sendet diesen Benachrichtigungs Code in Form einer Drag List-Nachricht. Weitere Informationen finden Sie unter [Drag List Box Messages](about-list-boxes.md).


```C++
DL_BEGINDRAG

    pDragInfo = (LPARAM)(LPDRAGLISTINFO) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**draglistinfo**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo) -Struktur, die den DL \_ BeginDrag-Benachrichtigungs Code, das Handle für das Zieh Listenfeld und die Cursorposition enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, um den Zieh Vorgang zu starten, oder **false** , um den Zieh Vorgang zu verhindern.

## <a name="remarks"></a>Bemerkungen

Bei der Verarbeitung dieses Benachrichtigungs Codes bestimmt eine Fenster Prozedur in der Regel das Listenelement an der angegebenen Cursorposition mithilfe der [**lbitemfrompt**](/windows/desktop/api/Commctrl/nf-commctrl-lbitemfrompt) -Funktion. Anschließend wird " **true** " oder " **false**" zurückgegeben, je nachdem, ob das Element gezogen werden soll. Vor der Rückgabe von **true** sollte die Fenster Prozedur den Index des Listen Elements speichern, damit die Anwendung weiß, welches Element verschoben oder kopiert werden soll, wenn der Zieh Vorgang abgeschlossen ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





