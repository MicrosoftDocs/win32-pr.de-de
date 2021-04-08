---
title: NM_KILLFOCUS (Datum/Uhrzeit) des Benachrichtigungs Codes (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster eines Steuer Elements für Datum und Uhrzeit, dass das Steuerelement den Eingabefokus verloren hat. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 33d6b88b-9608-4227-a822-1dc7a77d3a3f
keywords:
- NM_KILLFOCUS (Datum/Uhrzeit) Windows-Steuerelemente für Benachrichtigungs Code
topic_type:
- apiref
api_name:
- NM_KILLFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af47dca130d1025341e2a3c625c1bf7a9c44c42a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949414"
---
# <a name="nm_killfocus-date-time-notification-code"></a>NM- \_ killfokus (Date Time)-Benachrichtigungs Code

Benachrichtigt das übergeordnete Fenster eines Steuer Elements für Datum und Uhrzeit, dass das Steuerelement den Eingabefokus verloren hat. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
NM_KILLFOCUS

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Die Adresse einer [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -Struktur, die zusätzliche Informationen zu dieser Benachrichtigung enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird ignoriert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





