---
description: 'Ermöglicht dem Rückruf Objekt das Ändern eines Windows-Explorer-Popup Menüs, bevor es angezeigt wird. Wird von ishellfolderviewcb:: messagesfvcb verwendet.'
title: SFVM_INITMENUPOPUP Meldung (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 9d7e96e9-c52e-43bd-945b-05db33c8dfd0
api_name:
- SFVM_INITMENUPOPUP
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 1f9a2a169b232fe3ad16eeee8816536ed81c74dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980833"
---
# <a name="sfvm_initmenupopup-message"></a>Sfvm- \_ initmenupopup-Meldung

Ermöglicht dem Rückruf Objekt das Ändern eines Windows-Explorer-Popup Menüs, bevor es angezeigt wird. Wird von [**ishellfolderviewcb:: messagesfvcb**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)verwendet.


```C++
SFVM_INITMENUPOPUP 

    wParam = (WPARAM)(int) idCmd,nIndex;

    lParam = (LPARAM)(HMENU) hmenu;

            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*idcmd \_ nIndex* \[ in\]
</dt> <dd>

Das nieder wertige Wort dieses Parameters enthält den Wert der ersten Befehls-ID, die für Client Befehle reserviert ist. Das hochwertige Wort enthält den Index des Menüs.

</dd> <dt>

*HMENU* \[ in, out\]
</dt> <dd>

Das Handle des Menüs.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Das Objekt "Systemordner Ansicht" sendet diese Nachricht, wenn ein Menü ausgewählt wird, aber bevor es angezeigt wird. Verarbeiten Sie diese Meldung, wenn Sie beispielsweise Menübefehle aktivieren oder deaktivieren müssen. Das Popup Menü kann wie folgt lauten:

-   Das Menü "Datei", "Bearbeiten" oder "Ansicht".
-   Ein Menü der obersten Ebene, das vom Client definiert wird.
-   Ein Client definiertes Untermenü.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**sfvm \_ MergeMenu**](sfvm-mergemenu.md)
</dt> </dl>

 

 
