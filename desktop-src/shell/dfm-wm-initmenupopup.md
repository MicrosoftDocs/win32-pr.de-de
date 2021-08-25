---
description: 'DFM_WM_INITMENUPOPUP Meldung: Wird gesendet, wenn ein Dropdownmenü oder Untermenü aktiv wird. Dadurch kann eine Anwendung das Menü ändern, bevor es angezeigt wird, ohne das gesamte Menü zu ändern.'
title: DFM_WM_INITMENUPOPUP Meldung (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 314e83f7-839d-4ca0-b5c1-842c5bf14923
api_name:
- DFM_WM_INITMENUPOPUP
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 4cb68b8251fa383ae9386eae3e6753158330c4be7566f02a8758a72dfe05de03
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119943150"
---
# <a name="dfm_wm_initmenupopup-message"></a>DFM \_ WM \_ INITMENUPOPUP-Meldung

Wird gesendet, wenn ein Dropdownmenü oder Untermenü aktiv wird. Dadurch kann eine Anwendung das Menü ändern, bevor es angezeigt wird, ohne das gesamte Menü zu ändern.


```C++
DFM_WM_INITMENUPOPUP 

    wParam = (WPARAM);

    lParam = (LPARAM);

            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* \[ In\]
</dt> <dd>

Ein Handle für das Dropdownmenü oder untermenü.

</dd> <dt>

*lParam* \[ In\]
</dt> <dd>

Das Wort mit niedriger Reihenfolge gibt die nullbasierte relative Position des Menüelements an, das das Dropdownmenü oder Untermenü öffnet.

Das Wort in hoher Reihenfolge gibt an, ob das Dropdownmenü das Fenstermenü ist. Wenn das Menü das Fenstermenü ist, ist dieser Parameter **TRUE.** Andernfalls ist es **FALSE.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn eine Anwendung diese Nachricht verarbeitet, sollte sie 0 (null) zurückgeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 




