---
description: Veraltet. Ermöglicht das Benachrichtigen von Änderungen an Benutzer Identitäten im System sowie Benutzer Anforderungen zum Wechseln der aktuellen Benutzeridentität.
ms.assetid: 09903aa6-62bf-4820-9a09-79956d775441
title: Iidentitychangenotify-Schnittstelle (Msident. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IIdentityChangeNotify
api_type:
- COM
api_location:
- Msoe.dll
ms.openlocfilehash: 4a217b2cfb046bfb9ae5546e015264f74d00b1d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215931"
---
# <a name="iidentitychangenotify-interface"></a>Iidentitychangenotify-Schnittstelle

\[Die **iidentitychangenotify** -Schnittstelle ist für die Verwendung in Windows 2000 verfügbar. In Windows XP wurde diese Funktion durch [Benutzerkonten mit schneller Benutzerumschaltung und Remotedesktop](fastuserswitching.md)abgelöst und kann in nachfolgenden Versionen geändert oder nicht verfügbar sein.\]

Veraltet. Ermöglicht das Benachrichtigen von Änderungen an Benutzer Identitäten im System sowie Benutzer Anforderungen zum Wechseln der aktuellen Benutzeridentität.

## <a name="members"></a>Member

Die **iidentitychangenotify** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Iidentitychangenotify** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **iidentitychangenotifisierungsschnittstelle** verfügt über diese Methoden.



| Methode                                                                                 | BESCHREIBUNG                                                                                                                           |
|:---------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------|
| [**Identityinformationchanged**](iidentitychangenotify-identityinformationchanged.md) | Veraltet. Wird aufgerufen, wenn sich die Informationen zu einer Benutzeridentität geändert haben oder wenn eine Benutzeridentität hinzugefügt oder gelöscht wurde.<br/>  |
| [**Queryswitchidentities**](iidentitychangenotify-queryswitchidentities.md)           | Veraltet. Wird aufgerufen, wenn der aktuelle Benutzer angefordert hat, dass die Benutzeridentität gewechselt wird, jedoch bevor der Switch auftritt.<br/> |
| [**Switchidentities**](iidentitychangenotify-switchidentities.md)                     | Veraltet. Wird aufgerufen, wenn Benutzer Identitäten gewechselt werden.<br/>                                                                      |



 

## <a name="remarks"></a>Bemerkungen

Um Benachrichtigungen zu implementieren, muss eine abgeleitete Schnittstelle eine Verbindung mit dem [**iuseridentitymanager**](iuseridentitymanager.md) herstellen, indem [**IConnectionPoint:: Rat**](/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-advise) aufgerufen und ein Zeiger an die-Schnittstelle übergeben wird.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                             |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Msident. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Msident. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Msoe.dll</dt> </dl>    |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Iuseridentitymanager**](iuseridentitymanager.md)
</dt> <dt>

[**IConnectionPoint**](/windows/win32/api/ocidl/nn-ocidl-iconnectionpoint)
</dt> </dl>

 

 
