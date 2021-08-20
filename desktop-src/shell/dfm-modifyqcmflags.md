---
description: Ermöglicht dem Rückruf, die an \_ IContextMenu::QueryContextMenu übergebenen CFM-XXX-Werte zu ändern.
title: DFM_MODIFYQCMFLAGS (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 2c87e14d-4cf4-425d-a5fe-9dc7530f0e59
api_name:
- DFM_MODIFYQCMFLAGS
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 62ce86426b31abfb6dec67d7ee45b01a8bc47ba10c40ce9ed00051dd414a0ffd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119223590"
---
# <a name="dfm_modifyqcmflags-message"></a>DFM \_ MODIFYQCMFLAGS-Meldung

Ermöglicht dem Rückruf, die an \_ [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu)übergebenen CFM-XXX-Werte zu ändern.


```C++
DFM_MODIFYQCMFLAGS

    lParam = (LPARAM)(UINT) *puNewFlags;

    wParam = (WPARAM)(UINT) uFlags;         

            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*puNewFlags* \[ In\]
</dt> <dd>

Ein Zeiger auf die neuen Flagwerte.

</dd> <dt>

*uFlags* \[ In\]
</dt> <dd>

Flags, die angeben, wie das Kontextmenü geändert werden kann. Dieser Parameter verwendet die \_ CMF-XXX-Werte, die in [**IContextMenu::QueryContextMenu beschrieben werden.**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu)

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 




