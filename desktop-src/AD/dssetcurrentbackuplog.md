---
title: Dssetcurrentbackuplog-Funktion (ntdsbcli. h)
description: Legt die aktuelle Sicherungs Protokollnummer nach einer erfolgreichen Wiederherstellung fest.
ms.assetid: 903bddea-c5a7-4b3f-819c-0467a9c5ae1b
ms.tgt_platform: multiple
keywords:
- Dssetcurrentbackuplog-Funktion Active Directory
topic_type:
- apiref
api_name:
- DsSetCurrentBackupLog
- DsSetCurrentBackupLogA
- DsSetCurrentBackupLogW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f50fc41317ae22ae89c47f63bb19f981563e5c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859022"
---
# <a name="dssetcurrentbackuplog-function"></a>Dssetcurrentbackuplog-Funktion

\[Diese Funktion ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Verwenden Sie ab Windows Vista [Volumeschattenkopie-Dienst (VSS)](../vss/volume-shadow-copy-service-overview.md) .\]

Die **dssetcurrentbackuplog** -Funktion legt die aktuelle Sicherungs Protokollnummer nach einer erfolgreichen Wiederherstellung fest. Da Active Directory Domain Services nur zirkuläre Protokollierung unterstützen, wird diese Funktion normalerweise nicht verwendet.

## <a name="syntax"></a>Syntax


```C++
HRESULT DsSetCurrentBackupLog(
  _In_ LPCWSTR szServerName,
  _In_ DWORD   dwCurrentLog
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*szservername* \[ in\]
</dt> <dd>

Ein Zeiger auf eine mit NULL endenden Zeichenfolge, die den Namen des Servers enthält, für den die Sicherungs Protokollnummer festgelegt werden soll. Vorangehende umgekehrte Schrägstriche sind optional. Der Server muss derselbe Computer sein, von dem diese Funktion aufgerufen wird. Der Servername darf keine Unterstriche ( \_ ) enthalten. Ein Beispiel für einen Servernamen ist " \\ \\ Server1".

</dd> <dt>

*dwcurrentlog* \[ in\]
</dt> <dd>

Enthält die festzulegende Sicherungs Protokollnummer.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **S \_ OK** zurück, wenn die Funktion erfolgreich ist, andernfalls ein Win32-oder RPC-Fehlercode. In der folgenden Liste sind die möglichen Fehlercodes aufgeführt.

<dl> <dt>

**Fehler bei \_ ungültigem \_ Parameter**
</dt> <dd>

Mindestens ein Parameter ist ungültig.

</dd> <dt>

**Fehler \_ nicht \_ genügend Arbeits \_ Speicher**
</dt> <dd>

Es ist ein Fehler bei der Speicher Belegung aufgetreten.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Es ist normalerweise nicht erforderlich, die **dssetcurrentbackuplog** -Funktion aufzurufen. Die Sicherungsfunktionen bestimmen und legen die zuletzt gesicherte Protokollnummer automatisch fest. Verwenden Sie **dssetcurrentbackuplog** , um zu verhindern, dass eine andere inkrementelle Sicherung erfolgreich durchgeführt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Ntdsbcli. h</dt> </dl>   |
| Bibliothek<br/>                  | <dl> <dt>Ntdsbcli. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **Dssetcurrentbackuplogw** (Unicode) und **dssetcurrentbackuploga** (ANSI)<br/>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Sichern und Wiederherstellen eines Active Directory Servers](backing-up-and-restoring-an-active-directory-server.md)
</dt> <dt>

[Verzeichnis Sicherungsfunktionen](directory-backup-functions.md)
</dt> </dl>

 

