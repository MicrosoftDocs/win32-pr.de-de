---
title: Rasadminreleaseipaddress-Rückruffunktion
description: Die rasadminreleaseipaddress-Funktion ist eine Anwendungs definierte Funktion, die von einer Drittanbieter-RAS-Server-Verwaltungs-dll exportiert wird.
ms.assetid: 86fd9173-f158-4de5-8166-483a652a52cc
keywords:
- Rasadminreleaseipaddress-Rückruffunktion (RAS)
topic_type:
- apiref
api_name:
- RasAdminReleaseIpAddress
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d58c162ebc6d340b9bd913407bc00aac87e208e4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729816"
---
# <a name="rasadminreleaseipaddress-callback-function"></a>Rasadminreleaseipaddress-Rückruffunktion

\[Die **rasadminreleaseipaddress** -Funktion ist für die Verwendung in Windows NT 4,0 verfügbar und in nachfolgenden Versionen nicht verfügbar. Verwenden Sie stattdessen [**mpradminreleaseipaddress**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipaddress).\]

Die **rasadminreleaseipaddress** -Funktion ist eine Anwendungs definierte Funktion, die von einer Drittanbieter-RAS-Server-Verwaltungs-dll exportiert wird. RAS ruft diese Funktion auf, um die dll zu benachrichtigen, dass der Remote Client getrennt wurde und dass die IP-Adresse freigegeben werden sollte.

## <a name="syntax"></a>Syntax


```C++
void CALLBACK RasAdminReleaseIpAddress(
  _In_ WCHAR  *lpszUserName,
  _In_ WCHAR  *lpszPortName,
  _In_ IPADDR *pipAddress
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lpszusername* \[ in\]
</dt> <dd>

Gibt den Zeiger auf eine NULL-terminierte Unicode-Zeichenfolge an, die den Namen eines Remote Benutzers angibt, für den zuvor mithilfe der [**rasadmingetipaddressforuser**](rasadmingetipaddressforuser.md) -Funktion eine IP-Adresse abgerufen wurde.

</dd> <dt>

*lpszportname* \[ in\]
</dt> <dd>

Ein Zeiger auf eine mit NULL endenden Unicode-Zeichenfolge, die den Namen des Ports angibt, auf dem der von *lpszusername* angegebene Benutzer verbunden ist.

</dd> <dt>

*pipaddress* \[ in\]
</dt> <dd>

Zeiger auf eine **ipaddr** -Variable, die die IP-Adresse angibt, die für diesen Benutzer in einem vorherigen Aufruf von [**rasadmingetipaddressforuser**](rasadmingetipaddressforuser.md)zurückgegeben wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Es sind keine erweiterten Fehlerinformationen für diese Funktion vorhanden. " [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)" nicht aufrufen.

## <a name="remarks"></a>Bemerkungen

Der RAS-Server ruft **die rasadminreleaseipaddress** -Funktion nur auf, wenn die Anwendung während des vorherigen Aufrufs von [**rasadmingetipaddressforuser**](rasadmingetipaddressforuser.md) für den Benutzer, der durch den *lpszusername* -Parameter angegeben wurde, **true** im *bnotifyrelease* -Parameter zurückgegeben hat.

Das Setup Programm für eine Drittanbieter-RAS-Verwaltungs-dll muss die dll bei RAS registrieren, indem unter dem folgenden Schlüssel in der Registrierung Informationen bereitgestellt werden:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

Um die dll zu registrieren, legen Sie die folgenden Werte unter diesem Schlüssel fest.



| Wertname    | Wertdaten                                                                    |
|---------------|-------------------------------------------------------------------------------|
| *DisplayName* | Eine **reg \_ SZ** -Zeichenfolge, die den benutzerfreundlichen anzeigen amen der dll enthält. |
| *Dll*     | Eine **reg- \_ SZ** -Zeichenfolge, die den vollständigen Pfad der dll enthält.                  |



 

Beispielsweise könnte der Registrierungs Eintrag für eine RAS-Verwaltungs-dll von einem fiktiven Unternehmen mit dem Namen ProElectron, Inc. wie folgt lauten:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

*Display Name*: **reg \_ SZ** : ProElectron RAS admin dll *DllPath*: **reg \_ SZ** : C: \\ NT \\ system32 \\ntwkadm.dll

Das Setup Programm für eine RAS-Verwaltungs-dll sollte auch Funktionen zum Entfernen/Deinstallieren bereitstellen. Wenn ein Benutzer die dll entfernt, sollte das Setup Programm die Registrierungseinträge der dll löschen.

 

 