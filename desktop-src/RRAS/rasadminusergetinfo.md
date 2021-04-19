---
title: Rasadminusergetinfo-Funktion (rassapi. h)
description: Die rasadminusergetinfo-Funktion Ruft die RAS-Berechtigungen und Rückruf Telefonnummer-Informationen für einen angegebenen Benutzer ab.
ms.assetid: 178ff775-9cd2-43f0-9a9a-dbae337c5fe8
keywords:
- Rasadminusergetinfo-Funktion (RAS)
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
ms.openlocfilehash: 89fe08a918a958ffb5a656ce2c76cecec31cbb61
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352981"
---
# <a name="rasadminusergetinfo-function"></a>Rasadminusergetinfo-Funktion

\[Diese Funktion wird nur aus Gründen der Abwärtskompatibilität mit Windows NT Server 4,0 bereitgestellt. Es wird ein Fehler zurückgegeben, \_ \_ \_ der auf Windows Server 2003 nicht implementiert ist. Anwendungen sollten die [**mpradminusergetinfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusergetinfo) -Funktion verwenden.\]

Die **rasadminusergetinfo** -Funktion Ruft die RAS-Berechtigungen und Rückruf Telefonnummer-Informationen für einen angegebenen Benutzer ab.

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

*lpszuseraccountserver* \[ in\]
</dt> <dd>

Zeiger auf eine mit NULL endenden Unicode-Zeichenfolge, die den Namen des primären oder Sicherungs Domänen Controllers mit der Benutzerkonten Datenbank angibt. Verwenden Sie die [**rasadmingetuseraccountserver**](rasadmingetuseraccountserver.md) -Funktion, um diesen Servernamen abzurufen.

</dd> <dt>

*lpszuser* \[ in\]
</dt> <dd>

Ein Zeiger auf eine mit NULL endenden Unicode-Zeichenfolge, die den Namen des Benutzers angibt, für den RAS-Informationen zu erhalten sind.

</dd> <dt>

*pRasUser0* 
</dt> <dd>

Ein Zeiger auf die [**RAS- \_ Benutzer- \_ 0**](ras-user-0-str.md) -Struktur, die die RAS-Daten für den angegebenen Benutzer empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert Fehler \_ erfolgreich.

Wenn die Funktion fehlschlägt, kann der folgende Fehlercode als Rückgabewert zurückgegeben werden.



| Wert                                                                                            | Bedeutung                                                  |
|--------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**Nr \_ buf**</dt> </dl> | Nicht genügend Arbeitsspeicher zum Ausführen dieser Funktion.<br/> |



 

Es sind keine erweiterten Fehlerinformationen für diese Funktion vorhanden. " [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)" nicht aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows 2000 Professional<br/>                                                   |
| Ende des Supports (Server)<br/> | Windows 2000 Server<br/>                                                         |
| Header<br/>                | <dl> <dt>Rassapi. h</dt> </dl>   |
| Bibliothek<br/>               | <dl> <dt>Rassapi. lib</dt> </dl> |
| DLL<br/>                   | <dl> <dt>Rassapi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Remote Zugriffs Dienst (RAS) (Übersicht)](about-remote-access-service.md)
</dt> <dt>

[RAS-Server-Verwaltungsfunktionen](ras-server-administration-functions.md)
</dt> <dt>

[**RAS- \_ Benutzer \_ 0**](ras-user-0-str.md)
</dt> <dt>

[**Rasadmingetuseraccountserver**](rasadmingetuseraccountserver.md)
</dt> <dt>

[**Rasadminusereintinfo**](rasadminusersetinfo.md)
</dt> </dl>

 

