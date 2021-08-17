---
description: Ruft das Handle für die Autohide-Appbar ab, die einem Bildschirmrand zugeordnet ist. Wenn das System über mehrere Monitore verfügt, wird der Monitor verwendet, der die primäre Taskleiste enthält.
title: ABM_GETAUTOHIDEBAR (Shellapi.h)
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
ms.openlocfilehash: 5ce38caf8cc1ad39e682aa8650e08e4860a3406e33669008d6ceee65e0416149
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118051152"
---
# <a name="abm_getautohidebar-message"></a>ABM \_ GETAUTOHIDEBAR-Nachricht

Ruft das Handle für die Autohide-Appbar ab, die einem Bildschirmrand zugeordnet ist. Wenn das System über mehrere Monitore verfügt, wird der Monitor verwendet, der die primäre Taskleiste enthält.

> [!Note]  
> Verwenden Sie [**ABM \_ GETAUTOHIDEBAREX,**](abm-getautohidebarex.md)um eine Appbar automatisch auf einem bestimmten Monitor zu abfragen.

 


```C++
hwndAutoHide = (HWND) SHAppBarMessage(ABM_GETAUTOHIDEBAR, pabd);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pabd* 
</dt> <dd>

Ein Zeiger auf eine [**APPBARDATA-Struktur,**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) die den Bildschirmrand angibt. Sie müssen die **CbSize- und** **uEdge-Member** angeben, wenn Sie diese Nachricht senden. alle anderen Member werden ignoriert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt das Handle an die Automatischhide-Appbar zurück. Der Rückgabewert ist **NULL,** wenn ein Fehler auftritt oder dem angegebenen Edge keine App-Leiste für die automatischeHide zugeordnet ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Shellapi.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ABM \_ SETAUTOHIDEBAR**](abm-setautohidebar.md)
</dt> <dt>

[**ABM \_ GETAUTOHIDEBAREX**](abm-getautohidebarex.md)
</dt> <dt>

[**ABM \_ SETAUTOHIDEBAREX**](abm-setautohidebarex.md)
</dt> </dl>

 

 




