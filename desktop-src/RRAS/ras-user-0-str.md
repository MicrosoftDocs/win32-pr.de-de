---
title: RAS_USER_0 Struktur (rassapi. h)
description: Die Struktur "RAS \_ User \_ 0" wird in den rasadminuserminfo-und rasadminusergetinfo-Funktionen verwendet, um Informationen zu einem Benutzer anzugeben.
ms.assetid: a2d4a935-f46d-4bc2-ada8-beaa3ac74834
keywords:
- RAS_USER_0 Struktur-RAS
- PRAS_USER_0-Struktur Zeiger RAS
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
ms.openlocfilehash: c79a6b946ed9d10cd2bfc989f8cde27fad2ffa92
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517717"
---
# <a name="ras_user_0-structure"></a>RAS \_ User \_ 0-Struktur

\[Diese Version der **RAS- \_ Benutzer- \_ 0** -Struktur wird ab Windows Vista nicht unterstützt. Verwenden Sie stattdessen den neueren [**RAS- \_ Benutzer \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_user_0) , der in MPRAPI. h definiert ist.\]

Die Struktur " **RAS \_ User \_ 0** " wird in den [**rasadminuserminfo**](rasadminusersetinfo.md) -und [**rasadminusergetinfo**](rasadminusergetinfo.md) -Funktionen verwendet, um Informationen zu einem Benutzer anzugeben.

## <a name="syntax"></a>Syntax


```C++
typedef struct _RAS_USER_0 {
  BYTE  bfPrivilege;
  WCHAR szPhoneNumber[RASSAPI_MAX_PHONENUMBER_SIZE + 1];
} RAS_USER_0, *PRAS_USER_0;
```



## <a name="members"></a>Member

<dl> <dt>

**BF-Berechtigung**
</dt> <dd>

Ein Satz von Bitflags, die die RAS-Berechtigungen des Benutzers angeben. Dieser Member kann eine Kombination aus dem raspriv \_ -Flag "dialinprivilege" und einem der rückgabeflags sein. Verwenden Sie die raspriv \_ CallbackType Mask, um den Typ der dem Benutzer bereitgestellten Rückruf Berechtigung zu identifizieren. Die folgenden Flags sind definiert.



| Wert                                                                                                                                                                                                                                         | Bedeutung                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="RASPRIV_NoCallback"></span><span id="raspriv_nocallback"></span><span id="RASPRIV_NOCALLBACK"></span><dl> <dt>**Raspriv \_ NoCallback**</dt> </dl>                             | Der Benutzer hat keine Rückruf Berechtigung.<br/>                                               |
| <span id="RASPRIV_AdminSetCallback"></span><span id="raspriv_adminsetcallback"></span><span id="RASPRIV_ADMINSETCALLBACK"></span><dl> <dt>**Raspriv \_ adminsetcallback**</dt> </dl>     | Das Benutzerkonto ist so konfiguriert, dass der Administrator die Rückrufnummer festgelegt hat.<br/> |
| <span id="RASPRIV_CallerSetCallback"></span><span id="raspriv_callersetcallback"></span><span id="RASPRIV_CALLERSETCALLBACK"></span><dl> <dt>**Raspriv \_ callersetcallback**</dt> </dl> | Der Remote Benutzer kann beim Einwählen eine Telefonnummer für den Rückruf angeben.<br/>              |
| <span id="RASPRIV_DialinPrivilege"></span><span id="raspriv_dialinprivilege"></span><span id="RASPRIV_DIALINPRIVILEGE"></span><dl> <dt>**Raspriv- \_ dialinprivilege**</dt> </dl>         | Der Benutzer verfügt über die Berechtigung zum Einwählen dieses Servers.<br/>                                 |



 

Geben Sie eines der rückgabeflags im aufrufsbefehl der [**rasadminusereintinfo**](rasadminusersetinfo.md) -Funktion an.

</dd> <dt>

**szphonenumber**
</dt> <dd>

Eine NULL-terminierte Unicode-Zeichenfolge, die die Rückruf Telefonnummer des Benutzers angibt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                                                |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                       |
| Header<br/>                   | <dl> <dt>Rassapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Remote Zugriffs Dienst (RAS) (Übersicht)](about-remote-access-service.md)
</dt> <dt>

[RAS-Server-Verwaltungsstrukturen](ras-server-administration-structures.md)
</dt> <dt>

[**Rasadminusergetinfo**](rasadminusergetinfo.md)
</dt> <dt>

[**Rasadminusereintinfo**](rasadminusersetinfo.md)
</dt> </dl>

 

 





