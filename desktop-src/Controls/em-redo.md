---
title: EM_REDO Nachricht (Richedit.h)
description: Sendet eine \_ EM-REDO-Nachricht an ein Rich-Edit-Steuerelement, um die nächste Aktion in der Wiederholungswarteschlange des Steuerelements zu wiederholen.
ms.assetid: 28ec1ec2-a56d-442f-b3cb-9feeb92edaeb
keywords:
- EM_REDO Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- EM_REDO
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d39b679e8bf7e78cf7ce028d0bb440438770d0d0123516313fb418b2136ebc11
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119437860"
---
# <a name="em_redo-message"></a>\_EM-REDO-Nachricht

Sendet eine **\_ EM-REDO-Nachricht** an ein Rich-Edit-Steuerelement, um die nächste Aktion in der Wiederholungswarteschlange des Steuerelements zu wiederholen.

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

Wenn der **Wiederholungsvorgang** erfolgreich ist, ist der Rückgabewert ein Wert ungleich 0 (null).

Wenn der **Wiederholungsvorgang** fehlschlägt, ist der Rückgabewert 0 (null).

## <a name="remarks"></a>Hinweise

Um zu bestimmen, ob aktionen in der Wiederholungswarteschlange des Steuerelements vorhanden sind, senden Sie die [**EM \_ CANREDO-Nachricht.**](em-canredo.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Referenz**
</dt> <dt>

[**EM \_ CANREDO**](em-canredo.md)
</dt> <dt>

[**EM \_ GETREDONAME**](em-getredoname.md)
</dt> <dt>

[**EM \_ GETUNDONAME**](em-getundoname.md)
</dt> <dt>

[**EM \_ UNDO**](em-undo.md)
</dt> </dl>

 

 





