---
description: 'Benachrichtigt das Rückruf Objekt, dass einer seiner Symbolleisten-oder Menübefehle vom Benutzer aufgerufen wurde. Wird von ishellfolderviewcb:: messagesfvcb verwendet.'
ms.assetid: 6b9e4a4d-ec45-489c-bbff-d123d5756b75
title: SFVM_INVOKECOMMAND Meldung (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e5fc9709827250e5cf8060400bbecb714ae5998
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868695"
---
# <a name="sfvm_invokecommand-message"></a>Sfvm \_ InvokeCommand-Meldung

Benachrichtigt das Rückruf Objekt, dass einer seiner Symbolleisten-oder Menübefehle vom Benutzer aufgerufen wurde. Wird von [**ishellfolderviewcb:: messagesfvcb**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)verwendet.


```C++
SFVM_INVOKECOMMAND 

    wParam = (WPARAM)(UINT) idCmd;

            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*idcmd* \[ in\]
</dt> <dd>

Die Befehls-ID der ausgewählten Symbolleiste oder des ausgewählten Menü Elements.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Meldung dient im wesentlichen derselben Funktion wie eine [**WM- \_ Befehls**](../menurc/wm-command.md) Nachricht in einer herkömmlichen Fenster Prozedur. Dadurch kann das Rückruf Objekt alle Elemente verarbeiten, die es dem Windows-Explorer-Tool oder der Menüleiste hinzugefügt hat.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
