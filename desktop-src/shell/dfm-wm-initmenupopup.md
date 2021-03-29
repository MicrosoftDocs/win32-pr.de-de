---
description: Wird gesendet, wenn ein Dropdown Menü oder ein Untermenü aktiv werden soll. Dadurch kann eine Anwendung das Menü ändern, bevor es angezeigt wird, ohne das gesamte Menü zu ändern.
title: DFM_WM_INITMENUPOPUP Meldung (shlobj. h)
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
ms.openlocfilehash: 1c89731bdffc0e7d902e6c83b9a4f208134b7cfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128452"
---
# <a name="dfm_wm_initmenupopup-message"></a>DFM- \_ WM- \_ initmenupopup-Meldung

Wird gesendet, wenn ein Dropdown Menü oder ein Untermenü aktiv werden soll. Dadurch kann eine Anwendung das Menü ändern, bevor es angezeigt wird, ohne das gesamte Menü zu ändern.


```C++
DFM_WM_INITMENUPOPUP 

    wParam = (WPARAM);

    lParam = (LPARAM);

            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* \[ in\]
</dt> <dd>

Ein Handle für das Dropdown Menü oder Untermenü.

</dd> <dt>

*LPARAM* \[ in\]
</dt> <dd>

Das nieder wertige Wort gibt die null basierte relative Position des Menü Elements an, das das Dropdown Menü oder Untermenü öffnet.

Das höchst wertige Wort gibt an, ob das Dropdown Menü das Fenstermenü ist. Wenn das Menü das Menü "Fenster" ist, ist dieser Parameter " **true**". Andernfalls ist Sie **false**.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 




