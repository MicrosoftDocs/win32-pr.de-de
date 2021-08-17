---
title: RAS_USER_0 -Struktur (Rassapi.h)
description: Die RAS \_ USER \_ 0-Struktur wird in den Funktionen RasAdminUserSetInfo und RasAdminUserGetInfo verwendet, um Informationen zu einem Benutzer anzugeben.
ms.assetid: a2d4a935-f46d-4bc2-ada8-beaa3ac74834
keywords:
- RAS_USER_0 Ras-Struktur
- PRAS_USER_0 Strukturzeiger RAS
topic_type:
- apiref
api_name:
- RAS_USER_0
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbb4b04ddf3b81d330825b3333899e149d2f7b0d1f30c19106c6977e5291846f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117789141"
---
# <a name="ras_user_0-structure"></a>RAS \_ USER \_ 0-Struktur

\[Diese Version der **RAS \_ USER \_ 0-Struktur** wird ab Windows Vista nicht mehr unterstützt. Verwenden Sie stattdessen den [**neueren RAS \_ USER \_ 0,**](/windows/desktop/api/Mprapi/ns-mprapi-ras_user_0) der in mprapi.h definiert ist.\]

Die **RAS \_ USER \_ 0-Struktur** wird in den [**Funktionen RasAdminUserSetInfo**](rasadminusersetinfo.md) und [**RasAdminUserGetInfo**](rasadminusergetinfo.md) verwendet, um Informationen zu einem Benutzer anzugeben.

## <a name="syntax"></a>Syntax


```C++
typedef struct _RAS_USER_0 {
  BYTE  bfPrivilege;
  WCHAR szPhoneNumber[RASSAPI_MAX_PHONENUMBER_SIZE + 1];
} RAS_USER_0, *PRAS_USER_0;
```



## <a name="members"></a>Member

<dl> <dt>

**bfPrivilege**
</dt> <dd>

Ein Satz von Bitflags, die die RAS-Berechtigungen des Benutzers angeben. Dieser Member kann eine Kombination aus dem RASPRIV \_ DialinPrivilege-Flag und einem der Rückrufflags sein. Verwenden Sie die RASPRIV CallbackType-Maske, um den Typ der Rückrufberechtigung zu identifizieren, \_ die dem Benutzer bereitgestellt wird. Die folgenden Flags sind definiert.



| Wert                                                                                                                                                                                                                                         | Bedeutung                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="RASPRIV_NoCallback"></span><span id="raspriv_nocallback"></span><span id="RASPRIV_NOCALLBACK"></span><dl> <dt>**RASPRIV \_ NoCallback**</dt> </dl>                             | Der Benutzer verfügt über keine Rückrufberechtigung.<br/>                                               |
| <span id="RASPRIV_AdminSetCallback"></span><span id="raspriv_adminsetcallback"></span><span id="RASPRIV_ADMINSETCALLBACK"></span><dl> <dt>**RASPRIV \_ AdminSetCallback**</dt> </dl>     | Das Benutzerkonto ist so konfiguriert, dass der Administrator die Rückrufnummer festgelegt hat.<br/> |
| <span id="RASPRIV_CallerSetCallback"></span><span id="raspriv_callersetcallback"></span><span id="RASPRIV_CALLERSETCALLBACK"></span><dl> <dt>**RASPRIV \_ CallerSetCallback**</dt> </dl> | Der Remotebenutzer kann beim Einwählen eine Rückruf-Telefonnummer angeben.<br/>              |
| <span id="RASPRIV_DialinPrivilege"></span><span id="raspriv_dialinprivilege"></span><span id="RASPRIV_DIALINPRIVILEGE"></span><dl> <dt>**RASPRIV \_ DialinPrivilege**</dt> </dl>         | Der Benutzer hat die Berechtigung, sich bei diesem Server einwählen zu können.<br/>                                 |



 

Geben Sie eines der Rückrufflags im Aufruf der [**RasAdminUserSetInfo-Funktion**](rasadminusersetinfo.md) an.

</dd> <dt>

**szPhoneNumber**
</dt> <dd>

Eine auf NULL beendete Unicode-Zeichenfolge, die die Rückruftelefonnummer für den Benutzer angibt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                                                |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                       |
| Header<br/>                   | <dl> <dt>Rassapi.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Ras-Dienst (RAS): Übersicht](about-remote-access-service.md)
</dt> <dt>

[RAS-Serververwaltungsstrukturen](ras-server-administration-structures.md)
</dt> <dt>

[**RasAdminUserGetInfo**](rasadminusergetinfo.md)
</dt> <dt>

[**RasAdminUserSetInfo**](rasadminusersetinfo.md)
</dt> </dl>

 

 





