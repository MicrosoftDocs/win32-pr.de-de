---
description: Wird an das übergeordnete Fenster eines von einem Besitzer gezeichneten Steuer Elements oder Menüs gesendet, wenn sich ein visueller Aspekt des Steuer Elements oder Menüs geändert hat.
ms.assetid: 2515bbab-025f-4f00-8564-a732d68edea3
title: DFM_WM_DRAWITEM Meldung (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67255fea5c39bebc995e5c53d90378536b12921b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977265"
---
# <a name="dfm_wm_drawitem-message"></a>DFM- \_ WM- \_ DrawItem-Nachricht

Wird an das übergeordnete Fenster eines von einem Besitzer gezeichneten Steuer Elements oder Menüs gesendet, wenn sich ein visueller Aspekt des Steuer Elements oder Menüs geändert hat.


```C++
DFM_WM_DRAWITEM 

    wParam = (WPARAM);

    lParam = (LPARAM)(LPDRAWITEMSTRUCT) lpDrawItem;

            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* \[ in\]
</dt> <dd>

Der Bezeichner des Steuer Elements, das die **DFM- \_ WM- \_ DrawItem** -Nachricht gesendet hat. Wenn die Nachricht von einem Menü gesendet wurde, ist dieser Parameter gleich 0 (null).

</dd> <dt>

*lpdrawitem* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine [**drawitemstruct**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) -Struktur, die Informationen über das zu zeichende Element und den Typ der erforderlichen Zeichnung enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie " **true**" zurückgeben.

## <a name="remarks"></a>Bemerkungen

Der **itemaction** -Member der [**drawitemstruct**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) -Struktur gibt den Zeichnungs Vorgang an, den eine Anwendung ausführen soll.

Vor der Rückgabe aus der Verarbeitung dieser Nachricht muss eine Anwendung sicherstellen, dass der vom **hdc** -Member der [**drawitemstruct**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) -Struktur identifizierte Gerätekontext den Standardstatus aufweist.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
