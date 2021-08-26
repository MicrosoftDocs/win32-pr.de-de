---
title: DL_DROPPED Benachrichtigungscode (Commctrl.h)
description: Signalisiert, dass der Benutzer einen Ziehvorgang abgeschlossen hat, indem die linke Maustaste losgelassen wird. Ein Ziehlistenfeld sendet diesen Benachrichtigungscode in Form einer Ziehlistenmeldung an das übergeordnete Fenster. Weitere Informationen finden Sie unter Drag List Box Messages.
ms.assetid: 81b9b424-2735-407d-bac9-f03ea2f48b4e
keywords:
- DL_DROPPED Benachrichtigungscode Windows-Steuerelemente
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
ms.openlocfilehash: 4c245cbb85a4e67845bd86a25b4cccb2f2aa0dc1d9d9613afd1d685037c5e1ef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002720"
---
# <a name="dl_dropped-notification-code"></a>DL \_ DROPPED-Benachrichtigungscode

Signalisiert, dass der Benutzer einen Ziehvorgang abgeschlossen hat, indem die linke Maustaste losgelassen wird. Ein Ziehlistenfeld sendet diesen Benachrichtigungscode in Form einer Ziehlistenmeldung an das übergeordnete Fenster. Weitere Informationen finden Sie unter [Drag List Box Messages](about-list-boxes.md).


```C++
DL_DROPPED

    pDragInfo = (LPARAM)(LPDRAGLISTINFO) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**DRAGLISTINFO-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo) die den DL \_ DROPPED-Benachrichtigungscode, das Handle für das Ziehlistenfeld und die Cursorposition enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Hinweise

Dieser Benachrichtigungscode wird normalerweise verarbeitet, indem das Element eingefügt wird, das in die Liste vor dem Element unter dem Cursor gezogen wird. Um den Index des Elements an der Cursorposition abzurufen, verwenden Sie die [**LBItemFromPt-Funktion.**](/windows/desktop/api/Commctrl/nf-commctrl-lbitemfrompt) Beachten Sie, dass der \_ DL DROPPED-Benachrichtigungscode auch dann gesendet wird, wenn sich der Cursor nicht in einem Listenelement befindet. In diesem Fall gibt **LBItemFromPt** -1 zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





