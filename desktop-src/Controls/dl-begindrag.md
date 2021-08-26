---
title: DL_BEGINDRAG Benachrichtigungscode (Commctrl.h)
description: Benachrichtigt das übergeordnete Fenster des Ziehlistenfelds, dass der Benutzer auf die linke Maustaste eines Elements geklickt hat. Ein Ziehlistenfeld sendet diesen Benachrichtigungscode in Form einer Ziehlistennachricht. Weitere Informationen finden Sie unter Drag List Box Messages.
ms.assetid: ccf66818-e5f7-4165-8d0d-4d279944f70e
keywords:
- DL_BEGINDRAG Benachrichtigungscode Windows Steuerelementen
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
ms.openlocfilehash: 5e2c843398b21ad51df51ae706a515c2e6f9831b89d32092b87148598b4bed5f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119968330"
---
# <a name="dl_begindrag-notification-code"></a>DL \_ BEGINDRAG-Benachrichtigungscode

Benachrichtigt das übergeordnete Fenster des Ziehlistenfelds, dass der Benutzer auf die linke Maustaste eines Elements geklickt hat. Ein Ziehlistenfeld sendet diesen Benachrichtigungscode in Form einer Ziehlistennachricht. Weitere Informationen finden Sie unter [Drag List Box Messages](about-list-boxes.md).


```C++
DL_BEGINDRAG

    pDragInfo = (LPARAM)(LPDRAGLISTINFO) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**DRAGLISTINFO-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo) die den DL BEGINDRAG-Benachrichtigungscode, das Handle zum Ziehlistenfeld und \_ die Cursorposition enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Geben **Sie TRUE zurück,** um den Ziehvorgang zu starten, oder **FALSE,** um den Ziehvorgang zu verhindern.

## <a name="remarks"></a>Hinweise

Bei der Verarbeitung dieses Benachrichtigungscodes bestimmt eine Fensterprozedur in der Regel das Listenelement an der angegebenen Cursorposition mithilfe der [**LBItemFromPt-Funktion.**](/windows/desktop/api/Commctrl/nf-commctrl-lbitemfrompt) Anschließend wird **TRUE oder** **FALSE zurückgegeben,** je nachdem, ob das Element gezogen werden soll. Vor der **Rückgabe von TRUE** sollte die Fensterprozedur den Index des Listenelements speichern, damit die Anwendung weiß, welches Element nach Abschluss des Ziehvorganges bewegt oder kopiert werden soll.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





