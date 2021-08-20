---
description: IUserIdentityManager wird nicht unterstützt und kann in Zukunft geändert oder nicht mehr verfügbar sein. Verwenden Sie stattdessen Benutzerkonten mit schnellem Benutzerwechsel und Remotedesktop.
ms.assetid: 3d24b858-bbaf-455c-83cd-3f6f93aba2a8
title: IUserIdentityManager-Schnittstelle (Msident.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentityManager
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 3181677df73d2976853d373c2ec4b9ec24d321151598bf77acdc4ffbaa17508f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118049563"
---
# <a name="iuseridentitymanager-interface"></a>IUserIdentityManager-Schnittstelle

\[**IUserIdentityManager** wird nicht unterstützt und kann in Zukunft geändert oder nicht mehr verfügbar sein. Verwenden Sie stattdessen [Benutzerkonten mit schnellem Benutzerwechsel und Remotedesktop](fastuserswitching.md).\]

Macht Methoden verfügbar, die Benutzeridentitäten im System identifizieren, aufzählen und verwalten.

## <a name="members"></a>Member

Die **IUserIdentityManager-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IUserIdentityManager** verfügt auch über diese Membertypen:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IUserIdentityManager-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                  | Beschreibung                                                                                                                                                             |
|:------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EnumIdentities**](iuseridentitymanager-enumidentities.md)           | Veraltet. Ruft ein [**IEnumUserIdentity-Objekt**](ienumuseridentity.md) ab, das zum Aufzählen der im System vorhanden benutzeridentitäten verwendet werden kann.<br/> |
| [**GetIdentityByCookie**](iuseridentitymanager-getidentitybycookie.md) | Veraltet. Ruft eine bestimmte Benutzeridentität durch das Cookie ab, das zum eindeutigen Identifizieren verwendet wird.<br/>                                                                        |
| [**Abmelden**](iuseridentitymanager-logoff.md)                           | Veraltet. Melden Sie sich von der aktuellen Identität ab.<br/>                                                                                                                    |
| [**Anmelden**](iuseridentitymanager-logon.md)                             | Veraltet. Zeigt dem Benutzer eine Benutzeroberfläche an, über die der Benutzer eine Benutzeridentität auswählen kann. Bei erfolgreicher Anmeldung wird die Benutzeridentität angemeldet und abgerufen.<br/>        |
| [**ManageIdentities**](iuseridentitymanager-manageidentities.md)       | Veraltet. Zeigt dem Benutzer eine Benutzeroberfläche an, die es dem Benutzer ermöglicht, Benutzeridentitäten zu verwalten.<br/>                                                                          |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                             |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| Ende des Supports (Client)<br/>    | Windows 2000 Professional<br/>                                                   |
| Ende des Supports (Server)<br/>    | Windows 2000 Server<br/>                                                         |
| Header<br/>                   | <dl> <dt>Msident.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Msident.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Msident.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IUserIdentity**](iuseridentity.md)
</dt> <dt>

[**IUserIdentity2**](iuseridentity2.md)
</dt> <dt>

[**IEnumUserIdentity**](ienumuseridentity.md)
</dt> <dt>

[**IIdentityChangeNotify**](iidentitychangenotify.md)
</dt> </dl>

 

 
