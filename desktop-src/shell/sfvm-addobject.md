---
description: Fügt der Shellansicht ein -Objekt hinzu. Wird von SHShellFolderView \_ Message verwendet.
title: SFVM_ADDOBJECT (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 90394af6-3809-457c-b2f2-5f35187ed45b
api_name:
- SFVM_ADDOBJECT
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 441ddac74e1640b2f836686c171d6fc896cbccee2dd6325c31041903ba610b39
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119661060"
---
# <a name="sfvm_addobject-message"></a>SFVM \_ ADDOBJECT-Nachricht

Fügt der Shellansicht ein -Objekt hinzu. Wird von [**SHShellFolderView Message \_ verwendet.**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message)


```C++
SFVM_ADDOBJECT 

    lParam = (LPARAM) pidl;

            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pidl* \[ In\]
</dt> <dd>Ein Zeiger auf das hinzuzufügende Objekt.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die neue Listview-Element-ID des hinzugefügten Objekts zurück, wenn der Prozess erfolgreich war. andernfalls wird -1 zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 




