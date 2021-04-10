---
title: DTN_WMKEYDOWN Benachrichtigungs Code (kommctrl. h)
description: Wird von einem DTP-Steuerelement (Datums-und Zeitauswahl) gesendet, wenn der Benutzer ein Rückruf Feld eingibt. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: e67e222d-28a1-4d30-ae64-8ec9a62fa321
keywords:
- Windows-Steuerelemente für DTN_WMKEYDOWN Benachrichtigungs
topic_type:
- apiref
api_name:
- DTN_WMKEYDOWN
- DTN_WMKEYDOWNA
- DTN_WMKEYDOWNW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce2e7d0761308805746278d2f542f5e9458b56d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103062"
---
# <a name="dtn_wmkeydown-notification-code"></a>DTN \_ wmKeyDown-Benachrichtigungs Code

Wird von einem DTP-Steuerelement (Datums-und Zeitauswahl) gesendet, wenn der Benutzer ein Rückruf Feld eingibt. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
DTN_WMKEYDOWN

    lpDTKeystroke = (LPNMDATETIMEWMKEYDOWN)lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**nmdatetimewmkeydown**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimewmkeydowna) -Struktur, die Informationen zu dieser Instanz des Benachrichtigungs Codes enthält. Die Struktur enthält Informationen über den Schlüssel, den der Benutzer eingegeben hat, die Teil Zeichenfolge, die das Rückruf Feld definiert, und das aktuelle Systemdatum und die aktuelle Systemzeit.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Besitzer des Steuer Elements muss 0 (null) zurückgeben.

## <a name="remarks"></a>Bemerkungen

Durch die Behandlung dieses Benachrichtigungs Codes kann der Besitzer des Steuer Elements bestimmte Antworten auf Tastatureingaben innerhalb der Rückruf Felder des Steuer Elements bereitstellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **Dtn \_ Wmkeydownw** (Unicode) und **Dtn \_ wmkeydowna** (ANSI)<br/>               |



 

 





