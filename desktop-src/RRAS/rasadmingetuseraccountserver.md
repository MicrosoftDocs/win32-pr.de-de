---
title: RasAdminGetUserAccountServer-Funktion (Rassapi.h)
description: Die RasAdminGetUserAccountServer-Funktion ruft den Namen des Servers ab, der über die Benutzerkontodatenbank verfügt. Verwenden Sie den zurückgegebenen Servernamen in den Funktionen RasAdminUserGetInfo und RasAdminUserSetInfo, um Informationen zu einem angegebenen Benutzer zu erhalten oder festzulegen.
ms.assetid: db91aa48-32af-49ac-87ed-8c484926ca15
keywords:
- RasAdminGetUserAccountServer-Funktion RAS
topic_type:
- apiref
api_name:
- RasAdminGetUserAccountServer
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f2ac4052ad4638c3e0e2483adb68857f4c2b670322434107d93100b6a177855
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028540"
---
# <a name="rasadmingetuseraccountserver-function"></a>RasAdminGetUserAccountServer-Funktion

\[Diese Funktion wird nur aus Gründen der Abwärtskompatibilität mit Windows NT Server 4.0 bereitgestellt. Es wird ERROR \_ CALL NOT IMPLEMENTED auf Windows Server \_ \_ 2003 zurückgegeben. Anwendungen sollten die [**MprAdminGetPDCServer-Funktion**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetpdcserver) verwenden.\]

Die **RasAdminGetUserAccountServer-Funktion** ruft den Namen des Servers ab, der über die Benutzerkontodatenbank verfügt. Verwenden Sie den zurückgegebenen Servernamen in den [**Funktionen RasAdminUserGetInfo**](rasadminusergetinfo.md) und [**RasAdminUserSetInfo,**](rasadminusersetinfo.md) um Informationen zu einem angegebenen Benutzer zu erhalten oder festzulegen.

## <a name="syntax"></a>Syntax


```C++
DWORD RasAdminGetUserAccountServer(
  _In_  const WCHAR  *lpszDomain,
  _In_  const WCHAR  *lpszServer,
  _Out_       LPWSTR lpszUserAccountServer
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lpszDomain* \[ In\]
</dt> <dd>

Zeiger auf eine mit **NULL beendete** Unicode-Zeichenfolge, die den Namen der Domäne angibt, zu der der RAS-Server gehört. Dieser Parameter ist **NULL für** die RAS-Verwaltungsanwendungen, die auf Arbeitsstationen oder Servern ausgeführt werden, die nicht Mitglied einer Domäne sind. Wenn dieser Parameter **NULL ist,** muss *der lpszServer-Parameter* nicht NULL **sein.**

</dd> <dt>

*lpszServer* \[ In\]
</dt> <dd>

Zeiger auf eine mit **NULL beendete** Unicode-Zeichenfolge, die den Namen des RAS-Servers angibt. Geben Sie den Namen mit den \\ \\ führenden Zeichen " " im folgenden Formular an: \\ \\ *Servername*. Dieser Parameter kann NULL **sein,** wenn *der lpszDomain-Parameter* nicht **NULL ist.**

</dd> <dt>

*lpszUserAccountServer* \[ out\]
</dt> <dd>

Zeiger auf einen Puffer, der eine mit **NULL** beendete Unicode-Zeichenfolge empfängt, die den Namen eines Domänencontrollers angibt, der über die Benutzerkontodatenbank verfügt. Der Puffer sollte groß genug sein, um den Servernamen zu halten (WAITN +1). Die -Funktion präfixiert den zurückgegebenen Servernamen mit führenden ""-Zeichen \\ \\ im folgenden Formular: \\ \\ *Servername*.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert ERROR \_ SUCCESS.

Wenn die Funktion fehlschlägt, kann der Rückgabewert der folgende Fehlercode sein.



| Wert                                                                                                    | Bedeutung                                                     |
|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <dt>**FEHLER \_ UNGÜLTIGER \_ PARAMETER**</dt> </dl> | Sowohl *lpszDomain als* *auch lpszServer sind* **NULL.**<br/> |



 

Es gibt keine erweiterten Fehlerinformationen für diese Funktion. Rufen Sie [**getLastError nicht auf.**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)

## <a name="remarks"></a>Hinweise

Die **RasAdminGetUserAccountServer-Funktion** erhält den Namen des Servers mit der Benutzerkontendatenbank. Diese Funktion erfordert den Namen des RAS-Servers oder den Namen der Domäne, in der sich der RAS-Server befindet.

Der *lpszDomain-Parameter* sollte einen gültigen Domänennamen angeben. Dieser Parameter ist **NULL für** RAS-Verwaltungsanwendungen, die auf Servern ausgeführt werden, die keine Mitglieder einer Domäne sind (z. B. befindet sich der Server in einer eigenen Arbeitsgruppe). In diesem Fall muss der *lpszServer-Parameter* den Servernamen angeben. Um den Servernamen zu erhalten, rufen Sie die [**GetComputerName-Funktion**](/windows/win32/api/winbase/nf-winbase-getcomputernamea) auf. Stellen Sie sicher, dass Sie dem Servernamen die Zeichen " \\ \\ " vorangestellt haben.

Wenn der von *lpszServer* angegebene Servername ein eigenständiger Server ist (d. h., der Server oder die Arbeitsstation ist kein Mitglied einer Domäne), wird der Servername selbst im *puffer lpszUserAccountServer* zurückgegeben.

Verwenden Sie dann den Namen des Benutzerkontoservers in einem Aufruf der [**NetQueryDisplayInformation-Funktion,**](/windows/win32/api/lmaccess/nf-lmaccess-netquerydisplayinformation) um die Benutzer in der Benutzerkontodatenbank aufzählen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows 2000 Professional<br/>                                                   |
| Ende des Supports (Server)<br/> | Windows 2000 Server<br/>                                                         |
| Header<br/>                | <dl> <dt>Rassapi.h</dt> </dl>   |
| Bibliothek<br/>               | <dl> <dt>Rassapi.lib</dt> </dl> |
| DLL<br/>                   | <dl> <dt>Rassapi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Ras-Dienst (RAS): Übersicht](about-remote-access-service.md)
</dt> <dt>

[RAS-Serververwaltungsfunktionen](ras-server-administration-functions.md)
</dt> <dt>

[**GetComputerName**](/windows/win32/api/winbase/nf-winbase-getcomputernamea)
</dt> <dt>

[**RasAdminUserGetInfo**](rasadminusergetinfo.md)
</dt> <dt>

[**RasAdminUserSetInfo**](rasadminusersetinfo.md)
</dt> </dl>

 

