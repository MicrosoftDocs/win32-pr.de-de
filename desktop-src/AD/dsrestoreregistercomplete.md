---
title: Dsrestoreregistercomplete-Funktion (ntdsbcli. h)
description: Wird aufgerufen, um einen Active Directory Server zu entsperren, nachdem ein Wiederherstellungs Vorgang beendet wurde.
ms.assetid: 781cd2ec-d2e2-4f3a-903d-feda4b871de5
ms.tgt_platform: multiple
keywords:
- Dsrestoreregistercomplete-Funktion Active Directory
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
ms.openlocfilehash: ff5e5e01b29281860dff59fbcd08a3b48ec66c4a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040726"
---
# <a name="dsrestoreregistercomplete-function"></a>Dsrestoreregistercomplete-Funktion

\[Diese Funktion ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Verwenden Sie stattdessen [Volumeschattenkopie-Dienst (VSS)](../vss/volume-shadow-copy-service-overview.md) .\]

Die **dsrestoreregistercomplete** -Funktion wird aufgerufen, um einen Active Directory Server zu entsperren, nachdem ein Wiederherstellungs Vorgang beendet wurde. Diese Funktion ist Gegenstück zur [**dsrestoreregiester**](dsrestoreregister.md) -Funktion.

## <a name="syntax"></a>Syntax


```C++
HRESULT DsRestoreRegisterComplete(
  _In_ HBC     hbc,
  _In_ HRESULT hrRestoreState
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*HBC* \[ in\]
</dt> <dd>

Enthält das Wiederherstellungs Kontext Handle, das mit der [**dsrestoreprepare**](dsrestoreprepare.md) -Funktion abgerufen wurde.

</dd> <dt>

*hrrestorestate* \[ in\]
</dt> <dd>

Enthält den endgültigen Status des Wiederherstellungs Vorgangs. Dieser Parameter sollte **S \_ OK** enthalten, wenn der Wiederherstellungs Vorgang erfolgreich war, andernfalls ein Fehlercode.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **S \_ OK** zurück, wenn die Funktion erfolgreich ist, andernfalls ein Win32-oder RPC-Fehlercode. In der folgenden Liste sind die möglichen Fehlercodes aufgeführt.

<dl> <dt>

**Fehler \_ Zugriff \_ verweigert**
</dt> <dd>

Der Aufrufer verfügt nicht über die erforderlichen Zugriffsberechtigungen, um diese Funktion aufzurufen. Die [**dssetauthidentity**](dssetauthidentity.md) -Funktion kann verwendet werden, um die Anmelde Informationen festzulegen, die für die Sicherungs-und Wiederherstellungs Funktionen verwendet werden sollen.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Bevor Sie den Domänen Controller neu starten, können Sie diese Funktion zum Bereitstellen des Status des Wiederherstellungs Vorgangs abrufen. Wenn der Status nicht erfolgreich ist, wird der Verzeichnisdienst erst gestartet, wenn eine gültige Datenbank wieder hergestellt wurde. Diese Funktion schließt den Wiederherstellungs Vorgang ab und ermöglicht es, Active Directory Domain Services zu starten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                               |
| Ende des Supports (Client)<br/>    | Nicht unterstützt<br/>                                                               |
| Ende des Supports (Server)<br/>    | Nicht unterstützt<br/>                                                               |
| Header<br/>                   | <dl> <dt>Ntdsbcli. h</dt> </dl>   |
| Bibliothek<br/>                  | <dl> <dt>Ntdsbcli. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Dsrestoreregiester**](dsrestoreregister.md)
</dt> <dt>

[**Dsrestoreprepare**](dsrestoreprepare.md)
</dt> <dt>

[**Dssetauthidentity**](dssetauthidentity.md)
</dt> <dt>

[Wiederherstellen eines Active Directory Servers](restoring-an-active-directory-server.md)
</dt> <dt>

[Verzeichnis Sicherungsfunktionen](directory-backup-functions.md)
</dt> </dl>

 

