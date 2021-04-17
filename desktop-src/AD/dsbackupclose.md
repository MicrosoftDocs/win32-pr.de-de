---
title: Dsbackupclose-Funktion (ntdsbcli. h)
description: Schließt eine Sicherungsdatei, die mit der dsbackupopenfile-Funktion geöffnet wurde.
ms.assetid: 5452a222-abe8-4d2d-84ff-6f577073b220
ms.tgt_platform: multiple
keywords:
- Dsbackupclose-Funktion Active Directory
topic_type:
- apiref
api_name:
- DsBackupClose
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5d03c9cd7f125d223d264236a52120714d5198c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476359"
---
# <a name="dsbackupclose-function"></a>Dsbackupclose-Funktion

\[Diese Funktion ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Verwenden Sie ab Windows Vista [Volumeschattenkopie-Dienst (VSS)](../vss/volume-shadow-copy-service-overview.md) .\]

Die **dsbackupclose** -Funktion schließt eine Sicherungsdatei, die mit der [**dsbackupopenfile**](dsbackupopenfile.md) -Funktion geöffnet wurde. Für jedes Sicherungs Handle kann jeweils nur eine Datei geöffnet werden. Daher schließt diese Funktion die aktuell geöffnete Datei.

## <a name="syntax"></a>Syntax


```C++
HRESULT DsBackupClose(
  _In_ HBC hbc
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*HBC* \[ in\]
</dt> <dd>

Enthält das Sicherungs Kontext Handle, das mit der [**dsbackupprepare**](dsbackupprepare.md) -Funktion abgerufen wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **S \_ OK** zurück, wenn die Funktion erfolgreich ist, andernfalls ein Win32-oder RPC-Fehlercode. In der folgenden Liste sind andere mögliche Fehlercodes aufgeführt.

<dl> <dt>

**Fehler bei \_ ungültigem \_ Parameter**
</dt> <dd>

*HBC* ist ungültig.

</dd> <dt>

**hrinvalidhandle**
</dt> <dd>

Zurzeit ist keine Datei geöffnet.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Ntdsbcli. h</dt> </dl>   |
| Bibliothek<br/>                  | <dl> <dt>Ntdsbcli. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Dsbackupopenfile**](dsbackupopenfile.md)
</dt> <dt>

[**Dsbackupprepare**](dsbackupprepare.md)
</dt> <dt>

[Sichern eines Active Directory Servers](backing-up-an-active-directory-server.md)
</dt> <dt>

[Verzeichnis Sicherungsfunktionen](directory-backup-functions.md)
</dt> </dl>

 

