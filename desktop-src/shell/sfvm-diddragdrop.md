---
description: Sfvm \_ diddragdrop kann geändert oder nicht verfügbar sein.
ms.assetid: 5d37cf61-d8a7-4afa-9159-fea13d2b1d59
title: SFVM_DIDDRAGDROP Meldung (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 025bcf6320b014ff31b0819f394dd8b76fa90e59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104994918"
---
# <a name="sfvm_diddragdrop-message"></a>Sfvm- \_ diddragdrop-Nachricht

\[**Sfvm \_ Diddragdrop** steht zur Verwendung in den Betriebssystemen zur Verfügung, die im Abschnitt "Anforderungen" angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden.\]

Benachrichtigt die Rückruffunktion, dass ein Drag & Drop-Vorgang begonnen hat. Wird von [**ishellfolderviewcb:: messagesfvcb**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)verwendet.


```C++
SFVM_DIDDRAGDROP 
    wParam = (WPARAM)(DWORD) dwEffect;
    lParam = (LPARAM)(IDataObject*) pIdo;
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dweffect* \[ in\]
</dt> <dd>

Ein Drop Effect-Spezifizierer aus der [**dropffect**](../com/dropeffect-constants.md) -Enumeration. Dies wird durch Aufrufen von [**shdodragdrop**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shdodragdrop)erreicht.

</dd> <dt>

*Pido* \[ in\]
</dt> <dd>

Ein Zeiger auf die [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) -Instanz.

</dd> </dl>

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                |
| Ende des Supports (Client)<br/>    | Windows XP mit SP2<br/>                                                      |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                      |
| Header<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
