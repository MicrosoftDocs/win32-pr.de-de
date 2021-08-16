---
title: DsSetAuthIdentity-Funktion (Ntdsbcli.h)
description: Legt den Sicherheitskontext fest, unter dem die Verzeichnissicherungs-APIs aufgerufen werden.
ms.assetid: bfa2f847-6fe3-4f9b-bafa-acf6a7c861d9
ms.tgt_platform: multiple
keywords:
- DsSetAuthIdentity-Funktion Active Directory
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
ms.openlocfilehash: a8e4f990d1fa0c6a6a22b0068ea207be61b4aece441977b976f32f82b7b75c8b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118695505"
---
# <a name="dssetauthidentity-function"></a>DsSetAuthIdentity-Funktion

\[Diese Funktion ist für die Verwendung in den Im Abschnitt Anforderungen angegebenen Betriebssystemen verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Ab Windows Vista verwenden Sie stattdessen [Volumeschattenkopie-Dienst (VSS).](../vss/volume-shadow-copy-service-overview.md)\]

Die **DsSetAuthIdentity-Funktion** legt den Sicherheitskontext fest, unter dem die Verzeichnissicherungs-APIs aufgerufen werden.

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

*szUserName* \[ In\]
</dt> <dd>

Die auf NULL beendete Zeichenfolge, die den Benutzernamen angibt.

</dd> <dt>

*szDomainName* \[ In\]
</dt> <dd>

Die auf NULL beendete Zeichenfolge, die den Namen der Domäne angibt, zu der der Benutzer gehört.

</dd> <dt>

*szPassword* \[ In\]
</dt> <dd>

Die auf NULL beendete Zeichenfolge, die das Kennwort des Benutzers in der angegebenen Domäne angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn erfolgreich, gibt einen **HRESULT-Standarderfolgscode** zurück. Andernfalls wird ein Fehlercode zurückgegeben.

## <a name="remarks"></a>Hinweise

Wenn **DsSetAuthIdentity nicht** aufgerufen wird, wird der Sicherheitskontext des aktuellen Prozesses angenommen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Ntdsbcli.h</dt> </dl>   |
| Bibliothek<br/>                  | <dl> <dt>Ntdsbcli.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **DsSetAuthIdentityW** (Unicode) und **DsSetAuthIdentityA** (ANSI)<br/>           |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Sichern und Wiederherstellen eines Active Directory-Servers](backing-up-and-restoring-an-active-directory-server.md)
</dt> <dt>

[Verzeichnissicherungsfunktionen](directory-backup-functions.md)
</dt> </dl>

 

