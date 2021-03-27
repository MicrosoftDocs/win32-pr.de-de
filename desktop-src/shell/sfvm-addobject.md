---
description: Fügt der shellansicht ein Objekt hinzu. Wird von der shshellfolderview- \_ Nachricht verwendet.
title: SFVM_ADDOBJECT Meldung (shlobj. h)
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
ms.openlocfilehash: 0e5b3f0a5b1aed634ab8929b0501d2e23ba40352
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104994887"
---
# <a name="sfvm_addobject-message"></a>Sfvm- \_ AddObject-Nachricht

Fügt der shellansicht ein Objekt hinzu. Wird von der [**shshellfolderview- \_ Nachricht**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message)verwendet.


```C++
SFVM_ADDOBJECT 

    lParam = (LPARAM) pidl;

            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PIDL* \[ in\]
</dt> <dd>Ein Zeiger auf das hinzu zufügende Objekt.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die neue ListView-Element-ID des hinzugefügten Objekts zurück, wenn der Prozess erfolgreich war. Andernfalls wird-1 zurückgegeben.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 




