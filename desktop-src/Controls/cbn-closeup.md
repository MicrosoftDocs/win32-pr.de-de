---
title: CBN_CLOSEUP Benachrichtigungs Code (Winuser. h)
description: Wird gesendet, wenn das Listenfeld eines Kombinations Felds geschlossen wurde. Das übergeordnete Fenster des Kombinations Felds empfängt diesen Benachrichtigungs Code über die WM- \_ Befehls Meldung.
ms.assetid: 79b2108e-1ef3-433d-a0b0-ac9ad1a93905
keywords:
- Windows-Steuerelemente für CBN_CLOSEUP Benachrichtigungs
topic_type:
- apiref
api_name:
- CBN_CLOSEUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec67cf68109d32d6e1ad714f91a97987f9a3734d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106443"
---
# <a name="cbn_closeup-notification-code"></a>CBN- \_ closeup-Benachrichtigungs Code

Wird gesendet, wenn das Listenfeld eines Kombinations Felds geschlossen wurde. Das übergeordnete Fenster des Kombinations Felds empfängt diesen Benachrichtigungs Code über die [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldung.


```C++
CBN_CLOSEUP

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) enthält den Steuerelement Bezeichner des Kombinations Felds. Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt den Benachrichtigungs Code an.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle für das Kombinations Feld.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn der Benutzer die aktuelle Auswahl geändert hat, sendet das Kombinations Feld auch den [CBN \_ selChange](cbn-selchange.md) -Benachrichtigungs Code, wenn die Dropdown Liste geschlossen wird. Im Allgemeinen können Sie die Reihenfolge, in der die Benachrichtigungs Codes gesendet werden, nicht vorhersagen. Insbesondere kann es vorkommen, dass ein CBN-Änderungs \_ Benachrichtigungs Code entweder vor oder nach einem CBN- \_ closeup-Benachrichtigungs Code vorliegt.

Um einen bestimmten Prozess jedes Mal auszuführen, wenn der Benutzer ein Listenelement auswählt, können Sie entweder den Benachrichtigungs Code [CBN \_ selChange](cbn-selchange.md) oder CBN \_ closeup verarbeiten. In der Regel warten Sie \_ vor dem Verarbeiten einer Änderung in der aktuellen Auswahl den Benachrichtigungs Code für die CBN-Schließung. Dies kann besonders wichtig sein, wenn eine beträchtliche Menge an Verarbeitung erforderlich ist.

Dieser Benachrichtigungs Code wird nicht an ein Kombinations Feld mit dem [**\_ einfachen CBS**](combo-box-styles.md) -Format gesendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[CBN- \_ Dropdown](cbn-dropdown.md)
</dt> <dt>

[CBN \_ selChange](cbn-selchange.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**WM- \_ Befehl**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

