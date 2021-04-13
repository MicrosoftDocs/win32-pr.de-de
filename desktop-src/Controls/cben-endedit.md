---
title: CBEN_ENDEDIT Benachrichtigungs Code (kommctrl. h)
description: Wird gesendet, wenn der Benutzer einen Vorgang innerhalb des Bearbeitungs Felds abgeschlossen hat oder ein Element aus der Dropdown Liste des Steuer Elements ausgewählt hat. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: b6b50951-7304-4499-b57b-a5b592de2190
keywords:
- Windows-Steuerelemente für CBEN_ENDEDIT Benachrichtigungs
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
ms.openlocfilehash: 679b9f878dbd8f7f374b461ee548f9ce2c62e281
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391550"
---
# <a name="cben_endedit-notification-code"></a>Cben \_ EndEdit-Benachrichtigungs Code

Wird gesendet, wenn der Benutzer einen Vorgang innerhalb des Bearbeitungs Felds abgeschlossen hat oder ein Element aus der Dropdown Liste des Steuer Elements ausgewählt hat. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
CBEN_ENDEDIT

    pnmEditInfo = (PNMCBEENDEDIT) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**nmcbeendedit**](/windows/desktop/api/Commctrl/ns-commctrl-nmcbeendedita) -Struktur, die Informationen darüber enthält, wie der Benutzer den Bearbeitungsvorgang abgeschlossen hat.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

**False** , um den Benachrichtigungs Code zu akzeptieren und dem Steuerelement das Anzeigen des ausgewählten Elements zu ermöglichen. andernfalls **true**.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **Cben \_ "Dededitw** (Unicode)" und " **cben \_** " (ANSI)<br/>                 |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Informationen zu ComboBoxEx-Steuerelementen](comboboxex-controls.md)
</dt> </dl>

 

 





