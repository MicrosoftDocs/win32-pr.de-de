---
title: DsSetCurrentBackupLog-Funktion (Ntdsbcli.h)
description: Legt die aktuelle Sicherungsprotokollnummer nach einer erfolgreichen Wiederherstellung fest.
ms.assetid: 903bddea-c5a7-4b3f-819c-0467a9c5ae1b
ms.tgt_platform: multiple
keywords:
- DsSetCurrentBackupLog-Funktion Active Directory
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
ms.openlocfilehash: ab10ac21d1a3cb2501a809b938252414c756bdfbd62f1e142ba3b902cde8c291
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118191779"
---
# <a name="dssetcurrentbackuplog-function"></a>DsSetCurrentBackupLog-Funktion

\[Diese Funktion ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Verwenden Sie ab Windows Vista stattdessen [Volumeschattenkopie-Dienst (VSS).](../vss/volume-shadow-copy-service-overview.md)\]

Die **DsSetCurrentBackupLog-Funktion** legt die aktuelle Sicherungsprotokollnummer nach einer erfolgreichen Wiederherstellung fest. Da Active Directory Domain Services nur die zirkuläre Protokollierung unterstützen, wird diese Funktion normalerweise nicht verwendet.

## <a name="syntax"></a>Syntax


```C++
HRESULT DsSetCurrentBackupLog(
  _In_ LPCWSTR szServerName,
  _In_ DWORD   dwCurrentLog
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*szServerName* \[ In\]
</dt> <dd>

Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des Servers enthält, für den die Sicherungsprotokollnummer festgelegt werden soll. Die vorangehenden umgekehrten Schrägstriche sind optional. Der Server muss derselbe Computer sein, von dem diese Funktion aufgerufen wird. Der Servername darf keinen Unterstrich \_ () enthalten. Ein Beispiel für einen Servernamen ist \\ \\ "server1".

</dd> <dt>

*dwCurrentLog* \[ In\]
</dt> <dd>

Enthält die festzulegende Sicherungsprotokollnummer.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **S \_ OK** zurück, wenn die Funktion erfolgreich ist oder andernfalls ein Win32- oder RPC-Fehlercode vorliegt. In der folgenden Liste sind mögliche Fehlercodes aufgeführt.

<dl> <dt>

**FEHLER: \_ UNGÜLTIGER \_ PARAMETER**
</dt> <dd>

Mindestens ein Parameter ist ungültig.

</dd> <dt>

**FEHLER \_ NICHT \_ GENÜGEND \_ ARBEITSSPEICHER**
</dt> <dd>

Fehler bei der Speicherbelegung.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Normalerweise ist es nicht erforderlich, die **DsSetCurrentBackupLog-Funktion** aufzurufen. Die Sicherungsfunktionen bestimmen automatisch die letzte gesicherte Protokollnummer und legen sie fest. Verwenden Sie **DsSetCurrentBackupLog,** um zu verhindern, dass eine weitere inkrementelle Sicherung erfolgreich ist, bis eine vollständige Sicherung ausgeführt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Ntdsbcli.h</dt> </dl>   |
| Bibliothek<br/>                  | <dl> <dt>Ntdsbcli.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **DsSetCurrentBackupLogW** (Unicode) und **DsSetCurrentBackupLogA** (ANSI)<br/>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Sichern und Wiederherstellen eines Active Directory-Servers](backing-up-and-restoring-an-active-directory-server.md)
</dt> <dt>

[Verzeichnissicherungsfunktionen](directory-backup-functions.md)
</dt> </dl>

 

