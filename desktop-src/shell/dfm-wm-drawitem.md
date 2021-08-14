---
description: Wird an das übergeordnete Fenster eines vom Besitzer gezeichneten Steuerelements oder Menüs gesendet, wenn sich ein visueller Aspekt des Steuerelements oder Menüs geändert hat.
ms.assetid: 2515bbab-025f-4f00-8564-a732d68edea3
title: DFM_WM_DRAWITEM Meldung (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7190d445490b581967c8dda67e170eb5db5665dfa59302313d7af736b275944d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118969469"
---
# <a name="dfm_wm_drawitem-message"></a>DFM \_ WM \_ DRAWITEM-Nachricht

Wird an das übergeordnete Fenster eines vom Besitzer gezeichneten Steuerelements oder Menüs gesendet, wenn sich ein visueller Aspekt des Steuerelements oder Menüs geändert hat.


```C++
DFM_WM_DRAWITEM 

    wParam = (WPARAM);

    lParam = (LPARAM)(LPDRAWITEMSTRUCT) lpDrawItem;

            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* \[ In\]
</dt> <dd>

Der Bezeichner des Steuerelements, das die **DFM \_ WM \_ DRAWITEM-Nachricht** gesendet hat. Wenn die Nachricht von einem Menü gesendet wurde, ist dieser Parameter 0 (null).

</dd> <dt>

*lpDrawItem* \[ out\]
</dt> <dd>

Ein Zeiger auf eine [**DRAWITEMSTRUCT-Struktur,**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) die Informationen über das zu zeichnende Element und den erforderlichen Zeichnungstyp enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn eine Anwendung diese Nachricht verarbeitet, sollte sie **TRUE** zurückgeben.

## <a name="remarks"></a>Hinweise

Der **itemAction-Member** der [**DRAWITEMSTRUCT-Struktur**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) gibt den Zeichnungsvorgang an, den eine Anwendung ausführen soll.

Vor dem Verarbeiten dieser Nachricht sollte eine Anwendung sicherstellen, dass sich der vom **hDC-Member** der [**DRAWITEMSTRUCT-Struktur**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) identifizierte Gerätekontext im Standardzustand befindet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 
