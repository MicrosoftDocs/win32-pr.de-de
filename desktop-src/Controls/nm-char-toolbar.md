---
title: NM_CHAR (Symbolleisten-) Benachrichtigungs Code (kommstrg. h)
description: Wird von einer Symbolleiste gesendet, wenn Sie eine WM- \_ char-Nachricht empfängt. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 7bf0b046-da8e-448f-94e1-62ba0989f7ba
keywords:
- NM_CHAR (Symbolleiste) Benachrichtigungs Code Windows-Steuerelemente
topic_type:
- apiref
api_name:
- NM_CHAR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5a68cb85130f22c8cda63920ada974453a36991
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859342"
---
# <a name="nm_char-toolbar-notification-code"></a>NM \_ char (Toolbar)-Benachrichtigungs Code

Wird von einer Symbolleiste gesendet, wenn Sie eine [**WM- \_ char**](/windows/desktop/inputdev/wm-char) -Nachricht empfängt. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
NM_CHAR

    lpnmc = (LPNMCHAR) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**nmchar**](/windows/win32/api/commctrl/ns-commctrl-nmchar) -Struktur, die zusätzliche Informationen über das Zeichen enthält, das den Benachrichtigungs Code verursacht hat. Der **dwitemprev** -Member dieser Struktur enthält den Befehls Bezeichner des aktuell aktiven Elements oder-1, wenn derzeit kein Element aktiv ist. Der **dwitemnext** -Member dieser Struktur enthält den Befehls Bezeichner des Elements, das heiß wird, oder-1, wenn der Schlüssel nicht mit der Zugriffstaste eines Elements übereinstimmt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, um anzugeben, dass die Symbolleiste das Zeichen nicht verarbeiten soll, und **false** , damit von der Symbolleiste das Zeichen verarbeitet wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

