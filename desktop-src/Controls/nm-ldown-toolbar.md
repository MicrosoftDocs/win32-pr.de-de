---
title: NM_LDOWN (Symbolleisten-) Benachrichtigungs Code (kommstrg. h)
description: Benachrichtigt das übergeordnete Fenster einer Symbolleiste, dass die linke Maustaste gedrückt wurde. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: f5b356fb-265b-4eb0-a5a3-2a22d688f847
keywords:
- NM_LDOWN (Symbolleiste) Benachrichtigungs Code Windows-Steuerelemente
topic_type:
- apiref
api_name:
- NM_LDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e60f1f05d85aa8885acf31a36098056d68612ba2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858641"
---
# <a name="nm_ldown-toolbar-notification-code"></a>NM- \_ ldown-Benachrichtigungs Code (Symbolleiste)

Benachrichtigt das übergeordnete Fenster einer Symbolleiste, dass die linke Maustaste gedrückt wurde. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
NM_LDOWN

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

## <a name="remarks"></a>Bemerkungen

Diese Benachrichtigung wird gesendet, nachdem der Benachrichtigungs Code für die [TBN- \_ Dropdown](tbn-dropdown.md) Liste gesendet wurde.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





