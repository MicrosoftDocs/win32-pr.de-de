---
title: DsBackupEnd-Funktion (Ntdsbcli.h)
description: Wird aufgerufen, um einen Sicherungsvorgang zu beenden.
ms.assetid: 872645bc-3dbe-4b12-af4f-778d54feb18f
ms.tgt_platform: multiple
keywords:
- DsBackupEnd-Funktion Active Directory
topic_type:
- apiref
api_name:
- DsBackupEnd
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 479a1641a6d347837733da7e7d26e67b2011654e638681ec774a6ec5d931e211
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118430250"
---
# <a name="dsbackupend-function"></a>DsBackupEnd-Funktion

\[Diese Funktion ist für die Verwendung in den Im Abschnitt Anforderungen angegebenen Betriebssystemen verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Ab Windows Vista verwenden Sie stattdessen [Volumeschattenkopie-Dienst (VSS).](../vss/volume-shadow-copy-service-overview.md)\]

Die **DsBackupEnd-Funktion** wird aufgerufen, um einen Sicherungsvorgang zu beenden.

## <a name="syntax"></a>Syntax


```C++
HRESULT DsBackupEnd(
  _In_ HBC hbc
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hbc* \[ In\]
</dt> <dd>

Enthält das Sicherungskontexthand handle, das mit der [**DsBackupPrepare-Funktion ermittelt**](dsbackupprepare.md) wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **S \_ OK zurück,** wenn die Funktion erfolgreich ist, andernfalls ein Win32- oder RPC-Fehlercode. In der folgenden Liste sind weitere mögliche Fehlercodes aufgeführt.

<dl> <dt>

**FEHLER \_ UNGÜLTIGER \_ PARAMETER**
</dt> <dd>

*hbc* ist ungültig.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **DsBackupEnd-Funktion** schließt ausstehende Bindungshandles und führt nach einem erfolgreichen oder nicht erfolgreichen Sicherungsversuch eine Bereinigung durch.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Ntdsbcli.h</dt> </dl>   |
| Bibliothek<br/>                  | <dl> <dt>Ntdsbcli.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**DsSetAuthIdentity**](dssetauthidentity.md)
</dt> <dt>

[Sichern eines Active Directory-Servers](backing-up-an-active-directory-server.md)
</dt> <dt>

[Verzeichnissicherungsfunktionen](directory-backup-functions.md)
</dt> </dl>

 

