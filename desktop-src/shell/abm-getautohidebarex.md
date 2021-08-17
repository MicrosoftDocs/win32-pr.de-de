---
description: Ruft das Handle der automatischen App-Leiste ab, die einem Bildschirmrand zugeordnet ist. Diese Meldung erweitert ABM \_ GETAUTOHIDEBAR, indem Sie einen bestimmten Monitor für die Verwendung in mehreren Überwachungssituationen angeben können.
title: ABM_GETAUTOHIDEBAREX Meldung (Shellapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 538EA230-06DF-4441-A6AA-9DD613521BE1
api_name:
- ABM_GETAUTOHIDEBAREX
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 9aecbc81e313c3d971b310cc35bd399b93cc18f2ef2a4f02a00d51a16745eb61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118225239"
---
# <a name="abm_getautohidebarex-message"></a>ABM \_ GETAUTOHIDEBAREX-Nachricht

Ruft das Handle der automatischen App-Leiste ab, die einem Bildschirmrand zugeordnet ist. Diese Meldung erweitert [**ABM \_ GETAUTOHIDEBAR,**](abm-getautohidebar.md) indem Sie einen bestimmten Monitor für die Verwendung in mehreren Überwachungssituationen angeben können.


```C++
hwndAutoHide = (HWND) SHAppBarMessage(ABM_GETAUTOHIDEBAR, pabd);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pabd* 
</dt> <dd>

Ein Zeiger auf eine [**APPBARDATA-Struktur,**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) die den Bildschirmrand und den Monitor angibt. Sie müssen die Member **cbSize,** **uEdge** und **rc** angeben, wenn Sie diese Nachricht senden. alle anderen Member werden ignoriert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt das Handle für die appbar autohide zurück. Der Rückgabewert ist **NULL,** wenn ein Fehler auftritt oder wenn keine automatische Appbar mit dem angegebenen Rand des angegebenen Monitors verknüpft ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Shellapi.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ABM \_ GETAUTOHIDEBAR**](abm-getautohidebar.md)
</dt> <dt>

[**ABM \_ SETAUTOHIDEBAR**](abm-setautohidebar.md)
</dt> <dt>

[**ABM \_ SETAUTOHIDEBAREX**](abm-setautohidebarex.md)
</dt> </dl>

 

 




