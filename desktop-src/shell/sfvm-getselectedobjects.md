---
description: Ruft ein Array von Zeigern auf elementbezeichnerlisten (pidls) für alle ausgewählten Objekte ab. Wird von der shshellfolderview- \_ Nachricht verwendet.
title: SFVM_GETSELECTEDOBJECTS Meldung (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 9639fbb6-d0ef-49b1-b3c5-e6a1dee0b7ad
api_name:
- SFVM_GETSELECTEDOBJECTS
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 056a9bd6bea78ef5093f6654b9935eb90e3759ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868696"
---
# <a name="sfvm_getselectedobjects-message"></a>Sfvm \_ getSelectedObjects-Meldung

Ruft ein Array von Zeigern auf elementbezeichnerlisten (pidls) für alle ausgewählten Objekte ab. Wird von der [**shshellfolderview- \_ Nachricht**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message)verwendet.


```C++
SFVM_GETSELECTEDOBJECTS 

    lParam = (LPARAM*) ppidl;

            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppidl* \[ vorgenommen\]
</dt> <dd>Die Adresse eines Arrays von pidls der aktuell ausgewählten Objekte.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die Anzahl der Elemente im Array zurück.

## <a name="remarks"></a>Bemerkungen

Wenn Sie fertig sind, sollten Sie für jedes Element des Arrays [**ilfree**](/windows/desktop/api/shlobj_core/nf-shlobj_core-ilfree) abrufen, um den Arbeitsspeicher freizugeben.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 




