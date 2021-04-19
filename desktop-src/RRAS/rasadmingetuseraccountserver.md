---
title: Rasadmingetuseraccountserver-Funktion (rassapi. h)
description: Die rasadmingetuseraccountserver-Funktion Ruft den Namen des Servers ab, der über die Benutzerkonten Datenbank verfügt. Verwenden Sie den zurückgegebenen Servernamen in den rasadminusergetinfo-und rasadminusersetinfo-Funktionen, um Informationen zu einem angegebenen Benutzer abzurufen oder festzulegen.
ms.assetid: db91aa48-32af-49ac-87ed-8c484926ca15
keywords:
- Rasadmingetuseraccountserver-Funktion (RAS)
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
ms.openlocfilehash: c506287d94c5ec64445c74d8364a04db98100751
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354164"
---
# <a name="rasadmingetuseraccountserver-function"></a>Rasadmingetuseraccountserver-Funktion

\[Diese Funktion wird nur aus Gründen der Abwärtskompatibilität mit Windows NT Server 4,0 bereitgestellt. Es wird ein Fehler zurückgegeben, \_ \_ \_ der auf Windows Server 2003 nicht implementiert ist. Anwendungen sollten die [**mpradmingetpdcserver**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetpdcserver) -Funktion verwenden.\]

Die **rasadmingetuseraccountserver** -Funktion Ruft den Namen des Servers ab, der über die Benutzerkonten Datenbank verfügt. Verwenden Sie den zurückgegebenen Servernamen in den [**rasadminusergetinfo**](rasadminusergetinfo.md) -und [**rasadminusersetinfo**](rasadminusersetinfo.md) -Funktionen, um Informationen zu einem angegebenen Benutzer abzurufen oder festzulegen.

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

*lpszdomain* \[ in\]
</dt> <dd>

Zeiger auf eine mit **null** endenden Unicode-Zeichenfolge, die den Namen der Domäne angibt, zu der der RAS-Server gehört. Dieser Parameter ist **null** für die RAS-Verwaltungs Anwendungen, die auf Arbeitsstationen oder Servern ausgeführt werden, die keine Mitglieder einer Domäne sind. Wenn dieser Parameter **null** ist, muss der *lpszserver* -Parameter nicht **null** sein.

</dd> <dt>

*lpszserver* \[ in\]
</dt> <dd>

Zeiger auf eine mit **null** endenden Unicode-Zeichenfolge, die den Namen des RAS-Servers angibt. Geben Sie den Namen mit führenden " \\ \\ " Zeichen im folgenden Format an: \\ \\ *Servername*. Dieser Parameter kann **null** sein, wenn der *lpszdomain* -Parameter nicht **null** ist.

</dd> <dt>

*lpszuseraccountserver* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der eine **null**-terminierte Unicode-Zeichenfolge empfängt, die den Namen eines Domänen Controllers mit der Benutzerkonten Datenbank angibt. Der Puffer sollte groß genug sein, um den Servernamen zu speichern (unclen + 1). Die Funktion stellt den zurückgegebenen Servernamen mit führenden " \\ \\ "-Zeichen im Format " \\ \\ *Server* Name" als Präfix bereit.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert Fehler \_ erfolgreich.

Wenn die Funktion fehlschlägt, kann der folgende Fehlercode als Rückgabewert zurückgegeben werden.



| Wert                                                                                                    | Bedeutung                                                     |
|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <dt>**Fehler bei \_ ungültigem \_ Parameter**</dt> </dl> | Sowohl " *lpszdomain* " als auch " *lpszserver* " sind **null**.<br/> |



 

Es sind keine erweiterten Fehlerinformationen für diese Funktion vorhanden. " [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)" nicht aufrufen.

## <a name="remarks"></a>Bemerkungen

Die **rasadmingetuseraccountserver** -Funktion Ruft den Namen des Servers mit der Benutzerkonten Datenbank ab. Diese Funktion erfordert den Namen des RAS-Servers oder den Namen der Domäne, in der sich der RAS-Server befindet.

Der *lpszdomain* -Parameter muss einen gültigen Domänen Namen angeben. Dieser Parameter ist **null** für RAS-Verwaltungs Anwendungen, die auf Servern ausgeführt werden, die nicht Mitglied einer Domäne sind (z. b. befindet sich der Server in seiner eigenen Arbeitsgruppe). In diesem Fall muss der *lpszserver* -Parameter den Servernamen angeben. Um den Servernamen abzurufen, nennen Sie die [**GetComputerName**](/windows/win32/api/winbase/nf-winbase-getcomputernamea) -Funktion. Stellen Sie sicher, dass Sie dem Servernamen die Zeichen "" als Präfix voranstellen \\ \\ .

Handelt es sich bei dem von *lpszserver* angegebenen Servernamen um einen eigenständigen Server (d. h., der Server oder die Arbeitsstation ist kein Mitglied einer Domäne), wird der Servername selbst im *lpszuseraccountserver* -Puffer zurückgegeben.

Verwenden Sie dann den Namen des Benutzerkonto Servers in einem aufzurufenden Befehl der Funktion [**NetQueryDisplayInformation**](/windows/win32/api/lmaccess/nf-lmaccess-netquerydisplayinformation) , um die Benutzer in der Benutzerkonten Datenbank aufzuzählen.

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

[**GetComputerName**](/windows/win32/api/winbase/nf-winbase-getcomputernamea)
</dt> <dt>

[**Rasadminusergetinfo**](rasadminusergetinfo.md)
</dt> <dt>

[**Rasadminusereintinfo**](rasadminusersetinfo.md)
</dt> </dl>

 

