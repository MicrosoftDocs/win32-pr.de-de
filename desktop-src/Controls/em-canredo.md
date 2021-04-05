---
title: EM_CANREDO Meldung (RichEdit. h)
description: Bestimmt, ob in der Wiederholungs Warteschlange für das Steuerelement Aktionen vorhanden sind.
ms.assetid: 4a76adc8-f815-4cf7-8742-b7695e5a0f64
keywords:
- Windows-Steuerelemente für EM_CANREDO Meldung
topic_type:
- apiref
api_name:
- EM_CANREDO
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccfb12f8e72bdf5321151cd3a70b74f322a46591
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859056"
---
# <a name="em_canredo-message"></a>EM \_ CanRedo-Nachricht

Bestimmt, ob in der Wiederholungs Warteschlange für das Steuerelement Aktionen vorhanden sind.

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

Wenn in der Wiederholungs Warteschlange für das Steuerelement Aktionen vorhanden sind, ist der Rückgabewert ein Wert ungleich 0 (null).

Wenn die Wiederholungs Warteschlange leer ist, ist der Rückgabewert 0 (null).

## <a name="remarks"></a>Bemerkungen

Um den letzten Rückgängig-Vorgang zu wiederholen, senden Sie die EM-Wiederholungs Nachricht. [**\_**](em-redo.md)

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

[**EM \_ getredoname**](em-getredoname.md)
</dt> <dt>

[**EM \_ getundoname**](em-getundoname.md)
</dt> <dt>

[**EM- \_ Wiederholung**](em-redo.md)
</dt> <dt>

[**EM \_ rückgängig machen**](em-undo.md)
</dt> </dl>

 

 





