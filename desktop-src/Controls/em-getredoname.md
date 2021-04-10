---
title: EM_GETREDONAME Meldung (RichEdit. h)
description: Ruft den Typ der nächsten Aktion (sofern vorhanden) in der Wiederholungs Warteschlange des Rich-Edit-Steuer Elements ab.
ms.assetid: 8649236f-32dc-45d3-847e-c9f65ffba44c
keywords:
- Windows-Steuerelemente für EM_GETREDONAME Meldung
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
ms.openlocfilehash: 9ea44257344b9ebdb8ffe91ad97e939aae0db9b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956580"
---
# <a name="em_getredoname-message"></a>EM \_ getredoname-Meldung

Ruft den Typ der nächsten Aktion (sofern vorhanden) in der Wiederholungs Warteschlange des Rich-Edit-Steuer Elements ab.

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

Wenn die Wiederholungs Warteschlange für das Steuerelement nicht leer ist, ist der zurückgegebene Wert ein [**undonameid**](/windows/desktop/api/Richedit/ne-richedit-undonameid) -Enumerationswert, der den Typ der nächsten Aktion in der Wiederholungs Warteschlange des Steuer Elements angibt.

Wenn keine Redoable-Aktionen vorhanden sind oder der Typ der nächsten Redoable-Aktion unbekannt ist, ist der Rückgabewert 0 (null).

## <a name="remarks"></a>Bemerkungen

Die Typen von Aktionen, die rückgängig gemacht oder wiederholt werden können, sind das eingeben, löschen, Drag-Drop-, Ausschneide-und Einfügevorgänge. Diese Informationen können für Anwendungen nützlich sein, die eine erweiterte Benutzeroberfläche für Rückgängigvorgänge und Wiederholungs Vorgänge bereitstellen, z. b. ein Dropdown-Listenfeld mit Redoable-Aktionen.

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

[**EM \_ getundoname**](em-getundoname.md)
</dt> <dt>

[**EM- \_ Wiederholung**](em-redo.md)
</dt> <dt>

[**EM \_ rückgängig machen**](em-undo.md)
</dt> <dt>

[**Undonameid**](/windows/desktop/api/Richedit/ne-richedit-undonameid)
</dt> </dl>

 

 





