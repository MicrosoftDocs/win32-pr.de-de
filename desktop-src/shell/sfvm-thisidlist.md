---
description: SFVM \_ THISIDLIST kann geändert oder nicht verfügbar sein.
ms.assetid: 488f696d-aa71-4727-bbd2-c99e7d245d85
title: SFVM_THISIDLIST (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd00f1cfc2b6661dac2414f0327cab03d4c0586eb62b992b5e33f81e64565246
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968629"
---
# <a name="sfvm_thisidlist-message"></a>SFVM \_ THISIDLIST-Meldung

\[**SFVM \_ THISIDLIST steht** für die Verwendung in den Betriebssystemen zur Verfügung, die im Abschnitt Anforderungen angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden.\]

Ermöglicht es dem Rückrufobjekt, den Zeiger der Sicht auf eine Elementbezeichnerliste (PIDL) anzugeben. Dies wird nur verwendet, wenn [**IPersistIDList::SetIDList**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistidlist-setidlist) und [**IPersistFolder2::GetCurFolder**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder2-getcurfolder) fehlgeschlagen sind. Wird von [**IShellFolderViewCB::MessageSFVCB verwendet.**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)


```C++
SFVM_THISIDLIST
    lParam = (LPARAM)(LPITEMIDLIST*) pidl;
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pidl* \[ out\]
</dt> <dd>

Die Adresse der PIDL der Ansicht.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                |
| Ende des Supports (Client)<br/>    | Windows XP mit SP2<br/>                                                      |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                      |
| Header<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 
