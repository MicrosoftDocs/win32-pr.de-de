---
title: UDN_DELTAPOS Benachrichtigungscode (Commctrl.h)
description: Wird vom Betriebssystem an das übergeordnete Fenster eines Auf-Ab-Steuerelements gesendet, wenn sich die Position des Steuerelements ändert.
ms.assetid: 66262566-d35a-4b2a-8157-d1e789a21016
keywords:
- UDN_DELTAPOS Benachrichtigungscode Windows Steuerelementen
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
ms.openlocfilehash: 81285d2e0aa5c9a8b65eabf7c5b23d02da3acf02ac13e3274accce340530024f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088410"
---
# <a name="udn_deltapos-notification-code"></a>UDN \_ DELTAPOS-Benachrichtigungscode

Wird vom Betriebssystem an das übergeordnete Fenster eines Auf-Ab-Steuerelements gesendet, wenn sich die Position des Steuerelements ändert. Dies geschieht, wenn der Benutzer eine Änderung des Werts an fordert, indem er den Nach-oben- oder Nach-unten-Pfeil des Steuerelements drückt. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
UDN_DELTAPOS 

    lpnmud = (LPNMUPDOWN) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**NMUPDOWN-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-nmupdown) die Informationen zur Positionsänderung enthält. Der **iPos-Member** dieser -Struktur enthält die aktuelle Position des Steuerelements. Das **iDelta-Member** der -Struktur ist eine ganze Zahl mit Vorzeichen, die die vorgeschlagene Änderung der Position enthält. Wenn der Benutzer auf die Schaltfläche nach oben geklickt hat, ist dies ein positiver Wert. Wenn der Benutzer auf die Schaltfläche "Nach unten" geklickt hat, ist dies ein negativer Wert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Geben Sie einen Wert ungleich 0 (null) zurück, um die Änderung an der Position des Steuerelements zu verhindern, oder 0 (null), um die Änderung zu ermöglichen.

## <a name="remarks"></a>Hinweise

Der UDN DELTAPOS-Benachrichtigungscode wird vor der \_ [**WM \_ VSCROLL-**](wm-vscroll.md) oder [**WM \_ HSCROLL-Meldung**](wm-hscroll.md) gesendet, wodurch die Position des Steuerelements tatsächlich geändert wird. Auf diese Weise können Sie die Änderung untersuchen, zulassen, ändern oder nicht zulassen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_WM-BEFEHL**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

