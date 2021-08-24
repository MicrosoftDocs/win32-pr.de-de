---
description: Benachrichtigt das Rückrufobjekt des Containerstandorts. Dies wird nur verwendet, wenn IObjectWithSite::SetSite nicht unterstützt wird und SHCreateShellFolderViewEx verwendet wird. Wird von IShellFolderViewCB::MessageSFVCB verwendet.
ms.assetid: a4aa40f8-1d98-4686-86e2-87280e470aac
title: SFVM_SETISFV Meldung (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e6d9ad3e9b1b8302089da8a59a8d5502a04392da77c6fc5276725b144efa026
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119660800"
---
# <a name="sfvm_setisfv-message"></a>SFVM \_ SETISFV-Nachricht

\[Diese Benachrichtigung wird über Windows XP Service Pack 2 (SP2) und Windows Server 2003 unterstützt. In nachfolgenden Versionen von Windows wird sie möglicherweise nicht unterstützt.\]

Benachrichtigt das Rückrufobjekt des Containerstandorts. Dies wird nur verwendet, wenn [**IObjectWithSite::SetSite**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768221(v=vs.85)) nicht unterstützt wird und [**SHCreateShellFolderViewEx**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderviewex) verwendet wird. Wird von [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)verwendet.


```C++
SFVM_SETISFV
    lParam = (LPARAM)(IUnknown*) site;
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*site* \[ In\]
</dt> <dd>

Ein Zeiger auf die [**IUnknown-Schnittstelle**](/windows/win32/api/unknwn/nn-unknwn-iunknown) des Containerstandorts.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 
