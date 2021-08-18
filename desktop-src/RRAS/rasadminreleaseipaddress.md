---
title: Rückruffunktion "RasAdminReleaseIpAddress"
description: Die RasAdminReleaseIpAddress-Funktion ist eine anwendungsdefinierte Funktion, die von einer RAS-Serververwaltungs-DLL eines Drittanbieters exportiert wird.
ms.assetid: 86fd9173-f158-4de5-8166-483a652a52cc
keywords:
- RasAdminReleaseIpAddress-Rückruffunktion RAS
topic_type:
- apiref
api_name:
- RasAdminReleaseIpAddress
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 102c9af7a8e38ccbbb4a7e67b2734588857ddca93da862be211fd1223133f80d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117788862"
---
# <a name="rasadminreleaseipaddress-callback-function"></a>Rückruffunktion "RasAdminReleaseIpAddress"

\[Die **RasAdminReleaseIpAddress-Funktion** ist für die Verwendung in Windows NT 4.0 verfügbar und in nachfolgenden Versionen nicht verfügbar. Verwenden Sie stattdessen [**MprAdminReleaseIpAddress**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipaddress).\]

Die **RasAdminReleaseIpAddress-Funktion** ist eine anwendungsdefinierte Funktion, die von einer RAS-Serververwaltungs-DLL eines Drittanbieters exportiert wird. RAS ruft diese Funktion auf, um die DLL zu benachrichtigen, dass der Remoteclient getrennt wurde und dass die IP-Adresse freigegeben werden soll.

## <a name="syntax"></a>Syntax


```C++
void CALLBACK RasAdminReleaseIpAddress(
  _In_ WCHAR  *lpszUserName,
  _In_ WCHAR  *lpszPortName,
  _In_ IPADDR *pipAddress
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lpszUserName* \[ In\]
</dt> <dd>

Gibt den Zeiger auf eine auf NULL endende Unicode-Zeichenfolge an, die den Namen eines Remotebenutzers angibt, für den zuvor mithilfe der [**RasAdminGetIpAddressForUser-Funktion**](rasadmingetipaddressforuser.md) eine IP-Adresse abgerufen wurde.

</dd> <dt>

*lpszPortName* \[ In\]
</dt> <dd>

Zeiger auf eine auf NULL endende Unicode-Zeichenfolge, die den Namen des Ports angibt, an dem der von *lpszUserName* angegebene Benutzer verbunden ist.

</dd> <dt>

*pipAddress* \[ In\]
</dt> <dd>

Zeiger auf eine **IPADDR-Variable,** die die IP-Adresse angibt, die für diesen Benutzer in einem vorherigen Aufruf von [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md)zurückgegeben wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Für diese Funktion sind keine erweiterten Fehlerinformationen vorhanden. Rufen [**Sie getLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)nicht auf.

## <a name="remarks"></a>Hinweise

Der RAS-Server ruft die **RasAdminReleaseIpAddress-Funktion** nur auf, wenn die Anwendung **true** im *bNotifyRelease-Parameter* während des vorherigen Aufrufs von [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md) für den vom *lpszUserName-Parameter angegebenen* Benutzer zurückgegeben hat.

Das Setupprogramm für eine RAS-Verwaltungs-DLL eines Drittanbieters muss die DLL bei RAS registrieren, indem Informationen unter dem folgenden Schlüssel in der Registrierung zur Verfügung gestellt werden:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

Legen Sie zum Registrieren der DLL die folgenden Werte unter diesem Schlüssel fest.



| Wertname    | Wertdaten                                                                    |
|---------------|-------------------------------------------------------------------------------|
| *DisplayName* | Eine **REG \_ SZ-Zeichenfolge,** die den benutzerfreundlichen Anzeigenamen der DLL enthält. |
| *DLLPath*     | Eine **REG \_ SZ-Zeichenfolge,** die den vollständigen Pfad der DLL enthält.                  |



 

Der Registrierungseintrag für eine RAS-Verwaltungs-DLL eines fiktiven Unternehmens mit dem Namen ProElecron, Inc. kann beispielsweise wie im Folgenden beschrieben sein:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

*DisplayName*: **REG \_ SZ** : ProElecron RAS Admin DLL *DLLPath*: **REG \_ SZ** : C: \\ nt \\ system32 \\ntwkadm.dll

Das Setupprogramm für eine RAS-Verwaltungs-DLL sollte auch Funktionen zum Entfernen/Deinstallieren bereitstellen. Wenn ein Benutzer die DLL entfernt, sollte das Setupprogramm die Registrierungseinträge der DLL löschen.

 

 