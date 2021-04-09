---
title: TTN_SHOW Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das Besitzer Fenster, dass ein QuickInfo-Steuerelement angezeigt wird. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: ddfd18cd-0681-4e4a-b258-873f98da7479
keywords:
- Windows-Steuerelemente für TTN_SHOW Benachrichtigungs
topic_type:
- apiref
api_name:
- TTN_SHOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16acb41d1145c176799dd7997b56a850bb45ece7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956536"
---
# <a name="ttn_show-notification-code"></a>TTN \_ Anzeigen des Benachrichtigungs Codes

Benachrichtigt das Besitzer Fenster, dass ein QuickInfo-Steuerelement angezeigt wird. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
TTN_SHOW

    pnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -Struktur.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

[Version 4,70](common-control-versions.md). Wenn die QuickInfo an Ihrem Standard Speicherort angezeigt werden soll, wird NULL zurückgegeben. Zum Anpassen der QuickInfo-Position positionieren Sie das QuickInfo-Fenster mit der [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) -Funktion neu, und geben Sie **true** zurück.

> [!Note]  
> Bei früheren Versionen als 4,70 gibt es keinen Rückgabewert.

 

## <a name="remarks"></a>Bemerkungen

Ein QuickInfo-Fenster Rechteck ist etwas größer als das Textanzeige Rechteck, und sein Ursprung ist von links nach links. Wenn Sie das Textanzeige Rechteck einer QuickInfo exakt positionieren müssen, konvertiert die [**TTM \_**](ttm-adjustrect.md) -Nachricht "Bildschirm" ein Textanzeige Rechteck in das entsprechende QuickInfo-Fenster Rechteck und umgekehrt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

