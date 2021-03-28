---
description: Die sfvm- \_ thisidlist kann geändert werden oder ist nicht verfügbar.
ms.assetid: 488f696d-aa71-4727-bbd2-c99e7d245d85
title: SFVM_THISIDLIST Meldung (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e86e24199e5adbb895c8d1d5fc36bfff0c109bc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760195"
---
# <a name="sfvm_thisidlist-message"></a>Sfvm- \_ thisidlist-Meldung

\[**Sfvm \_ Thisidlist** ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden.\]

Ermöglicht dem Rückruf Objekt, den Zeiger der Ansicht auf eine Element Bezeichner-Liste (PIDL) anzugeben. Dies wird nur verwendet, wenn " [**ipersistidlist:: abtidlist**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistidlist-setidlist) " und " [**IPersistFolder2:: getcurrfolder**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder2-getcurfolder) " fehlgeschlagen sind. Wird von [**ishellfolderviewcb:: messagesfvcb**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)verwendet.


```C++
SFVM_THISIDLIST
    lParam = (LPARAM)(LPITEMIDLIST*) pidl;
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PIDL* \[ vorgenommen\]
</dt> <dd>

Die Adresse der PIDL der Ansicht.

</dd> </dl>

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                |
| Ende des Supports (Client)<br/>    | Windows XP mit SP2<br/>                                                      |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                      |
| Header<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
