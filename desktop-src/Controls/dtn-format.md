---
title: DTN_FORMAT Benachrichtigungs Code (kommctrl. h)
description: Wird von einem DTP-Steuerelement (Datums-und Zeitauswahl) zum Anfordern von Text gesendet, der in einem Rückruf Feld angezeigt werden soll. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: ce0ee230-638e-425f-9f34-c379342cea93
keywords:
- Windows-Steuerelemente für DTN_FORMAT Benachrichtigungs
topic_type:
- apiref
api_name:
- DTN_FORMAT
- DTN_FORMATA
- DTN_FORMATW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fadd11b090777d2226eeed85f32d2062e8340e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477634"
---
# <a name="dtn_format-notification-code"></a>DTN- \_ Format-Benachrichtigungs Code

Wird von einem DTP-Steuerelement (Datums-und Zeitauswahl) zum Anfordern von Text gesendet, der in einem Rückruf Feld angezeigt werden soll. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
DTN_FORMAT

    lpNMFormat = (LPNMDATETIMEFORMAT) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**NMDATETIMEFORMAT**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimeformata) -Struktur, die Informationen zu dieser Instanz des Benachrichtigungs Codes enthält. Die Struktur enthält die Teil Zeichenfolge, die das Rückruf Feld definiert, und empfängt die formatierte Zeichenfolge, die vom Steuerelement angezeigt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Besitzer des Steuer Elements muss 0 (null) zurückgeben.

## <a name="remarks"></a>Bemerkungen

Durch die Behandlung dieses Benachrichtigungs Codes kann der Besitzer des Steuer Elements eine benutzerdefinierte Zeichenfolge bereitstellen, die vom Steuerelement angezeigt wird. (Weitere Informationen zu Rückruf Feldern finden Sie unter [Rückruf Felder](date-and-time-picker-controls.md).)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **Dtn \_ Formatw** (Unicode) und **Dtn \_ Formata** (ANSI)<br/>                     |



 

 





