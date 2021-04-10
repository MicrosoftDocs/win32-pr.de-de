---
title: HDN_BEGINTRACK Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster eines Header Steuer Elements, dass der Benutzer mit dem Ziehen eines unter Teilers im-Steuerelement begonnen hat (d. h., der Benutzer hat mit der linken Maustaste gedrückt, während sich der Mauszeiger auf einem unter Teiler im Header Steuerelement befindet).
ms.assetid: 363b14bc-2b7e-4c37-9caf-7671fcc3cfa5
keywords:
- Windows-Steuerelemente für HDN_BEGINTRACK Benachrichtigungs
topic_type:
- apiref
api_name:
- HDN_BEGINTRACK
- HDN_BEGINTRACKA
- HDN_BEGINTRACKW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6da4ae2c360b13077a612b92ab19a739a58a07e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106683"
---
# <a name="hdn_begintrack-notification-code"></a>Hdn \_ BeginTrack-Benachrichtigungs Code

Benachrichtigt das übergeordnete Fenster eines Header Steuer Elements, dass der Benutzer mit dem Ziehen eines unter Teilers im-Steuerelement begonnen hat (d. h., der Benutzer hat mit der linken Maustaste gedrückt, während sich der Mauszeiger auf einem unter Teiler im Header Steuerelement befindet). Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
HDN_BEGINTRACK

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) -Struktur, die Informationen über das Header Steuerelement und das Element enthält, dessen Trennzeichen gezogen werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **false** zurück, um die Nachverfolgung des unter Teilers zuzulassen, oder **true** , um die Überwachung zu verhindern.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **Hdn \_ Begintrackw** (Unicode) und **Hdn \_ begintracka** (ANSI)<br/>             |



 

 





