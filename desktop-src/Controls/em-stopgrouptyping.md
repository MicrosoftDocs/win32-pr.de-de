---
title: EM_STOPGROUPTYPING Meldung (RichEdit. h)
description: Beendet ein Rich-Edit-Steuerelement, das zusätzliche Typisierungsaktionen in der aktuellen Rückgängig-Aktion sammelt. Das Steuerelement speichert die nächste Typisierungsaktion, sofern vorhanden, in eine neue Aktion in der Rückgängig-Warteschlange.
ms.assetid: 3059826f-84d1-4b7b-b4a8-da17d5f41013
keywords:
- Windows-Steuerelemente für EM_STOPGROUPTYPING Meldung
topic_type:
- apiref
api_name:
- EM_STOPGROUPTYPING
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eced7ff12526296552e4adcc38c927ae94ee0502
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741233"
---
# <a name="em_stopgrouptyping-message"></a>EM \_ stopgrouptypismeldungs

Beendet ein Rich-Edit-Steuerelement, das zusätzliche Typisierungsaktionen in der aktuellen Rückgängig-Aktion sammelt. Das Steuerelement speichert die nächste Typisierungsaktion, sofern vorhanden, in eine neue Aktion in der Rückgängig-Warteschlange.

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

Der Rückgabewert ist 0 (null). Diese Meldung kann nicht fehlerhaft sein.

## <a name="remarks"></a>Bemerkungen

Ein Rich Edit-Steuerelement gruppiert aufeinander folgende Typisierungsaktionen, einschließlich Zeichen, die mithilfe des **Backspace** -Schlüssels gelöscht wurden, in eine einzelne Rückgängig-Aktion, bis eines der folgenden Ereignisse eintritt:

-   Das-Steuerelement empfängt eine **EM \_ stopgrouptypisnachricht** .
-   Das Steuerelement verliert den Fokus.
-   Der Benutzer verschiebt die aktuelle Auswahl entweder mithilfe der Pfeiltasten oder durch Klicken auf die Maus.
-   Der Benutzer drückt die ENTF **-Taste.**
-   Der Benutzer führt eine beliebige andere Aktion aus, z. b. einen Einfügevorgang, der **keine** Eingabe erfordert.

Sie können die **EM \_ stopgrouptypisnachricht** senden, um aufeinander folgende Typisierungsaktionen in kleinere rückgängig-Gruppen zu unterbrechen. Sie könnten z. b. **EM \_ stopgrouptypisierung** nach jedem Zeichen oder bei jedem Wort Umbruch senden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**EM \_ rückgängig machen**](em-undo.md)
</dt> </dl>

 

 





