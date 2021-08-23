---
title: EM_SETUNDOLIMIT Nachricht (Richedit.h)
description: Legt die maximale Anzahl von Aktionen fest, die in der Rückgängig-Warteschlange eines Rich-Edit-Steuerelements gespeichert werden können.
ms.assetid: 485dbcda-89f4-40de-ad55-cd524958e910
keywords:
- EM_SETUNDOLIMIT Windows-Steuerelemente für Nachrichten
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
ms.openlocfilehash: 771e339e38437ea0299e5da6120fa555fd26148f72ff7da4e0287ed46cc4ad22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697520"
---
# <a name="em_setundolimit-message"></a>EM \_ SETUNDOLIMIT-Meldung

Legt die maximale Anzahl von Aktionen fest, die in der Rückgängig-Warteschlange eines Rich-Edit-Steuerelements gespeichert werden können.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt die maximale Anzahl von Aktionen an, die in der Rückgängig-Warteschlange gespeichert werden können.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet. muss 0 (null) sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist die neue maximale Anzahl von Rückgängig-Aktionen für das Rich Edit-Steuerelement. Dieser Wert kann kleiner als *wParam* sein, wenn der Arbeitsspeicher begrenzt ist.

## <a name="remarks"></a>Hinweise

Standardmäßig beträgt die maximale Anzahl von Aktionen in der Rückgängig-Warteschlange 100. Wenn Sie diese Zahl erhöhen, muss genügend Arbeitsspeicher verfügbar sein, um die neue Zahl aufnehmen zu können. Um eine bessere Leistung zu erzielen, legen Sie den Grenzwert auf den kleinstmöglichen Wert fest.

Wenn Sie den Grenzwert auf 0 (null) festlegen, wird die Funktion **Rückgängig** deaktiviert.

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

[**EM \_ CANREDO**](em-canredo.md)
</dt> <dt>

[**EM \_ GETREDONAME**](em-getredoname.md)
</dt> <dt>

[**EM \_ GETUNDONAME**](em-getundoname.md)
</dt> <dt>

[**EM \_ REDO**](em-redo.md)
</dt> <dt>

[**EM \_ UNDO**](em-undo.md)
</dt> </dl>

 

 





