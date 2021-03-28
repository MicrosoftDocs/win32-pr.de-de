---
description: Registriert oder hebt die Registrierung einer appbar zum automatischen Ausblenden für eine bestimmte Bildschirm Kante auf. Wenn das System über mehrere Monitore verfügt, wird der Monitor verwendet, der die primäre Taskleiste enthält.
title: ABM_SETAUTOHIDEBAR Meldung (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 0cbd6c9c-e83f-41f8-91ed-81afaa24f524
api_name:
- ABM_SETAUTOHIDEBAR
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 53ca89008dda1233d12a7f0a9588803776ba1181
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977449"
---
# <a name="abm_setautohidebar-message"></a>ABM- \_ Meldung "logdehidebar"

Registriert oder hebt die Registrierung einer appbar zum automatischen Ausblenden für eine bestimmte Bildschirm Kante auf. Wenn das System über mehrere Monitore verfügt, wird der Monitor verwendet, der die primäre Taskleiste enthält.

> [!Note]  
> Verwenden Sie zum Registrieren oder Aufheben der Registrierung einer appbar für das automatische Ausblenden eines bestimmten Monitors [**ABM \_**](abm-setautohidebarex.md).

 


```C++
fSuccess = (BOOL) SHAppBarMessage(ABM_SETAUTOHIDEBAR, pabd); 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pabd* 
</dt> <dd>

Ein Zeiger auf eine [**appbardata**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) -Struktur. Legen Sie den **LPARAM** -Member auf " **true** " fest, um die appbar **zu registrieren** Sie müssen die Member **CBSIZE**, **HWND**, **uedge** und **LPARAM** angeben, wenn diese Nachricht gesendet wird. alle anderen Member werden ignoriert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, oder **false** , wenn ein Fehler auftritt oder wenn eine APP-Leiste zum automatischen Ausblenden für den angegebenen Edge bereits registriert ist.

## <a name="remarks"></a>Bemerkungen

Das System lässt nur eine automatische Ausblend-appbar für jeden Bildschirmrand zu. Dies wird bestimmt, wenn der Member **uedge** der [**appbardata**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) -Struktur festgelegt wird.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Shellapi. h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ABM-Bild-auf \_**](abm-getautohidebar.md)
</dt> <dt>

[**ABM \_ getautohidebarex**](abm-getautohidebarex.md)
</dt> <dt>

[**ABM \_ .**](abm-setautohidebarex.md)
</dt> </dl>

 

 




