---
description: Aktualisiert ein -Objekt, indem ein Zeiger auf ein Array von zwei Zeigern auf Elementbezeichnerlisten (PIDLs) übergeben wird. Wird von SHShellFolderView \_ Message verwendet.
title: SFVM_UPDATEOBJECT Meldung (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 3bd68ace-3ccf-446c-8cf9-52f42444674e
api_name:
- SFVM_UPDATEOBJECT
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 1e3c4ee64583710e84af0d377999c389f6fe1bfa6876bb150789a5fd118f79f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118452844"
---
# <a name="sfvm_updateobject-message"></a>SFVM \_ UPDATEOBJECT-Meldung

Aktualisiert ein -Objekt, indem ein Zeiger auf ein Array von zwei Zeigern auf Elementbezeichnerlisten (PIDLs) übergeben wird. Wird von [**SHShellFolderView \_ Message**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message)verwendet.


```C++

                SFVM_UPDATEOBJECT 

    lParam = (LPARAM*) ppidl;

            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppidl* \[ In\]
</dt> <dd>

Die Adresse eines Arrays mit zwei PIDLs. Die erste PIDL ist die alte PIDL. Das zweite ist eine Kopie der alten PIDL mit aktualisierten Informationen. Die Kontrolle über die Lebensdauer der Kopie gehört nach erfolgreichem Abschluss dieses Aufrufs zur Ansicht.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die Listview-ID des aktualisierten Objekts zurück, wenn das Update erfolgreich war. andernfalls wird -1 zurückgegeben.

## <a name="remarks"></a>Hinweise

Wenn das Update nicht erfolgreich war, muss der Aufrufer den Arbeitsspeicher freigeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 




