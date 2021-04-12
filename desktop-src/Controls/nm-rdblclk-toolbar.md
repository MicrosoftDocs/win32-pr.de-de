---
title: NM_RDBLCLK (Symbolleisten-) Benachrichtigungs Code (kommstrg. h)
description: Benachrichtigt das übergeordnete Fenster eines Steuer Elements, dass der Benutzer die Rechte Maustaste im Steuerelement doppelt geklickt hat. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 0281a687-3f1c-4fc1-bf1d-19c7ac920cd3
keywords:
- NM_RDBLCLK (Symbolleiste) Benachrichtigungs Code Windows-Steuerelemente
topic_type:
- apiref
api_name:
- NM_RDBLCLK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dec2129b6400c60bd59e441ff8af2083e781ba22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478255"
---
# <a name="nm_rdblclk-toolbar-notification-code"></a>NM \_ rdblclk (Toolbar)-Benachrichtigungs Code

Benachrichtigt das übergeordnete Fenster eines Steuer Elements, dass der Benutzer die Rechte Maustaste im Steuerelement doppelt geklickt hat. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
NM_RDBLCLK

    lpnmmouse = (LPNMMOUSE) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**nmmouse**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) -Struktur, die Informationen zu diesem Benachrichtigungs Code enthält. Wenn auf ein Symbolleisten Element auf die Maus geklickt wurde, enthält das Element **dwitemspec** den Element Bezeichner, und der **dwitemdata** -Member enthält die Elementdaten. Wenn die Maus auf ein Trennzeichen oder Leerraum auf der Symbolleiste geklickt wurde, enthält das Element **dwitemspec** -1.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **false** zurück, damit das Symbolleisten-Steuerelement die Standard Verarbeitung des Ereignisses ausführen kann, oder **true** , um zu verhindern, dass das Steuerelement das Ereignis verarbeitet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





