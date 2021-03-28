---
description: Ruft das Handle für die automatisch Ausblend Ende appbar ab, die einem Bildschirmrand zugeordnet ist. Diese Meldung erweitert "dem \_ getautohidebar", indem Sie einen bestimmten Monitor zur Verwendung in mehreren Überwachungssituationen angeben.
title: ABM_GETAUTOHIDEBAREX Meldung (shellapi. h)
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
ms.openlocfilehash: 2ef95739a1031efb199e6acd99686e0858a9630e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "104982972"
---
# <a name="abm_getautohidebarex-message"></a>ABM \_ getautohidebarex-Meldung

Ruft das Handle für die automatisch Ausblend Ende appbar ab, die einem Bildschirmrand zugeordnet ist. Diese Meldung erweitert " [**dem \_ getautohidebar**](abm-getautohidebar.md) ", indem Sie einen bestimmten Monitor zur Verwendung in mehreren Überwachungssituationen angeben.


```C++
hwndAutoHide = (HWND) SHAppBarMessage(ABM_GETAUTOHIDEBAR, pabd);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pabd* 
</dt> <dd>

Ein Zeiger auf eine [**appbardata**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) -Struktur, die den Bildschirmrand und-Monitor angibt. Sie müssen die Member **CBSIZE**, **uedge** und **RC** angeben, wenn diese Nachricht gesendet wird. alle anderen Member werden ignoriert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt das Handle für die automatisch Ausblend-appbar zurück. Der Rückgabewert ist **null** , wenn ein Fehler auftritt oder wenn dem angegebenen Rand des angegebenen Monitors keine Automatisches Ausblenden-appbar zugeordnet ist.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Shellapi. h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ABM \_ getautohidebar**](abm-getautohidebar.md)
</dt> <dt>

[**ABM-Bild-auf \_**](abm-setautohidebar.md)
</dt> <dt>

[**ABM \_ .**](abm-setautohidebarex.md)
</dt> </dl>

 

 




