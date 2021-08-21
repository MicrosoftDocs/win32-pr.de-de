---
title: DTN_FORMATQUERY Benachrichtigungscode (Commctrl.h)
description: Wird von einem DTP-Steuerelement (Date and Time Picker) gesendet, um die maximal zulässige Größe der Zeichenfolge abzurufen, die in einem Rückruffeld angezeigt wird. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: 0f00086a-0ab8-4f6f-9c3e-6e77008aa088
keywords:
- DTN_FORMATQUERY Benachrichtigungscode Windows Steuerelementen
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
ms.openlocfilehash: 14bd1a9efe22251aba71f157dfb2a68e2b0a70385c30564bb7f08e420e0c0cb4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019988"
---
# <a name="dtn_formatquery-notification-code"></a>DTN \_ FORMATQUERY-Benachrichtigungscode

Wird von einem DTP-Steuerelement (Date and Time Picker) gesendet, um die maximal zulässige Größe der Zeichenfolge abzurufen, die in einem Rückruffeld angezeigt wird. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
DTN_FORMATQUERY

    lpDTFormatQuery = (LPNMDATETIMEFORMATQUERY) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**NMDATETIMEFORMATQUERY-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimeformatquerya) die Informationen über das Rückruffeld enthält. Die -Struktur enthält eine Teilzeichenfolge, die ein Rückruffeld definiert und die maximal zulässige Größe der Zeichenfolge empfängt, die im Rückruffeld angezeigt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Besitzer des Steuerelements muss die maximal mögliche Breite des Texts berechnen, der im Rückruffeld angezeigt wird, den **szMax-Member** der [**NMDATETIMEFORMATQUERY-Struktur**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimeformatquerya) festlegen und 0 (null) zurückgeben.

## <a name="remarks"></a>Hinweise

Durch die Behandlung dieses Benachrichtigungscodes wird das Steuerelement auf die maximale Größe der Zeichenfolge vorbereitet, die in einem bestimmten Rückruffeld angezeigt wird. Dadurch kann das Steuerelement die Ausgabe jederzeit ordnungsgemäß anzeigen, was das Flackern innerhalb der Anzeige des Steuerelements reduziert. (Weitere Informationen zu Rückruffeldern finden Sie unter [Rückruffelder.)](date-and-time-picker-controls.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **DTN \_ FORMATQUERYW** (Unicode) und **DTN \_ FORMATQUERYA** (ANSI)<br/>           |



 

 





