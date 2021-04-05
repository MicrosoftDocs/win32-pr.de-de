---
title: DL_DROPPED Benachrichtigungs Code (kommctrl. h)
description: Signalisiert, dass der Benutzer einen Zieh Vorgang durch Loslassen der linken Maustaste abgeschlossen hat. Ein Drag List Box-Element sendet diesen Benachrichtigungs Code in Form einer Drag List-Nachricht an das übergeordnete Fenster. Weitere Informationen finden Sie unter Drag List Box Messages.
ms.assetid: 81b9b424-2735-407d-bac9-f03ea2f48b4e
keywords:
- Windows-Steuerelemente für DL_DROPPED Benachrichtigungs
topic_type:
- apiref
api_name:
- DL_DROPPED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1b2480360ea38a00c4dd8efe6eb84eed8999890
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859356"
---
# <a name="dl_dropped-notification-code"></a>Benachrichtigungs Code für gelöschte DL \_

Signalisiert, dass der Benutzer einen Zieh Vorgang durch Loslassen der linken Maustaste abgeschlossen hat. Ein Drag List Box-Element sendet diesen Benachrichtigungs Code in Form einer Drag List-Nachricht an das übergeordnete Fenster. Weitere Informationen finden Sie unter [Drag List Box Messages](about-list-boxes.md).


```C++
DL_DROPPED

    pDragInfo = (LPARAM)(LPDRAGLISTINFO) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**draglistinfo**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo) -Struktur, die den gelöschten DL \_ -Benachrichtigungs Code, das Handle für das Zieh Listenfeld und die Cursorposition enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Dieser Benachrichtigungs Code wird normalerweise verarbeitet, indem das Element eingefügt wird, das vor dem Element unter dem Cursor in die Liste eingefügt wird. Um den Index des Elements an der Cursorposition abzurufen, verwenden Sie die [**lbitemfrompt**](/windows/desktop/api/Commctrl/nf-commctrl-lbitemfrompt) -Funktion. Beachten Sie, dass der \_ gesendete DL-Benachrichtigungs Code auch dann gesendet wird, wenn sich der Cursor nicht in einem Listenelement befindet. In diesem Fall gibt **lbitemfrompt** -1 zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





