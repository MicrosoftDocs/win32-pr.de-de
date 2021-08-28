---
description: Ermöglicht dem Rückrufobjekt das Zusammenführen von Menüelementen in Windows Explorer-Menüs. Wird von IShellFolderViewCB::MessageSFVCB verwendet.
title: SFVM_MERGEMENU (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 59bb99a3-9a5a-4ea5-9830-b04d7d886b3f
api_name:
- SFVM_MERGEMENU
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5f6838b3c2ee845794bfa506beada2b7092f1bb918438f820f0e77d6b6543dc1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111170"
---
# <a name="sfvm_mergemenu-message"></a>SFVM \_ MERGEMENU-Nachricht

Ermöglicht dem Rückrufobjekt das Zusammenführen von Menüelementen in Windows Explorer-Menüs. Wird von [**IShellFolderViewCB::MessageSFVCB verwendet.**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)


```C++
SFVM_MERGEMENU 

    lParam = (LPARAM)(LPQCMINFO) pInfo;

            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pInfo* \[ out\]
</dt> <dd>

Eine [**QCMINFO-Struktur**](/windows/desktop/api/shlobj_core/ns-shlobj_core-qcminfo) mit den Informationen, die zum Zusammenführen der Elemente im Menü erforderlich sind.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Nachricht dient im Wesentlichen demselben Zweck wie [**IShellBrowser::InsertMenusSB**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-insertmenussb) und [**IShellBrowser::SetMenuSB**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-setmenusb) in einer benutzerdefinierten Ordneransicht. Weitere Informationen finden Sie im Abschnitt Using *IShellBrowser to Communicate with Windows Explorer* des [Abschnitts Implementing a Folder View](../lwef/nse-folderview.md) (Implementieren einer Ordneransicht).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 
