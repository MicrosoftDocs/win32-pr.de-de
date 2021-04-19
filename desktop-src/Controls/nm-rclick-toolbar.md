---
title: NM_RCLICK (Symbolleisten-) Benachrichtigungs Code (kommstrg. h)
description: Wird von einem ToolBar-Steuerelement gesendet, wenn der Benutzer mit der rechten Maustaste auf die Symbolleiste klickt. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: e9d2d871-e922-444d-a76c-e73f249ed410
keywords:
- NM_RCLICK (Symbolleiste) Benachrichtigungs Code Windows-Steuerelemente
topic_type:
- apiref
api_name:
- NM_RCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6464c30a031aa55aef94bccd3ab852720fb14403
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106343071"
---
# <a name="nm_rclick-toolbar-notification-code"></a>NM \_ rclick-Benachrichtigungs Code (Symbolleiste)

Wird von einem ToolBar-Steuerelement gesendet, wenn der Benutzer mit der rechten Maustaste auf die Symbolleiste klickt. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
NM_RCLICK

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



 

 





