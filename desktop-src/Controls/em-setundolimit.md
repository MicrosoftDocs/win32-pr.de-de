---
title: EM_SETUNDOLIMIT Meldung (RichEdit. h)
description: Legt die maximale Anzahl von Aktionen fest, die in der Rückgängig-Warteschlange eines Rich-Edit-Steuer Elements gespeichert werden können.
ms.assetid: 485dbcda-89f4-40de-ad55-cd524958e910
keywords:
- Windows-Steuerelemente für EM_SETUNDOLIMIT Meldung
topic_type:
- apiref
api_name:
- EM_SETUNDOLIMIT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5b668d047f1de6d8720f09af5baf23e7cfc9cc2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956632"
---
# <a name="em_setundolimit-message"></a>EM- \_ logdolimit-Meldung

Legt die maximale Anzahl von Aktionen fest, die in der Rückgängig-Warteschlange eines Rich-Edit-Steuer Elements gespeichert werden können.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt die maximale Anzahl von Aktionen an, die in der Rückgängig-Warteschlange gespeichert werden können.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet. Er muss NULL sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist die neue maximale Anzahl von Rückgängig-Aktionen für das Rich Edit-Steuerelement. Dieser Wert ist möglicherweise kleiner als *wParam* , wenn der Arbeitsspeicher begrenzt ist.

## <a name="remarks"></a>Bemerkungen

Standardmäßig ist die maximale Anzahl von Aktionen in der Rückgängig-Warteschlange 100. Wenn Sie diese Zahl erhöhen, muss genügend Arbeitsspeicher zur Verfügung stehen, um die neue Zahl aufnehmen zu können. Um die Leistung zu verbessern, legen Sie den Grenzwert auf den kleinsten möglichen Wert fest.

Wenn Sie den Grenzwert auf NULL festlegen, wird die Funktion **Rückgängig** deaktiviert.

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

[**EM- \_ Wiederholung**](em-redo.md)
</dt> <dt>

[**EM \_ rückgängig machen**](em-undo.md)
</dt> </dl>

 

 





