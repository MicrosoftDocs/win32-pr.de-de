---
description: Aktualisiert ein Objekt durch Übergabe eines Zeigers auf ein Array von zwei Zeigern auf Element Bezeichner Listen (pidls). Wird von der shshellfolderview- \_ Nachricht verwendet.
title: SFVM_UPDATEOBJECT Meldung (shlobj. h)
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
ms.openlocfilehash: 4367551cdf2d48a06c633329ad850c3f7c2e0976
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218581"
---
# <a name="sfvm_updateobject-message"></a>Sfvm- \_ UpdateObject-Nachricht

Aktualisiert ein Objekt durch Übergabe eines Zeigers auf ein Array von zwei Zeigern auf Element Bezeichner Listen (pidls). Wird von der [**shshellfolderview- \_ Nachricht**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message)verwendet.


```C++

                SFVM_UPDATEOBJECT 

    lParam = (LPARAM*) ppidl;

            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppidl* \[ in\]
</dt> <dd>

Die Adresse eines Arrays mit zwei pidls. Die erste PIDL ist die alte PIDL. Die zweite ist eine Kopie der alten PIDL mit aktualisierten Informationen. Die Kontrolle über die Lebensdauer des Kopiervorgangs gehört der Ansicht nach erfolgreichem Abschluss dieses Aufrufens an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die ListView-ID des aktualisierten Objekts zurück, wenn das Update erfolgreich war. Andernfalls wird-1 zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Wenn das Update nicht erfolgreich war, muss der Aufrufer den Arbeitsspeicher freigeben.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 




