---
title: DsBackupClose-Funktion (Ntdsbcli.h)
description: Schließt eine Mit der DsBackupOpenFile-Funktion geöffnete Sicherungsdatei.
ms.assetid: 5452a222-abe8-4d2d-84ff-6f577073b220
ms.tgt_platform: multiple
keywords:
- DsBackupClose-Funktion Active Directory
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
ms.openlocfilehash: 00c9c8931d67b33fdad1f9e3605ee6efe801dac988d3931d96d1417561c093b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118192188"
---
# <a name="dsbackupclose-function"></a>DsBackupClose-Funktion

\[Diese Funktion ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Verwenden Sie ab Windows Vista stattdessen [Volumeschattenkopie-Dienst (VSS).](../vss/volume-shadow-copy-service-overview.md)\]

Die **DsBackupClose-Funktion** schließt eine Sicherungsdatei, die mit der [**DsBackupOpenFile-Funktion**](dsbackupopenfile.md) geöffnet wurde. Für jedes Sicherungshandle kann jeweils nur eine Datei geöffnet werden, sodass diese Funktion die derzeit geöffnete Datei schließt.

## <a name="syntax"></a>Syntax


```C++
HRESULT DsBackupClose(
  _In_ HBC hbc
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hbc* \[ In\]
</dt> <dd>

Enthält das Sicherungskontexthandle, das mit der [**DsBackupPrepare-Funktion**](dsbackupprepare.md) abgerufen wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **S \_ OK** zurück, wenn die Funktion erfolgreich ist oder andernfalls ein Win32- oder RPC-Fehlercode vorliegt. In der folgenden Liste sind weitere mögliche Fehlercodes aufgeführt.

<dl> <dt>

**FEHLER: \_ UNGÜLTIGER \_ PARAMETER**
</dt> <dd>

*hbc* ist ungültig.

</dd> <dt>

**hrInvalidHandle**
</dt> <dd>

Derzeit ist keine Datei geöffnet.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Ntdsbcli.h</dt> </dl>   |
| Bibliothek<br/>                  | <dl> <dt>Ntdsbcli.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**DsBackupOpenFile**](dsbackupopenfile.md)
</dt> <dt>

[**DsBackupPrepare**](dsbackupprepare.md)
</dt> <dt>

[Sichern eines Active Directory-Servers](backing-up-an-active-directory-server.md)
</dt> <dt>

[Verzeichnissicherungsfunktionen](directory-backup-functions.md)
</dt> </dl>

 

