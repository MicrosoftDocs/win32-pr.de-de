---
title: EM_GETLIMITTEXT Meldung (Winuser.h)
description: Ruft den aktuellen Textgrenzwert für ein Bearbeitungssteuerelement ab. Sie können diese Nachricht entweder an ein Bearbeitungssteuerelement oder ein Rich Edit-Steuerelement senden.
ms.assetid: 778967f0-c090-46a2-9f27-194b17bbb1be
keywords:
- EM_GETLIMITTEXT Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- EM_GETLIMITTEXT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de2066bf03fd8ea05851a9cef58f4e308db49f82bdee94c2d503cadf1c20a2c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117831681"
---
# <a name="em_getlimittext-message"></a>EM \_ GETLIMITTEXT-Nachricht

Ruft den aktuellen Textgrenzwert für ein Bearbeitungssteuerelement ab. Sie können diese Nachricht entweder an ein Bearbeitungssteuerelement oder ein Rich Edit-Steuerelement senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Nicht verwendet; muss 0 (null) sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Nicht verwendet; muss 0 (null) sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist der Textgrenzwert.

## <a name="remarks"></a>Hinweise

**Steuerelemente bearbeiten, Rich Edit 2.0 und höher:** Der Textgrenzwert ist die maximale Textmenge in **TCHAR** s, die das Steuerelement enthalten kann. Für ANSI-Text ist dies die Anzahl von Bytes. Für Unicode-Text ist dies die Anzahl der Zeichen. Zwei Dokumente mit dem gleichen Zeichenlimit ergeben den gleichen Textgrenzwert, auch wenn eines ANSI und das andere Unicode ist.

**Rich Edit 1.0:** Der Textgrenzwert ist die maximale Textmenge in Bytes, die das Rich Edit-Steuerelement enthalten kann.

**Rich Edit:** Wird in Microsoft Rich Edit 1.0 und höher unterstützt. Informationen zur Kompatibilität von Rich Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter [Informationen zu Rich Edit-Steuerelementen.](about-rich-edit-controls.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**EM \_ SETLIMITTEXT**](em-setlimittext.md)
</dt> </dl>

 

 





