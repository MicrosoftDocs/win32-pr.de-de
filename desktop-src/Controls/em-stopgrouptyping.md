---
title: EM_STOPGROUPTYPING Nachricht (Richedit.h)
description: Verhindert, dass ein umfassendes Bearbeitungssteuerelement zusätzliche Eingabeaktionen für die aktuelle Rückgängigaktion erfasst. Das Steuerelement speichert ggf. die nächste Eingabeaktion in einer neuen Aktion in der Rückgängig-Warteschlange.
ms.assetid: 3059826f-84d1-4b7b-b4a8-da17d5f41013
keywords:
- EM_STOPGROUPTYPING Windows-Steuerelemente für Nachrichten
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
ms.openlocfilehash: 5e62a5d652218b24240ce612851c4c08e335b31230532bc778bb44c5d7e74854
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118672278"
---
# <a name="em_stopgrouptyping-message"></a>EM \_ STOPGROUPTYPING-Meldung

Verhindert, dass ein umfassendes Bearbeitungssteuerelement zusätzliche Eingabeaktionen für die aktuelle Rückgängigaktion erfasst. Das Steuerelement speichert ggf. die nächste Eingabeaktion in einer neuen Aktion in der Rückgängig-Warteschlange.

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

Der Rückgabewert ist 0 (null). Diese Meldung kann nicht fehlschlagen.

## <a name="remarks"></a>Hinweise

Ein Umfassendes Bearbeitungssteuerelement gruppiert aufeinanderfolgende Eingabeaktionen, einschließlich Zeichen, die mithilfe der **Rücktaste** gelöscht wurden, zu einer einzelnen Rückgängigaktion, bis eines der folgenden Ereignisse eintritt:

-   Das Steuerelement empfängt eine **EM \_ STOPGROUPTYPING-Meldung.**
-   Das Steuerelement verliert den Fokus.
-   Der Benutzer verschiebt die aktuelle Auswahl entweder mithilfe der Pfeiltasten oder durch Klicken mit der Maus.
-   Der Benutzer drückt die **Löschtaste.**
-   Der Benutzer führt eine andere Aktion aus, z. B. einen Einfügevorgang, der **keine** Eingabe umfasst.

Sie können die **EM \_ STOPGROUPTYPING-Nachricht** senden, um aufeinanderfolgende Eingabeaktionen in kleinere Rückgängiggruppen zu unterteilen. Beispielsweise können Sie **EM \_ STOPGROUPTYPING** nach jedem Zeichen oder an jedem Wortbruch senden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**EM \_ UNDO**](em-undo.md)
</dt> </dl>

 

 





