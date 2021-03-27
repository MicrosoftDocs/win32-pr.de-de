---
description: 'Benachrichtigt das Rückruf Objekt, dass die Statusleiste aktualisiert wird. Wird von ishellfolderviewcb:: messagesfvcb verwendet.'
title: SFVM_UPDATESTATUSBAR Meldung (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: f1bac364-1011-4308-8b9b-8ed1800dd30d
api_name:
- SFVM_UPDATESTATUSBAR
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 14045c797d7292099c1c7b2c67f5958609d8d6b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104994814"
---
# <a name="sfvm_updatestatusbar-message"></a>Sfvm \_ updatestatusbar-Meldung

Benachrichtigt das Rückruf Objekt, dass die Statusleiste aktualisiert wird. Wird von [**ishellfolderviewcb:: messagesfvcb**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)verwendet.


```C++
SFVM_UPDATESTATUSBAR 

    wParam = (WPARAM)(BOOL) fInitialize;

            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*finitialize* \[ in\]
</dt> <dd>

Ein **boolescher** Wert, der auf **true** festgelegt wird, wenn die Statusleiste initialisiert wird.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn Sie diese Benachrichtigung erhalten:

-   Gibt "S OK" zurück, \_ Wenn Sie das Update verarbeiten.
-   Geben \_ Sie HRESULT (Schweregrad \_ erfolgreich, 0, 1) zurück, damit das Systemordner-Ansichts Objekt den Text der Statusleiste festlegen kann.
-   Return E \_ schlägt fehl, wenn das Ansichts Objekt des System Ordners die Statusleiste nicht verarbeiten kann.

Der Standardtext der Statusleiste lautet wie folgt.



| Status                      | Statusleistentext                         |
|-----------------------------|-----------------------------------------|
| Keine Elemente ausgewählt.           | " \# \# Objects" (im Ordner)          |
| Ein ausgewähltes Element           | Der Infotipp für das Element, falls verfügbar. |
| Es wurden mehrere Elemente ausgewählt. | " \# \# ausgewählte Objekte"                 |



 

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
