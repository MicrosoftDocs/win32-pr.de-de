---
description: Wird an das Besitzer Fenster eines Steuer Elements oder Menü Elements gesendet, wenn das Steuerelement oder das Menü erstellt wird.
ms.assetid: 4584a3da-6c92-4ecd-8cf2-e4afc1b8321d
title: DFM_WM_MEASUREITEM Meldung (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61c4ad79acf221ecaabf9060940ad2514422bef1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393437"
---
# <a name="dfm_wm_measureitem-message"></a>DFM- \_ WM- \_ MeasureItem-Meldung

Wird an das Besitzer Fenster eines Steuer Elements oder Menü Elements gesendet, wenn das Steuerelement oder das Menü erstellt wird.


```C++
DFM_WM_MEASUREITEM 

    wParam = (WPARAM);

    lParam = (LPARAM)(LPMEASUREITEMSTRUCT) lpMeasureItem;

            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* \[ in\]
</dt> <dd>

Der Wert des **ctlid** -Members der [**measureitemstruct**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) -Struktur, auf die durch den *lpmeasureitem* -Parameter verwiesen wird. Dieser Wert identifiziert das Steuerelement, das die **DFM- \_ WM- \_ MeasureItem** -Nachricht gesendet hat.

</dd> <dt>

*lpmeasureitem* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine [**measureitemstruct**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) -Struktur, die die Dimensionen des vom Besitzer gezeichneten Steuer Elements oder Menü Elements enthält.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn das Besitzer Fenster die **DFM- \_ WM- \_ MeasureItem** -Nachricht empfängt, füllt der Besitzer die [**measureitemstruct**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) -Struktur aus, auf die durch den *lpmeasureitem* -Parameter der Nachricht verwiesen wird, und gibt zurück. Dadurch wird das System über die Abmessungen des Steuer Elements informiert.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
