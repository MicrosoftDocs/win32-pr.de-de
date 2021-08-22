---
title: HDN_OVERFLOWCLICK Benachrichtigungscode (Commctrl.h)
description: Wird von einem Headersteuerelement an das übergeordnete Element gesendet, wenn auf die Überlaufschaltfläche des Headers geklickt wird. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: 770ae00a-b87f-4de2-b869-2a233f2c493e
keywords:
- HDN_OVERFLOWCLICK Benachrichtigungscode Windows-Steuerelemente
topic_type:
- apiref
api_name:
- HDN_OVERFLOWCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61cee31369bfa1574ba4690f952bc60fb0dde1e5a9bf2f41e98b659356a79625
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119576220"
---
# <a name="hdn_overflowclick-notification-code"></a>HDN \_ OVERFLOWCLICK-Benachrichtigungscode

Wird von einem Headersteuerelement an das übergeordnete Element gesendet, wenn auf die Überlaufschaltfläche des Headers geklickt wird. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
HDN_OVERFLOWCLICK

    pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* \[ In\]
</dt> <dd>

Ein Zeiger auf eine [**NMHEADER-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) die den Benachrichtigungscode beschreibt. Der aufrufende Prozess ist für die Zuordnung dieser Struktur verantwortlich, einschließlich der enthaltenen [**NMHDR-Struktur.**](/windows/desktop/api/richedit/ns-richedit-nmhdr) Legen Sie die Member der **NMHDR-Struktur** fest, einschließlich des *Codemembers,* der auf HDN OVERFLOWCLICK festgelegt werden \_ muss.

Legen Sie den **iItem-Member** der [**NMHEADER-Struktur**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) auf den Index des ersten Headerelements fest, das nicht sichtbar ist und daher bei einem Überlauf angezeigt werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Hinweise

Der Benachrichtigungsempfänger castt **LPARAM,** um die [**NMHEADER-Struktur**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) abzurufen. **WPARAM** enthält die ID des Steuerelements, das die Benachrichtigung sendet.

Diese Meldung wird nur gesendet, wenn [**der HDS \_ OVERFLOW-Stil**](header-control-styles.md) für das Headersteuerelement festgelegt ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





