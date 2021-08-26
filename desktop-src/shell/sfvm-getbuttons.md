---
description: Ermöglicht dem Rückrufobjekt, die Schaltflächen anzugeben, die der Symbolleiste hinzugefügt werden sollen. Wird von IShellFolderViewCB::MessageSFVCB verwendet.
ms.assetid: 0c0dbf61-9da9-4bcc-bad9-92c3f78db78f
title: SFVM_GETBUTTONS (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 299641ef45d17a6ad1e4d709c3250abe220e297daedabcb563eeba9dcf56262a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008980"
---
# <a name="sfvm_getbuttons-message"></a>SFVM \_ GETBUTTONS-Nachricht

Ermöglicht dem Rückrufobjekt, die Schaltflächen anzugeben, die der Symbolleiste hinzugefügt werden sollen. Wird von [**IShellFolderViewCB::MessageSFVCB verwendet.**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)


```C++
SFVM_GETBUTTONS 

    wParam = (WPARAM)(DWORD) idCmdFirst,cbtnMax;

    lParam = (LPARAM)(LPTBBUTTON) pbtn;

            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*idCmdFirst \_ cbtnMax* \[ in\]
</dt> <dd>

Enthält zwei 16-Bit-Werte, die mit dem [**MAKEWPARAM-Makro**](/windows/win32/api/winuser/nf-winuser-makewparam) in den Parameter gepackt sind. Das Wort in niedriger Reihenfolge enthält die anfängliche Befehls-ID. Das obere Wort enthält die Anzahl der schaltflächen, die hinzugefügt werden sollen, wie in der vorherigen [**SFVM \_ GETBUTTONINFO-Meldung**](sfvm-getbuttoninfo.md) angegeben.

</dd> <dt>

*pbtn* \[ out\]
</dt> <dd>

Die Adresse eines Arrays von [**TBBUTTON-Strukturen,**](/windows/win32/api/commctrl/ns-commctrl-tbbutton) eine für jede Schaltfläche, die der Symbolleiste hinzugefügt werden soll.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Dieser Meldung wird eine [**SFVM \_ GETBUTTONINFO-Nachricht**](sfvm-getbuttoninfo.md) vorangehende. Das Rückrufobjekt muss diese Nachricht verarbeiten, um die Anzahl der Schaltflächen anzugeben und anzugeben, wo sie auf der Symbolleiste platziert werden sollen. Je nachdem, wie das Rückrufobjekt auf die **SFVM \_ GETBUTTONINFO-Nachricht** reagiert, werden die durch den *pbtn-Parameter* angegebenen Schaltflächen an die Standardschaltflächen des Ordneransichtsobjekts des Systems angefügt oder ihr vorgezeigt oder der Standardsatz ersetzt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 
