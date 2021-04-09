---
title: DL_CANCELDRAG Benachrichtigungs Code (kommctrl. h)
description: Signalisiert, dass der Benutzer einen Zieh Vorgang abgebrochen hat, indem er auf die Rechte Maustaste klickt oder die ESC-Taste gedrückt hat.
ms.assetid: 62c1377f-41b6-449f-a95e-2689dc1913c6
keywords:
- Windows-Steuerelemente für DL_CANCELDRAG Benachrichtigungs
topic_type:
- apiref
api_name:
- DL_CANCELDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab10f7c31184c44fabdffd4f611847e550b62cc7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106689"
---
# <a name="dl_canceldrag-notification-code"></a>\_Benachrichtigungs Code zum Abbrechen von DL

Signalisiert, dass der Benutzer einen Zieh Vorgang abgebrochen hat, indem er auf die Rechte Maustaste klickt oder die ESC-Taste gedrückt hat. Ein Drag List Box-Element sendet diesen Benachrichtigungs Code in Form einer Drag List-Nachricht an das übergeordnete Fenster. Weitere Informationen finden Sie unter [Drag List Box Messages](about-list-boxes.md).


```C++
DL_CANCELDRAG

    pDragInfo = (LPARAM)(LPDRAGLISTINFO) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**draglistinfo**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo) -Struktur, die den DL \_ -Abbruch Benachrichtigungs Code, das Handle für das Zieh Listenfeld und die Cursorposition enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Durch die Verarbeitung des DL- \_ CancelDrag-Benachrichtigungs Codes kann eine Anwendung den internen Zustand zurücksetzen, um anzugeben, dass das ziehen nicht wirksam ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





