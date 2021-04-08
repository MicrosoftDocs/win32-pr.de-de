---
title: UDN_DELTAPOS Benachrichtigungs Code (kommctrl. h)
description: Wird vom Betriebssystem an das übergeordnete Fenster eines auf-ab-Steuer Elements gesendet, wenn sich die Position des-Steuer Elements ändert.
ms.assetid: 66262566-d35a-4b2a-8157-d1e789a21016
keywords:
- Windows-Steuerelemente für UDN_DELTAPOS Benachrichtigungs
topic_type:
- apiref
api_name:
- UDN_DELTAPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dec8f0ec2200d1f18e48c068b581b42868db197b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741681"
---
# <a name="udn_deltapos-notification-code"></a>Udn- \_ Delta-Benachrichtigungs Code

Wird vom Betriebssystem an das übergeordnete Fenster eines auf-ab-Steuer Elements gesendet, wenn sich die Position des-Steuer Elements ändert. Dies geschieht, wenn der Benutzer eine Änderung des Werts anfordert, indem er den Pfeil nach oben oder nach unten drückt. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
UDN_DELTAPOS 

    lpnmud = (LPNMUPDOWN) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**nmupdown**](/windows/win32/api/commctrl/ns-commctrl-nmupdown) -Struktur, die Informationen über die Positionsänderung enthält. Der **IPOs** -Member dieser-Struktur enthält die aktuelle Position des-Steuer Elements. Der **idelta** -Member der-Struktur ist eine Ganzzahl mit Vorzeichen, die die vorgeschlagene Änderung an der Position enthält. Wenn der Benutzer auf die Schaltfläche "nach oben" geklickt hat, ist dies ein positiver Wert. Wenn der Benutzer auf die Schaltfläche "nach unten" geklickt hat, ist dies ein negativer Wert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen Wert ungleich 0 (null) zurück, um zu verhindern, dass die Position des Steuer Elements geändert wird.

## <a name="remarks"></a>Bemerkungen

Der udn- \_ Delta-Delta-Benachrichtigungs Code wird vor der [**WM- \_ VScroll**](wm-vscroll.md) -oder [**WM- \_ HScroll**](wm-hscroll.md) -Nachricht gesendet, die tatsächlich die Position des Steuer Elements ändert. Dies ermöglicht es Ihnen, die Änderung zu überprüfen, zuzulassen, zu ändern oder zu unterbinden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**WM- \_ Befehl**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

