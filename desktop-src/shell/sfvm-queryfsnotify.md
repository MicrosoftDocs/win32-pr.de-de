---
description: SFVM \_ QUERYFSNOTIFY kann geändert oder nicht verfügbar sein.
ms.assetid: 5d777115-bae3-47c4-9edc-c99c40a4f926
title: SFVM_QUERYFSNOTIFY Meldung (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 932650257ddb039e3841a583c3856316a86eca469db74a0e8ab6ebf33e9411f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941990"
---
# <a name="sfvm_queryfsnotify-message"></a>SFVM \_ QUERYFSNOTIFY-Nachricht

\[**SFVM \_ QUERYFSNOTIFY** ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden.\]

Ermöglicht dem Rückrufobjekt das Registrieren eines Ordners, sodass Änderungen an der Ansicht dieses Ordners Benachrichtigungen generieren. Wird von [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)verwendet.


```C++
SFVM_QUERYFSNOTIFY 
    lParam = (LPARAM)(SHChangeNotifyEntry*) shcne;
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*shcne* \[ in, out\]
</dt> <dd>

Eine -Struktur zum Speichern der PIDL des Elements, das auf Ereignisse überwacht werden soll, und ein Hinweis darauf, ob unterordner dieses Elements ebenfalls überwacht werden sollen.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                |
| Ende des Supports (Client)<br/>    | Windows XP mit SP2<br/>                                                      |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                      |
| Header<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 
