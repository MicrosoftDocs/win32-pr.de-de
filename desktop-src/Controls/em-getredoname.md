---
title: EM_GETREDONAME Nachricht (Richedit.h)
description: Ruft ggf. den Typ der nächsten Aktion in der Wiederholungswarteschlange des Rich Edit-Steuerelements ab.
ms.assetid: 8649236f-32dc-45d3-847e-c9f65ffba44c
keywords:
- EM_GETREDONAME Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- EM_GETREDONAME
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9687ae54223ec7cc0f908d747eff2504216b79469b5f285863f8c8ffdfe91b3b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048820"
---
# <a name="em_getredoname-message"></a>EM \_ GETREDONAME-Nachricht

Ruft ggf. den Typ der nächsten Aktion in der Wiederholungswarteschlange des Rich Edit-Steuerelements ab.

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

Wenn die Wiederholungswarteschlange für das Steuerelement nicht leer ist, ist der zurückgegebene Wert ein [**UNDONAMEID-Enumerationswert,**](/windows/desktop/api/Richedit/ne-richedit-undonameid) der den Typ der nächsten Aktion in der Wiederholungswarteschlange des Steuerelements angibt.

Wenn keine wiederholbaren Aktionen vorhanden sind oder der Typ der nächsten wiederholbaren Aktion unbekannt ist, ist der Rückgabewert 0 (null).

## <a name="remarks"></a>Hinweise

Zu den Aktionstypen, die rückgängig oder neu gezeichnet werden können, gehören Eingabe-, Lösch-, Drag&Drop-, Ausschneide- und Einfügevorgänge. Diese Informationen können für Anwendungen nützlich sein, die eine erweiterte Benutzeroberfläche für Rückgängig- und Wiederholungsvorgänge bereitstellen, z. B. ein Dropdownlistenfeld mit wiederverwendebaren Aktionen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[**EM \_ GETUNDONAME**](em-getundoname.md)
</dt> <dt>

[**EM \_ REDO**](em-redo.md)
</dt> <dt>

[**EM \_ UNDO**](em-undo.md)
</dt> <dt>

[**UNDONAMEID**](/windows/desktop/api/Richedit/ne-richedit-undonameid)
</dt> </dl>

 

 





