---
title: DsBackupOpenFile-Funktion (Ntdsbcli.h)
description: Öffnet die angegebene Datei und führt die Client- und Servervorgänge aus, die zum Vorbereiten der Datei für die Sicherung erforderlich sind.
ms.assetid: 1ffb81ee-9e7e-4d88-91fc-f1857377d125
ms.tgt_platform: multiple
keywords:
- DsBackupOpenFile-Funktion Active Directory
topic_type:
- apiref
api_name:
- DsBackupOpenFile
- DsBackupOpenFileA
- DsBackupOpenFileW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6331dc79a93e515d49c688bc8c5dd3b9e747cfbac91ace9c7685a219ae21e95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118430012"
---
# <a name="dsbackupopenfile-function"></a>DsBackupOpenFile-Funktion

\[Diese Funktion ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Verwenden Sie ab Windows Vista stattdessen [Volumeschattenkopie-Dienst (VSS).](../vss/volume-shadow-copy-service-overview.md)\]

Die **DsBackupOpenFile-Funktion** öffnet die angegebene Datei und führt die Client- und Servervorgänge aus, die zum Vorbereiten der Datei für die Sicherung erforderlich sind.

## <a name="syntax"></a>Syntax


```C++
HRESULT DsBackupOpenFile(
  _In_  HBC           hbc,
  _In_  LPCTSTR       szAttachmentName,
  _In_  DWORD         cbReadHintSize,
  _Out_ LARGE_INTEGER *pliFileSize
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hbc* \[ In\]
</dt> <dd>

Enthält das Sicherungskontexthandle, das mit der [**DsBackupPrepare-Funktion**](dsbackupprepare.md) abgerufen wurde.

</dd> <dt>

*szAttachmentName* \[ In\]
</dt> <dd>

Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen der zu öffnenden Sicherungsdatei angibt.

</dd> <dt>

*cbReadHintSize* \[ In\]
</dt> <dd>

Enthält die mögliche Größe des Puffers in Bytes, der als *pvBuffer-Argument* in der [**DsBackupRead-Funktion**](dsbackupread.md) übergeben wird. Die Sicherungsfunktionen verwenden diesen Wert als Hinweis, um den Netzwerkdatenverkehr zu optimieren. Dieser Wert muss ein Vielfaches von 8192 und größer oder gleich 24576 sein.

</dd> <dt>

*pliFileSize* \[ out\]
</dt> <dd>

Zeiger auf einen **LARGE \_ INTEGER-Wert,** der die Größe der geöffneten Sicherungsdatei in Bytes empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **S \_ OK** zurück, wenn die Funktion erfolgreich ist oder andernfalls ein Win32- oder RPC-Fehlercode vorliegt. In der folgenden Liste sind weitere mögliche Fehlercodes aufgeführt.

<dl> <dt>

**FEHLERZUGRIFF \_ \_ VERWEIGERT**
</dt> <dd>

Der Aufrufer verfügt nicht über die richtigen Zugriffsberechtigungen zum Aufrufen dieser Funktion. Die [**DsSetAuthIdentity-Funktion**](dssetauthidentity.md) kann verwendet werden, um die Anmeldeinformationen festzulegen, die für die Sicherungs- und Wiederherstellungsfunktionen verwendet werden sollen.

</dd> <dt>

**FEHLER: \_ UNGÜLTIGER \_ PARAMETER**
</dt> <dd>

*hbc,* *szAttachmentName* oder *pliFileSize* sind ungültig.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Ntdsbcli.h</dt> </dl>   |
| Bibliothek<br/>                  | <dl> <dt>Ntdsbcli.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **DsBackupOpenFileW** (Unicode) und **DsBackupOpenFileA** (ANSI)<br/>             |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**DsBackupRead**](dsbackupread.md)
</dt> <dt>

[Sichern eines Active Directory-Servers](backing-up-an-active-directory-server.md)
</dt> <dt>

[Verzeichnissicherungsfunktionen](directory-backup-functions.md)
</dt> </dl>

 

