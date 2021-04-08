---
title: DTN_FORMATQUERY Benachrichtigungs Code (kommctrl. h)
description: Wird von einem DTP-Steuerelement gesendet, um die maximal zulässige Größe der Zeichenfolge abzurufen, die in einem Rückruf Feld angezeigt wird. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 0f00086a-0ab8-4f6f-9c3e-6e77008aa088
keywords:
- Windows-Steuerelemente für DTN_FORMATQUERY Benachrichtigungs
topic_type:
- apiref
api_name:
- DTN_FORMATQUERY
- DTN_FORMATQUERYA
- DTN_FORMATQUERYW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69e9653f369f13e0ef4a775265d763e854db4de7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949466"
---
# <a name="dtn_formatquery-notification-code"></a>DTN \_ formatQuery-Benachrichtigungs Code

Wird von einem DTP-Steuerelement gesendet, um die maximal zulässige Größe der Zeichenfolge abzurufen, die in einem Rückruf Feld angezeigt wird. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
DTN_FORMATQUERY

    lpDTFormatQuery = (LPNMDATETIMEFORMATQUERY) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**nmdatetimeformatquery**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimeformatquerya) -Struktur, die Informationen über das Rückruf Feld enthält. Die-Struktur enthält eine Teil Zeichenfolge, die ein Rückruf Feld definiert und die maximal zulässige Größe der Zeichenfolge empfängt, die im Rückruf Feld angezeigt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Besitzer des Steuer Elements muss die maximal mögliche Breite des Texts berechnen, der im Rückruf Feld angezeigt wird, den **szmax** -Member der [**nmdatetimeformatquery**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimeformatquerya) -Struktur festlegen und 0 (null) zurückgeben.

## <a name="remarks"></a>Bemerkungen

Durch die Behandlung dieses Benachrichtigungs Codes wird das Steuerelement so vorbereitet, dass es die maximale Größe der Zeichenfolge anpasst, die in einem bestimmten Rückruf Feld angezeigt wird. Dies ermöglicht es dem Steuerelement, die Ausgabe jederzeit ordnungsgemäß anzuzeigen und das Flimmern innerhalb der Anzeige des Steuer Elements zu reduzieren. (Weitere Informationen zu Rückruf Feldern finden Sie unter [Rückruf Felder](date-and-time-picker-controls.md).)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **Dtn \_ Formatqueryw** (Unicode) und **Dtn \_ formatquerya** (ANSI)<br/>           |



 

 





