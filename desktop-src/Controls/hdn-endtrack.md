---
title: HDN_ENDTRACK Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster eines Header Steuer Elements, dass der Benutzer das Ziehen eines unter Teilers abgeschlossen hat. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: d9b25871-7bd6-439c-91b8-e8249d9be67d
keywords:
- Windows-Steuerelemente für HDN_ENDTRACK Benachrichtigungs
topic_type:
- apiref
api_name:
- HDN_ENDTRACK
- HDN_ENDTRACKA
- HDN_ENDTRACKW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42ab7625690a2de0414f1da391f26f919c1c2617
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040182"
---
# <a name="hdn_endtrack-notification-code"></a>Hdn- \_ EndTrack-Benachrichtigungs Code

Benachrichtigt das übergeordnete Fenster eines Header Steuer Elements, dass der Benutzer das Ziehen eines unter Teilers abgeschlossen hat. Dieser Benachrichtigungs Code wird in Form einer [**WM- \_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
HDN_ENDTRACK

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) -Struktur, die Informationen über das Header Steuerelement und das Element enthält, dessen Trennzeichen gezogen wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **Hdn \_ Endtrackw** (Unicode) und **Hdn \_ endtracka** (ANSI)<br/>                 |



 

 





