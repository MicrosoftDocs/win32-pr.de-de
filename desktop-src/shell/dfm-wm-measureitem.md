---
description: Wird an das Besitzerfenster eines Steuerelements oder Menüelements gesendet, wenn das Steuerelement oder Menü erstellt wird.
ms.assetid: 4584a3da-6c92-4ecd-8cf2-e4afc1b8321d
title: DFM_WM_MEASUREITEM Meldung (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e7ad0d39a56f598a8ef4773c70f4f438388e91a2154b3083fdf85a1ebebec22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117860898"
---
# <a name="dfm_wm_measureitem-message"></a>DFM \_ WM \_ MEASUREITEM-Meldung

Wird an das Besitzerfenster eines Steuerelements oder Menüelements gesendet, wenn das Steuerelement oder Menü erstellt wird.


```C++
DFM_WM_MEASUREITEM 

    wParam = (WPARAM);

    lParam = (LPARAM)(LPMEASUREITEMSTRUCT) lpMeasureItem;

            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* \[ In\]
</dt> <dd>

Der Wert des **CtlID-Members** der [**MEASUREITEMSTRUCT-Struktur,**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) auf den der *lpMeasureItem-Parameter* zeigt. Dieser Wert identifiziert das Steuerelement, das die **DFM \_ WM \_ MEASUREITEM-Nachricht** gesendet hat.

</dd> <dt>

*lpMeasureItem* \[ out\]
</dt> <dd>

Ein Zeiger auf eine [**MEASUREITEMSTRUCT-Struktur,**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) die die Dimensionen des vom Besitzer gezeichneten Steuerelements oder Menüelements enthält.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Wenn das Besitzerfenster die **DFM \_ WM \_ MEASUREITEM-Nachricht** empfängt, füllt der Besitzer die [**MEASUREITEMSTRUCT-Struktur**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) aus, auf die der *lpMeasureItem-Parameter* der Nachricht zeigt, und gibt zurück. Dadurch wird das System über die Dimensionen des Steuerelements informiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 
