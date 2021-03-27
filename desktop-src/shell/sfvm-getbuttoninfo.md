---
description: 'Ermöglicht dem Rückruf Objekt das Hinzufügen von Schaltflächen zur Symbolleiste. Wird von ishellfolderviewcb:: messagesfvcb verwendet.'
title: SFVM_GETBUTTONINFO Meldung (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 983652ed-7309-46aa-a6c9-7516411ba5ac
api_name:
- SFVM_GETBUTTONINFO
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d0db40f7c1f54cd13d54765ba34a8eab31246809
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980225"
---
# <a name="sfvm_getbuttoninfo-message"></a>Sfvm \_ getbuttoninfo-Meldung

Ermöglicht dem Rückruf Objekt das Hinzufügen von Schaltflächen zur Symbolleiste. Wird von [**ishellfolderviewcb:: messagesfvcb**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)verwendet.


```C++
SFVM_GETBUTTONINFO 

    lParam = (LPARAM)(LPTBINFO) ptbinfo;

            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ptbinfo* \[ vorgenommen\]
</dt> <dd>

Die Adresse einer [**tbinfo**](/windows/desktop/api/Shlobj/ns-shlobj-tbinfo) -Struktur, die die Anzahl der Schaltflächen angibt, und wie Sie der Symbolleiste hinzugefügt werden sollen.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Schaltflächen können den standardmäßigen Systemordner Ansichts Objekt-Schaltflächen angefügt oder vorangestellt werden oder anstelle der Standard Schaltflächen angezeigt werden. Auf diese Nachricht folgt eine [**sfvm- \_ getButtons**](sfvm-getbuttons.md) -Meldung, die die Informationen zu den Details der Schaltfläche abruft.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
