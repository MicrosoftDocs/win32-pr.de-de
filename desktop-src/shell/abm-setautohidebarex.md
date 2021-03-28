---
description: Registriert oder hebt die Registrierung einer appbar zum automatischen Ausblenden für eine bestimmte Bildschirm Kante auf. Diese Meldung erweitert ABM-Abbild-Abbild \_ , indem Sie einen bestimmten Monitor zur Verwendung in mehreren Monitor Situationen angeben können.
title: ABM_SETAUTOHIDEBAREX Meldung (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: C437727C-3FF6-4598-9D81-A39FCC2EF1C4
api_name:
- ABM_SETAUTOHIDEBAREX
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: ba4e1474d3b57465fa68446fd7ab787c9a62570b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "104996466"
---
# <a name="abm_setautohidebarex-message"></a>ABM-Nachricht "- \_ Abmeldung"

Registriert oder hebt die Registrierung einer appbar zum automatischen Ausblenden für eine bestimmte Bildschirm Kante auf. Diese Meldung erweitert [**ABM \_ -Abbild-Abbild**](abm-setautohidebar.md) , indem Sie einen bestimmten Monitor zur Verwendung in mehreren Monitor Situationen angeben können.


```C++
fSuccess = (BOOL) SHAppBarMessage(ABM_SETAUTOHIDEBAR, pabd); 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pabd* 
</dt> <dd>

Ein Zeiger auf eine [**appbardata**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) -Struktur. Legen Sie den **LPARAM** -Member auf " **true** " fest, um die appbar **zu registrieren** Sie müssen die Member **CBSIZE**, **HWND**, **uedge**, **RC** und **LPARAM** angeben, wenn diese Nachricht gesendet wird. alle anderen Member werden ignoriert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, oder **false** , wenn ein Fehler auftritt oder wenn für den angegebenen Edge für den angegebenen Monitor bereits eine appbar zum automatischen Ausblenden registriert ist.

## <a name="remarks"></a>Bemerkungen

Das System lässt nur eine automatisch Ausblend Ende appbar für jeden Rand jedes Monitors zu. Der Monitor wird durch das **RC** -Element bestimmt, und der Edge wird vom **uedge** -Member der [**appbardata**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) -Struktur bestimmt.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Shellapi. h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ABM \_ getautohidebar**](abm-getautohidebar.md)
</dt> <dt>

[**ABM \_ getautohidebarex**](abm-getautohidebarex.md)
</dt> <dt>

[**ABM-Bild-auf \_**](abm-setautohidebar.md)
</dt> </dl>

 

 




