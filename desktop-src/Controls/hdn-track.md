---
title: HDN_TRACK Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster eines Header Steuer Elements, dass der Benutzer einen unter Teiler im Header Steuerelement zieht. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 26660ae1-0d6e-4ee7-8b6a-d621abef352d
keywords:
- Windows-Steuerelemente für HDN_TRACK Benachrichtigungs
topic_type:
- apiref
api_name:
- HDN_TRACK
- HDN_TRACKA
- HDN_TRACKW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91b55ac23e2de17788b17c1f121530308de9e7a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859053"
---
# <a name="hdn_track-notification-code"></a>Benachrichtigungs Code für Hdn- \_ Track

Benachrichtigt das übergeordnete Fenster eines Header Steuer Elements, dass der Benutzer einen unter Teiler im Header Steuerelement zieht. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
HDN_TRACK

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) -Struktur, die Informationen über das Header Steuerelement und das Element enthält, dessen Trennzeichen gezogen werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **false** zurück, um die Nachverfolgung des unter Teilers fortzusetzen, oder **true** zum Beenden der Nachverfolgung

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **Hdn \_ Trackw** (Unicode) und **Hdn \_ tracka** (ANSI)<br/>                       |



 

 





