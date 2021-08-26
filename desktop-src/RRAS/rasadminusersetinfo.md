---
title: RasAdminUserSetInfo-Funktion (Rassapi.h)
description: Die RasAdminUserSetInfo-Funktion legt die RAS-Berechtigungen und die Rückruftelefonnummer für einen angegebenen Benutzer fest.
ms.assetid: 5b049dfd-ecc8-47e4-82cc-71a875752714
keywords:
- RasAdminUserSetInfo-Funktion RAS
topic_type:
- apiref
api_name:
- RasAdminUserSetInfo
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51bc4b56b9aa606892002fbef0eda8036c45442c06ce06b8561afba57620b7a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028430"
---
# <a name="rasadminusersetinfo-function"></a>RasAdminUserSetInfo-Funktion

\[Diese Funktion wird nur aus Gründen der Abwärtskompatibilität mit Windows NT Server 4.0 bereitgestellt. Es wird ERROR \_ CALL NOT IMPLEMENTED auf Windows Server \_ \_ 2003 zurückgegeben. Anwendungen sollten die [**MprAdminUserSetInfo-Funktion**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusersetinfo) verwenden.\]

Die **RasAdminUserSetInfo-Funktion** legt die RAS-Berechtigungen und die Rückruftelefonnummer für einen angegebenen Benutzer fest.

## <a name="syntax"></a>Syntax


```C++
DWORD RasAdminUserSetInfo(
  _In_ const WCHAR       *lpszUserAccountServer,
  _In_ const WCHAR       *lpszUser,
  _In_ const PRAS_USER_0 pRasUser0
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lpszUserAccountServer* \[ In\]
</dt> <dd>

Zeiger auf eine auf NULL beendete Unicode-Zeichenfolge, die den Namen des primären Domänencontrollers oder Sicherungsdomänencontrollers angibt, der über die Benutzerkontodatenbank verfügt. Verwenden Sie [**die RasAdminGetUserAccountServer-Funktion,**](rasadmingetuseraccountserver.md) um diesen Servernamen zu erhalten.

</dd> <dt>

*lpszUser* \[ In\]
</dt> <dd>

Zeiger auf eine mit NULL beendete Unicode-Zeichenfolge, die den Namen des Benutzers angibt, für den RAS-Informationen festgelegt werden sollen.

</dd> <dt>

*pRasUser0* \[ In\]
</dt> <dd>

Zeiger auf die [**RAS \_ USER \_ 0-Struktur,**](ras-user-0-str.md) die die neuen RAS-Daten für den angegebenen Benutzer angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert ERROR \_ SUCCESS.

Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Fehlercodes sein.



| Wert                                                                                                           | BESCHREIBUNG                                                                                     |
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**FEHLER \_ UNGÜLTIGE \_ DATEN**</dt> </dl>             | Der *pRasUser0-Puffer* enthält ungültige Daten.<br/>                                        |
| <dl> <dt>**FEHLER: \_ \_ UNGÜLTIGE \_ RÜCKRUFNUMMER**</dt> </dl> | Die im *pRasUser0-Puffer angegebene* Rückrufnummer enthält ungültige Zeichen.<br/> |
| <dl> <dt>**NERR \_ BufTooSmall**</dt> </dl>               | Nicht genügend Arbeitsspeicher zum Ausführen dieser Funktion.<br/>                                        |



 

Es gibt keine erweiterten Fehlerinformationen für diese Funktion. Rufen Sie [**getLastError nicht auf.**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)

## <a name="remarks"></a>Hinweise

Beim Festlegen der RAS-Berechtigungen für einen Benutzer muss **das bfPrivilege-Mitglied** der [**RAS USER \_ \_ 0-Struktur**](ras-user-0-str.md) mindestens eines der Rückrufflags angeben. Legen Sie **bfPrivilege** beispielsweise auf RASPRIV \_ DialinPrivilege \| RASPRIV NoCallback fest, um die Berechtigungen eines Benutzers so zu festlegen, dass Einwahlberechtigungen, aber keine Rückrufberechtigungen zulässig \_ sind.

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

[**\_RAS-BENUTZER \_ 0**](ras-user-0-str.md)
</dt> <dt>

[**RasAdminGetUserAccountServer**](rasadmingetuseraccountserver.md)
</dt> <dt>

[**RasAdminUserGetInfo**](rasadminusergetinfo.md)
</dt> </dl>

 

