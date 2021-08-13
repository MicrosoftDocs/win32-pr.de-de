---
title: DsBackupGetBackupLogs-Funktion (Ntdsbcli.h)
description: Erhält die Liste der Protokolldateien, die für den angegebenen Sicherungskontext gesichert werden müssen.
ms.assetid: 09b3fdac-41ea-471c-a0dd-54414181f6fe
ms.tgt_platform: multiple
keywords:
- DsBackupGetBackupLogs-Funktion Active Directory
topic_type:
- apiref
api_name:
- DsBackupGetBackupLogs
- DsBackupGetBackupLogsA
- DsBackupGetBackupLogsW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d4a240ef514fc62450a04f512f04d985380b79fa20daaee9ff4b27ccb71027a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118430103"
---
# <a name="dsbackupgetbackuplogs-function"></a>DsBackupGetBackupLogs-Funktion

\[Diese Funktion ist für die Verwendung in den im Abschnitt Anforderungen angegebenen Betriebssystemen verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Ab Windows Vista verwenden Sie stattdessen [Volumeschattenkopie-Dienst (VSS).](../vss/volume-shadow-copy-service-overview.md)\]

Die **DsBackupGetBackupLogs-Funktion** erhält die Liste der Protokolldateien, die für den angegebenen Sicherungskontext gesichert werden müssen.

## <a name="syntax"></a>Syntax


```C++
HRESULT DsBackupGetBackupLogs(
  _In_  HBC     hbc,
  _Out_ LPTSTR  *pszBackupLogFiles,
  _Out_ LPDWORD pcbSize
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hbc* \[ In\]
</dt> <dd>

Enthält das Mit der [**DsBackupPrepare-Funktion erhaltene Sicherungskontexthand**](dsbackupprepare.md) handle.

</dd> <dt>

*pszBackupLogFiles* \[ out\]
</dt> <dd>

Zeiger auf einen Zeichenfolgenzeiger, der die Liste der Protokolldateinamen als UNC-Pfade empfängt. Initialisieren Sie diesen Wert auf **NULL,** bevor **Sie DsBackupGetBackupLogs aufrufen.**

Diese Liste empfängt eine doppelte Null-Terminierungsliste mit einzelnen Zeichenfolgen mit NULL-Terminierung.

Dieser Puffer wird von der **DsBackupGetBackupLogs-Funktion** zugeordnet und muss durch Aufrufen der [**DsBackupFree-Funktion nicht**](dsbackupfree.md) mehr benötigt werden.

Das erste Zeichen jedes Dateinamens enthält eine der [**BFT-Konstanten,**](bft-constants.md) die den Typ des Namens identifizieren.

</dd> <dt>

*besize* \[ out\]
</dt> <dd>

Zeiger auf **den DWORD-Wert,** der die Größe des *Puffers pszBackupLogFiles* in Bytes empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **S \_ OK zurück,** wenn die Funktion erfolgreich ist, andernfalls ein Win32- oder RPC-Fehlercode. In der folgenden Liste sind weitere mögliche Fehlercodes aufgeführt.

<dl> <dt>

**FEHLER \_ BEIM \_ ZUGRIFF VERWEIGERT**
</dt> <dd>

Der Aufrufer verfügt nicht über die richtigen Zugriffsberechtigungen zum Aufrufen dieser Funktion. Mit [**der DsSetAuthIdentity-Funktion**](dssetauthidentity.md) können die Anmeldeinformationen festgelegt werden, die für die Sicherungs- und Wiederherstellungsfunktionen verwendet werden sollen.

</dd> <dt>

**FEHLER \_ UNGÜLTIGER \_ PARAMETER**
</dt> <dd>

*"hbc",* *"pszBackupLogFiles"* *oder "formatSize" ist* ungültig.

</dd> <dt>

**FEHLER: \_ NICHT \_ GENÜGEND \_ ARBEITSSPEICHER**
</dt> <dd>

Es ist ein Speicherbelegungsfehler aufgetreten.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **Funktion DsBackupGetBackupLogs enthält** eine Liste der Protokolldateien, die für eine Sicherung erforderlich sind. Eine vollständige Sicherung besteht aus den Datenbankdateien, die von der [**DsBackupGetDatabaseNames-Funktion**](dsbackupgetdatabasenames.md) bereitgestellt werden, und den Protokolldateien. Inkrementelle Sicherungen von Active Directory-Servern werden nicht unterstützt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Ntdsbcli.h</dt> </dl>   |
| Bibliothek<br/>                  | <dl> <dt>Ntdsbcli.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **DsBackupGetBackupLogsW** (Unicode) und **DsBackupGetBackupLogsA** (ANSI)<br/>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**DsBackupFree**](dsbackupfree.md)
</dt> <dt>

[**DsBackupGetDatabaseNames**](dsbackupgetdatabasenames.md)
</dt> <dt>

[**BFT-Konstanten**](bft-constants.md)
</dt> <dt>

[Sichern eines Active Directory-Servers](backing-up-an-active-directory-server.md)
</dt> <dt>

[Verzeichnissicherungsfunktionen](directory-backup-functions.md)
</dt> </dl>

 

