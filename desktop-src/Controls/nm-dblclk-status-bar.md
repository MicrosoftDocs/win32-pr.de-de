---
title: NM_DBLCLK (Statusleiste) Benachrichtigungs Code (kommstrg. h)
description: Benachrichtigt das übergeordnete Fenster eines Status leisten-Steuer Elements, dass der Benutzer die linke Maustaste im Steuerelement doppelt geklickt hat. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 4c02c76d-2bdb-48ef-aa8e-635d0e200eb1
keywords:
- NM_DBLCLK (Statusleiste) Windows-Steuerelemente für Benachrichtigungs Code
topic_type:
- apiref
api_name:
- NM_DBLCLK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28866effbc4143dc9d0d5a3800f88711c99f88db
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949417"
---
# <a name="nm_dblclk-status-bar-notification-code"></a>NM- \_ dblclk-Benachrichtigungs Code (Statusleiste)

Benachrichtigt das übergeordnete Fenster eines Status leisten-Steuer Elements, dass der Benutzer die linke Maustaste im Steuerelement doppelt geklickt hat. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
NM_DBLCLK
        
    LPNMMOUSE lpnm = (LPNMMOUSE) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**nmmouse**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) -Struktur, die zusätzliche Informationen zu dieser Benachrichtigung enthält. Der **dwitemspec** -Member enthält den Index des Abschnitts, auf den geklickt wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, um anzugeben, dass der Maus Klick behandelt wurde, und unterdrückt die Standard Verarbeitung durch das System. Gibt **false** zurück, um die Standard Verarbeitung des Click zuzulassen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





