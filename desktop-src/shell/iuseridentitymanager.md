---
description: Iuseridentitymanager wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein. Verwenden Sie stattdessen Benutzerkonten mit schneller Benutzerumschaltung und Remotedesktop.
ms.assetid: 3d24b858-bbaf-455c-83cd-3f6f93aba2a8
title: Iuseridentitymanager-Schnittstelle (Msident. h)
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
ms.openlocfilehash: d0d00399e0ba958ef63c5e6597eb4a34387f92f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861783"
---
# <a name="iuseridentitymanager-interface"></a>Iuseridentitymanager-Schnittstelle

\[**Iuseridentitymanager** wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein. Verwenden Sie stattdessen [Benutzerkonten mit schneller Benutzerumschaltung und Remotedesktop](fastuserswitching.md).\]

Macht Methoden verfügbar, mit denen Benutzer Identitäten im System identifiziert, aufgelistet und verwaltet werden.

## <a name="members"></a>Member

Die **iuseridentitymanager** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Iuseridentitymanager** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **iuseridentitymanager** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                  | BESCHREIBUNG                                                                                                                                                             |
|:------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**-Eigenschaften**](iuseridentitymanager-enumidentities.md)           | Veraltet. Ruft ein [**ienumuseridentity**](ienumuseridentity.md) -Objekt ab, das verwendet werden kann, um die Benutzer Identitäten aufzulisten, die auf dem System vorhanden sind.<br/> |
| [**Getidentitybycookie**](iuseridentitymanager-getidentitybycookie.md) | Veraltet. Ruft eine bestimmte Benutzeridentität durch das Cookie ab, das zur eindeutigen Identifizierung verwendet wird.<br/>                                                                        |
| [**Abmeldung**](iuseridentitymanager-logoff.md)                           | Veraltet. Melden Sie sich von der aktuellen Identität ab.<br/>                                                                                                                    |
| [**Anmelden**](iuseridentitymanager-logon.md)                             | Veraltet. Zeigt dem Benutzer eine Benutzeroberfläche an und ermöglicht dem Benutzer die Auswahl einer Benutzeridentität. Bei erfolgreicher Ausführung wird die Benutzeridentität angemeldet und abgerufen.<br/>        |
| [**Manageidentities**](iuseridentitymanager-manageidentities.md)       | Veraltet. Zeigt dem Benutzer eine Benutzeroberfläche an und ermöglicht dem Benutzer die Verwaltung von Benutzer Identitäten.<br/>                                                                          |



 

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                             |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| Ende des Supports (Client)<br/>    | Windows 2000 Professional<br/>                                                   |
| Ende des Supports (Server)<br/>    | Windows 2000 Server<br/>                                                         |
| Header<br/>                   | <dl> <dt>Msident. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Msident. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Msident.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Iuseridentity**](iuseridentity.md)
</dt> <dt>

[**IUserIdentity2**](iuseridentity2.md)
</dt> <dt>

[**Iumumuseridentity**](ienumuseridentity.md)
</dt> <dt>

[**Iidentitychangenotify**](iidentitychangenotify.md)
</dt> </dl>

 

 
