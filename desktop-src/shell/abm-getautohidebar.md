---
description: Ruft das Handle für die automatisch Ausblend Ende appbar ab, die einem Bildschirmrand zugeordnet ist. Wenn das System über mehrere Monitore verfügt, wird der Monitor verwendet, der die primäre Taskleiste enthält.
title: ABM_GETAUTOHIDEBAR Meldung (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 545dd1d9-8cbb-4ff3-b871-4908ecac56db
api_name:
- ABM_GETAUTOHIDEBAR
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 979825a9dbc28a89e3579419542877faacbace45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128480"
---
# <a name="abm_getautohidebar-message"></a>ABM \_ getautohidebar-Meldung

Ruft das Handle für die automatisch Ausblend Ende appbar ab, die einem Bildschirmrand zugeordnet ist. Wenn das System über mehrere Monitore verfügt, wird der Monitor verwendet, der die primäre Taskleiste enthält.

> [!Note]  
> Verwenden Sie zum Abfragen eines automatischen Ausblenden der appbar eines bestimmten Monitors [**ABM \_ getautohidebarex**](abm-getautohidebarex.md).

 


```C++
hwndAutoHide = (HWND) SHAppBarMessage(ABM_GETAUTOHIDEBAR, pabd);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pabd* 
</dt> <dd>

Ein Zeiger auf eine [**appbardata**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) -Struktur, die den Bildschirmrand angibt. Sie müssen die Member **CBSIZE** und **uedge** angeben, wenn diese Nachricht gesendet wird. alle anderen Member werden ignoriert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt das Handle für die automatisch Ausblend-appbar zurück. Der Rückgabewert ist **null** , wenn ein Fehler auftritt oder wenn dem angegebenen Edge keine Automatisches Ausblenden-appbar zugeordnet ist.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Shellapi. h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ABM-Bild-auf \_**](abm-setautohidebar.md)
</dt> <dt>

[**ABM \_ getautohidebarex**](abm-getautohidebarex.md)
</dt> <dt>

[**ABM \_ .**](abm-setautohidebarex.md)
</dt> </dl>

 

 




