---
title: Rasadminusermentinfo-Funktion (rassapi. h)
description: Die rasadminusersetinfo-Funktion legt die RAS-Berechtigungen und die Rückruf Telefonnummer für einen angegebenen Benutzer fest.
ms.assetid: 5b049dfd-ecc8-47e4-82cc-71a875752714
keywords:
- Rasadminusereintinfo-Funktion (RAS)
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
ms.openlocfilehash: 16d35f62713a3f4669db191891d2fb6b1694cabe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364962"
---
# <a name="rasadminusersetinfo-function"></a>Rasadminusermentinfo-Funktion

\[Diese Funktion wird nur aus Gründen der Abwärtskompatibilität mit Windows NT Server 4,0 bereitgestellt. Es wird ein Fehler zurückgegeben, \_ \_ \_ der auf Windows Server 2003 nicht implementiert ist. Anwendungen sollten die [**mpradminusermentinfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusersetinfo) -Funktion verwenden.\]

Die **rasadminusersetinfo** -Funktion legt die RAS-Berechtigungen und die Rückruf Telefonnummer für einen angegebenen Benutzer fest.

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

*lpszuseraccountserver* \[ in\]
</dt> <dd>

Zeiger auf eine mit NULL endenden Unicode-Zeichenfolge, die den Namen des primären oder Sicherungs Domänen Controllers mit der Benutzerkonten Datenbank angibt. Verwenden Sie die [**rasadmingetuseraccountserver**](rasadmingetuseraccountserver.md) -Funktion, um diesen Servernamen abzurufen.

</dd> <dt>

*lpszuser* \[ in\]
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Unicode-Zeichenfolge, die den Namen des Benutzers angibt, für den RAS-Informationen festgelegt werden sollen.

</dd> <dt>

*pRasUser0* \[ in\]
</dt> <dd>

Ein Zeiger auf die [**RAS- \_ Benutzer- \_ 0**](ras-user-0-str.md) -Struktur, die die neuen RAS-Daten für den angegebenen Benutzer angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert Fehler \_ erfolgreich.

Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Fehlercodes sein.



| Wert                                                                                                           | BESCHREIBUNG                                                                                     |
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_ungültige \_ Daten**</dt> </dl>             | Der *pRasUser0* -Puffer enthält ungültige Daten.<br/>                                        |
| <dl> <dt>**Fehler \_ ungültige \_ Rückruf \_ Nummer.**</dt> </dl> | Die im *pRasUser0* -Puffer angegebene Rückrufnummer enthält ungültige Zeichen.<br/> |
| <dl> <dt>**NERR \_ Buf-osmall**</dt> </dl>               | Nicht genügend Arbeitsspeicher zum Ausführen dieser Funktion.<br/>                                        |



 

Es sind keine erweiterten Fehlerinformationen für diese Funktion vorhanden. " [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)" nicht aufrufen.

## <a name="remarks"></a>Bemerkungen

Beim Festlegen der RAS-Berechtigungen für einen Benutzer muss der **bfprivilege** -Member der [**RAS-Benutzer- \_ \_ 0**](ras-user-0-str.md) -Struktur mindestens eines der rückgabeflags angeben. Um z. b. die Berechtigungen eines Benutzers so festzulegen, dass Einwählberechtigungen, aber keine Rückruf Berechtigung zulässig sind, legen Sie **bfprivilege** auf raspriv \_ dialinprivilege \| raspriv \_ NoCallback fest.

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

[**Rasadminusergetinfo**](rasadminusergetinfo.md)
</dt> </dl>

 

