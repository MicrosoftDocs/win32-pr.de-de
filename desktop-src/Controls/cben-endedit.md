---
title: CBEN_ENDEDIT Benachrichtigungscode (Commctrl.h)
description: Wird gesendet, wenn der Benutzer einen Vorgang im Bearbeitungsfeld abgeschlossen oder ein Element aus der Dropdownliste des Steuerelements ausgewählt hat. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: b6b50951-7304-4499-b57b-a5b592de2190
keywords:
- CBEN_ENDEDIT Benachrichtigungscode Windows-Steuerelemente
topic_type:
- apiref
api_name:
- CBEN_ENDEDIT
- CBEN_ENDEDITA
- CBEN_ENDEDITW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22ae9205e84e4f1c0b10e516b1f406f2d167f1bc5cc38417a31379d20e16fcac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118413950"
---
# <a name="cben_endedit-notification-code"></a>CBEN \_ ENDEDIT-Benachrichtigungscode

Wird gesendet, wenn der Benutzer einen Vorgang im Bearbeitungsfeld abgeschlossen oder ein Element aus der Dropdownliste des Steuerelements ausgewählt hat. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
CBEN_ENDEDIT

    pnmEditInfo = (PNMCBEENDEDIT) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**NMCBEENDEDIT-Struktur,**](/windows/desktop/api/Commctrl/ns-commctrl-nmcbeendedita) die Informationen darüber enthält, wie der Benutzer den Bearbeitungsvorgang abgeschlossen hat.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

**FALSE,** um den Benachrichtigungscode zu akzeptieren und dem Steuerelement das Anzeigen des ausgewählten Elements zu ermöglichen; Andernfalls **TRUE.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **CBEN \_ ENDEDITW** (Unicode) und **CBEN \_ ENDEDITA** (ANSI)<br/>                 |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Informationen zu ComboBoxEx-Steuerelementen](comboboxex-controls.md)
</dt> </dl>

 

 





