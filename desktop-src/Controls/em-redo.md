---
title: EM_REDO Meldung (RichEdit. h)
description: Sendet eine EM-Wiederholungs \_ Nachricht an ein Rich Edit-Steuerelement, um die nächste Aktion in der Wiederholungs Warteschlange des Steuer Elements wiederholen.
ms.assetid: 28ec1ec2-a56d-442f-b3cb-9feeb92edaeb
keywords:
- Windows-Steuerelemente für EM_REDO Meldung
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
ms.openlocfilehash: bba7a684db0d40ebcfeec4a540989c4dab4c5dd2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477601"
---
# <a name="em_redo-message"></a>EM-Wiederholungs \_ Nachricht

Sendet eine **EM \_** -Wiederholungs Nachricht an ein Rich Edit-Steuerelement, um die nächste Aktion in der Wiederholungs Warteschlange des Steuer Elements wiederholen.

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

Wenn der **Redo** -Vorgang erfolgreich ist, ist der Rückgabewert ein Wert ungleich 0 (null).

Wenn der **Wiederholungs Vorgang fehl** schlägt, ist der Rückgabewert 0 (null).

## <a name="remarks"></a>Bemerkungen

Um zu ermitteln, ob in der Wiederholungs Warteschlange des Steuer Elements Aktionen vorhanden sind, senden Sie die [**EM \_ CanRedo**](em-canredo.md) -Nachricht.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**EM \_ CanRedo**](em-canredo.md)
</dt> <dt>

[**EM \_ getredoname**](em-getredoname.md)
</dt> <dt>

[**EM \_ getundoname**](em-getundoname.md)
</dt> <dt>

[**EM \_ rückgängig machen**](em-undo.md)
</dt> </dl>

 

 





