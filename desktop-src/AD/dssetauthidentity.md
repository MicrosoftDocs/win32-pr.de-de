---
title: Dssetauthidentity-Funktion (ntdsbcli. h)
description: Legt den Sicherheitskontext fest, unter dem die APIs für die Verzeichnis Sicherung aufgerufen werden.
ms.assetid: bfa2f847-6fe3-4f9b-bafa-acf6a7c861d9
ms.tgt_platform: multiple
keywords:
- Dssetauthidentity-Funktion Active Directory
topic_type:
- apiref
api_name:
- DsSetAuthIdentity
- DsSetAuthIdentityA
- DsSetAuthIdentityW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40d973d5f818b4bd81278a1466487ae89ebf888f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477343"
---
# <a name="dssetauthidentity-function"></a>Dssetauthidentity-Funktion

\[Diese Funktion ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Verwenden Sie ab Windows Vista [Volumeschattenkopie-Dienst (VSS)](../vss/volume-shadow-copy-service-overview.md) .\]

Die **dssetauthidentity** -Funktion legt den Sicherheitskontext fest, unter dem die Verzeichnis Sicherungs-APIs aufgerufen werden.

## <a name="syntax"></a>Syntax


```C++
HRESULT DsSetAuthIdentity(
  _In_ LPCTSTR szUserName,
  _In_ LPCTSTR szDomainName,
  _In_ LPCTSTR szPassword
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*szusername* \[ in\]
</dt> <dd>

Die NULL-terminierte Zeichenfolge, die den Benutzernamen angibt.

</dd> <dt>

*szdomainname* \[ in\]
</dt> <dd>

Die NULL-terminierte Zeichenfolge, die den Namen der Domäne angibt, zu der der Benutzer gehört.

</dd> <dt>

*szPassword* \[ in\]
</dt> <dd>

Die NULL-terminierte Zeichenfolge, die das Kennwort des Benutzers in der angegebenen Domäne angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn erfolgreich, wird ein Standard- **HRESULT** -Erfolgs Code zurückgegeben. Andernfalls wird ein Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Wenn **dssetauthidentity** nicht aufgerufen wird, wird der Sicherheitskontext des aktuellen Prozesses angenommen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Ntdsbcli. h</dt> </dl>   |
| Bibliothek<br/>                  | <dl> <dt>Ntdsbcli. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **Dssetauthidentityw** (Unicode) und **dssetauthidentitya** (ANSI)<br/>           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Sichern und Wiederherstellen eines Active Directory Servers](backing-up-and-restoring-an-active-directory-server.md)
</dt> <dt>

[Verzeichnis Sicherungsfunktionen](directory-backup-functions.md)
</dt> </dl>

 

