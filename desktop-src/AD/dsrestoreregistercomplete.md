---
title: DsRestoreRegisterComplete-Funktion (Ntdsbcli.h)
description: Wird aufgerufen, um einen Active Directory-Server nach Abschluss eines Wiederherstellungsvorgangs zu entsperren.
ms.assetid: 781cd2ec-d2e2-4f3a-903d-feda4b871de5
ms.tgt_platform: multiple
keywords:
- DsRestoreRegisterComplete-Funktion Active Directory
topic_type:
- apiref
api_name:
- DsRestoreRegisterComplete
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b335f67ed4d392d189553f66655797e03121cbdee6ce19dffbd9803199f6c72
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118429928"
---
# <a name="dsrestoreregistercomplete-function"></a>DsRestoreRegisterComplete-Funktion

\[Diese Funktion ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Verwenden Sie stattdessen [Volumeschattenkopie-Dienst (VSS).](../vss/volume-shadow-copy-service-overview.md)\]

Die **DsRestoreRegisterComplete-Funktion** wird aufgerufen, um einen Active Directory-Server nach Abschluss eines Wiederherstellungsvorgangs zu entsperren. Diese Funktion ist eine Entsprechung zur [**DsRestoreRegister-Funktion.**](dsrestoreregister.md)

## <a name="syntax"></a>Syntax


```C++
HRESULT DsRestoreRegisterComplete(
  _In_ HBC     hbc,
  _In_ HRESULT hrRestoreState
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hbc* \[ In\]
</dt> <dd>

Enthält das Mit der [**DsRestorePrepare-Funktion abgerufene**](dsrestoreprepare.md) Wiederherstellungskontexthandle.

</dd> <dt>

*hrRestoreState* \[ In\]
</dt> <dd>

Enthält den endgültigen Status des Wiederherstellungsvorgangs. Dieser Parameter sollte **S \_ OK** enthalten, wenn der Wiederherstellungsvorgang erfolgreich war, oder andernfalls einen Fehlercode.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **S \_ OK** zurück, wenn die Funktion erfolgreich ist oder andernfalls ein Win32- oder RPC-Fehlercode vorliegt. In der folgenden Liste sind mögliche Fehlercodes aufgeführt.

<dl> <dt>

**FEHLERZUGRIFF \_ \_ VERWEIGERT**
</dt> <dd>

Der Aufrufer verfügt nicht über die richtigen Zugriffsberechtigungen zum Aufrufen dieser Funktion. Die [**DsSetAuthIdentity-Funktion**](dssetauthidentity.md) kann verwendet werden, um die Anmeldeinformationen festzulegen, die für die Sicherungs- und Wiederherstellungsfunktionen verwendet werden sollen.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Bevor Sie den Domänencontroller neu starten, rufen Sie diese Funktion auf, um den Status des Wiederherstellungsvorgangs anzugeben. Wenn der Status nicht erfolgreich ist, wird der Verzeichnisdienst erst gestartet, nachdem eine gültige Datenbank wiederhergestellt wurde. Diese Funktion schließt den Wiederherstellungsvorgang ab und ermöglicht das Starten Active Directory Domain Services.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                               |
| Ende des Supports (Client)<br/>    | Nicht unterstützt<br/>                                                               |
| Ende des Supports (Server)<br/>    | Nicht unterstützt<br/>                                                               |
| Header<br/>                   | <dl> <dt>Ntdsbcli.h</dt> </dl>   |
| Bibliothek<br/>                  | <dl> <dt>Ntdsbcli.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**DsRestoreRegister**](dsrestoreregister.md)
</dt> <dt>

[**DsRestorePrepare**](dsrestoreprepare.md)
</dt> <dt>

[**DsSetAuthIdentity**](dssetauthidentity.md)
</dt> <dt>

[Wiederherstellen eines Active Directory-Servers](restoring-an-active-directory-server.md)
</dt> <dt>

[Verzeichnissicherungsfunktionen](directory-backup-functions.md)
</dt> </dl>

 

