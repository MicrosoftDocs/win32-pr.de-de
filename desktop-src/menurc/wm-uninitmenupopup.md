---
title: WM_UNINITMENUPOPUP Meldung (Winuser.h)
description: Wird gesendet, wenn ein Dropdownmenü oder Untermenü zerstört wurde.
ms.assetid: 06129d88-6cf9-4d55-b8eb-6f78994bc87a
keywords:
- WM_UNINITMENUPOPUP Meldung Menüs und andere Ressourcen
topic_type:
- apiref
api_name:
- WM_UNINITMENUPOPUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7356c0aa4aa62521d2ab998773d07b8aa1a107c92b541c556756a567d31a09a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971789"
---
# <a name="wm_uninitmenupopup-message"></a>WM \_ UNINITMENUPOPUP-Meldung

Wird gesendet, wenn ein Dropdownmenü oder Untermenü zerstört wurde.


```C++
#define WM_UNINITMENUPOPUP              0x0125
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Handle für das Menü

</dd> <dt>

*lParam* 
</dt> <dd>

Das Wort in hoher Reihenfolge identifiziert das Menü, das zerstört wurde. Derzeit kann dieser Parameter nur **MF \_ SYSMENU** (das Fenstermenü) sein.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Wenn eine Anwendung eine [**\_ WM-INITMENUPOPUP-Nachricht**](wm-initmenupopup.md) empfängt, empfängt sie eine **\_ WM-UNINITMENUPOPUP-Nachricht.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Referenz**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Menüs](menus.md)
</dt> </dl>

 

