---
description: Veraltet. Stellt Benachrichtigungen zu Änderungen an Benutzeridentitäten im System sowie Benutzeranforderungen zum Wechseln der aktuellen Benutzeridentität bereit.
ms.assetid: 09903aa6-62bf-4820-9a09-79956d775441
title: IIdentityChangeNotify-Schnittstelle (Msident.h)
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
ms.openlocfilehash: 4419f55b2fe4561a22035d962da5e3c271108d06fa417cfbed1b603c883e5b32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118721908"
---
# <a name="iidentitychangenotify-interface"></a>IIdentityChangeNotify-Schnittstelle

\[Die **IIdentityChangeNotify-Schnittstelle** ist für die Verwendung in Windows 2000 verfügbar. In Windows XP wurde diese Funktion durch Benutzerkonten [mit schnellem Benutzerwechsel und Remotedesktop](fastuserswitching.md)ersetzt und kann in nachfolgenden Versionen geändert oder nicht verfügbar sein.\]

Veraltet. Stellt Benachrichtigungen zu Änderungen an Benutzeridentitäten im System sowie Benutzeranforderungen zum Wechseln der aktuellen Benutzeridentität bereit.

## <a name="members"></a>Member

Die **IIdentityChangeNotify-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IIdentityChangeNotify** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IIdentityChangeNotify-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                                 | Beschreibung                                                                                                                           |
|:---------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------|
| [**IdentityInformationChanged**](iidentitychangenotify-identityinformationchanged.md) | Veraltet. Wird aufgerufen, wenn Informationen zu einer Benutzeridentität geändert wurden oder wenn eine Benutzeridentität hinzugefügt oder gelöscht wurde.<br/>  |
| [**QuerySwitchIdentities**](iidentitychangenotify-queryswitchidentities.md)           | Veraltet. Wird aufgerufen, wenn der aktuelle Benutzer angefordert hat, dass seine Benutzeridentität gewechselt wird, aber bevor der Wechsel erfolgt.<br/> |
| [**SwitchIdentities**](iidentitychangenotify-switchidentities.md)                     | Veraltet. Wird aufgerufen, wenn Benutzeridentitäten gewechselt werden.<br/>                                                                      |



 

## <a name="remarks"></a>Hinweise

Um Benachrichtigungen zu implementieren, muss eine abgeleitete Schnittstelle eine Verbindung mit [**dem IUserIdentityManager**](iuseridentitymanager.md) herstellen, indem [**IConnectionPoint::Advise**](/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-advise) aufgerufen und ein Zeiger an die Schnittstelle übergeben wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                             |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Msident.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Msident.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Msoe.dll</dt> </dl>    |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IUserIdentityManager**](iuseridentitymanager.md)
</dt> <dt>

[**IConnectionPoint**](/windows/win32/api/ocidl/nn-ocidl-iconnectionpoint)
</dt> </dl>

 

 
