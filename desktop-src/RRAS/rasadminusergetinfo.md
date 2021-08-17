---
title: RasAdminUserGetInfo-Funktion (Rassapi.h)
description: Die RasAdminUserGetInfo-Funktion ruft die RAS-Berechtigungen und Rückruf-Telefonnummerninformationen für einen angegebenen Benutzer ab.
ms.assetid: 178ff775-9cd2-43f0-9a9a-dbae337c5fe8
keywords:
- RasAdminUserGetInfo-Funktion RAS
topic_type:
- apiref
api_name:
- RasAdminUserGetInfo
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4cda41447af832bd4ae04a14c6f8038fee4b61a17ac98c919c0b085261b242d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117788688"
---
# <a name="rasadminusergetinfo-function"></a>RasAdminUserGetInfo-Funktion

\[Diese Funktion wird nur aus Gründen der Abwärtskompatibilität mit Windows NT Server 4.0 bereitgestellt. Auf \_ Windows \_ Server 2003 wird ERROR CALL NOT \_ IMPLEMENTED zurückgegeben. Anwendungen sollten die [**MprAdminUserGetInfo-Funktion**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusergetinfo) verwenden.\]

Die **RasAdminUserGetInfo-Funktion** ruft die RAS-Berechtigungen und Rückruf-Telefonnummerninformationen für einen angegebenen Benutzer ab.

## <a name="syntax"></a>Syntax


```C++
DWORD RasAdminUserGetInfo(
  _In_ const WCHAR       *lpszUserAccountServer,
  _In_ const WCHAR       *lpszUser,
             PRAS_USER_0 pRasUser0
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lpszUserAccountServer* \[ In\]
</dt> <dd>

Zeiger auf eine auf NULL endende Unicode-Zeichenfolge, die den Namen des primären oder Sicherungsdomänencontrollers angibt, der über die Benutzerkontodatenbank verfügt. Verwenden Sie die [**RasAdminGetUserAccountServer-Funktion,**](rasadmingetuseraccountserver.md) um diesen Servernamen abzurufen.

</dd> <dt>

*lpszUser* \[ In\]
</dt> <dd>

Zeiger auf eine auf NULL endende Unicode-Zeichenfolge, die den Namen des Benutzers angibt, für den RAS-Informationen abzurufen sind.

</dd> <dt>

*pRasUser0* 
</dt> <dd>

Zeiger auf die [**RAS \_ USER \_ 0-Struktur,**](ras-user-0-str.md) die die RAS-Daten für den angegebenen Benutzer empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert ERROR \_ SUCCESS.

Wenn die Funktion fehlschlägt, kann der Rückgabewert der folgende Fehlercode sein.



| Wert                                                                                            | Bedeutung                                                  |
|--------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**NERR \_ BufTooSmall**</dt> </dl> | Nicht genügend Arbeitsspeicher, um diese Funktion auszuführen.<br/> |



 

Für diese Funktion sind keine erweiterten Fehlerinformationen vorhanden. Rufen [**Sie getLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)nicht auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows 2000 Professional<br/>                                                   |
| Ende des Supports (Server)<br/> | Windows 2000 Server<br/>                                                         |
| Header<br/>                | <dl> <dt>Rassapi.h</dt> </dl>   |
| Bibliothek<br/>               | <dl> <dt>Rassapi.lib</dt> </dl> |
| DLL<br/>                   | <dl> <dt>Rassapi.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Remotezugriffsdienst (RAS) – Übersicht](about-remote-access-service.md)
</dt> <dt>

[RAS-Serververwaltungsfunktionen](ras-server-administration-functions.md)
</dt> <dt>

[**\_RAS-BENUTZER \_ 0**](ras-user-0-str.md)
</dt> <dt>

[**RasAdminGetUserAccountServer**](rasadmingetuseraccountserver.md)
</dt> <dt>

[**RasAdminUserSetInfo**](rasadminusersetinfo.md)
</dt> </dl>

 

