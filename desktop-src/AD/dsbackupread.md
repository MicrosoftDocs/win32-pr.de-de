---
title: DsBackupRead-Funktion (Ntdsbcli.h)
description: Liest einen Datenblock aus der aktuellen geöffneten Datei in einen Puffer.
ms.assetid: 01576d41-3cd6-4540-966b-7d98561f7b8c
ms.tgt_platform: multiple
keywords:
- DsBackupRead-Funktion Active Directory
topic_type:
- apiref
api_name:
- DsBackupRead
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16b5ea4da5b004bb4584eb119419b8c89658f36fed7e8c47514bae47d44e31b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118430002"
---
# <a name="dsbackupread-function"></a>DsBackupRead-Funktion

\[Diese Funktion ist für die Verwendung in den Im Abschnitt Anforderungen angegebenen Betriebssystemen verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Ab Windows Vista verwenden Sie stattdessen [Volumeschattenkopie-Dienst (VSS).](../vss/volume-shadow-copy-service-overview.md)\]

Die **DsBackupRead-Funktion** liest einen Datenblock aus der aktuellen geöffneten Datei in einen Puffer. Es wird erwartet, dass die Clientanwendung diese Funktion wiederholt aufruft, bis die gesamte Sicherungsdatei empfangen wurde. Die [**DsBackupOpenFile-Funktion**](dsbackupopenfile.md) bietet die gesamte Größe der Sicherungsdatei.

## <a name="syntax"></a>Syntax


```C++
HRESULT DsBackupRead(
  _In_  HBC    hbc,
  _In_  PVOID  pvBuffer,
  _In_  DWORD  cbBuffer,
  _Out_ PDWORD pcbRead
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hbc* \[ In\]
</dt> <dd>

Enthält das Sicherungskontexthand handle, das mit der [**DsBackupPrepare-Funktion ermittelt**](dsbackupprepare.md) wurde.

</dd> <dt>

*pvBuffer* \[ In\]
</dt> <dd>

Zeiger auf einen Puffer, der die Daten empfängt. Dieser Puffer muss mindestens die *Größe cbBuffer-Bytes* haben.

</dd> <dt>

*cbBuffer* \[ In\]
</dt> <dd>

Enthält die Größe des Puffers bei *pvBuffer* in Bytes. Dieser Wert muss ein Vielfaches von 8192 und größer oder gleich 24576 sein.

</dd> <dt>

*vorlesen* \[ out\]
</dt> <dd>

Zeiger auf einen **DWORD-Wert,** der die tatsächliche Anzahl gelesener Bytes empfängt. Dies kann kleiner als die Anzahl der angeforderten Bytes sein, da einige Transporte den übertragenen Puffer fragmentieren, anstatt den gesamten Puffer mit Daten zu füllen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **S \_ OK zurück,** wenn die Funktion erfolgreich ist, andernfalls ein Win32- oder RPC-Fehlercode. Mögliche Fehlercodes:

<dl> <dt>

**FEHLER \_ UNGÜLTIGER \_ PARAMETER**
</dt> <dd>

Mindestens ein Parameter ist ungültig.

</dd> <dt>

**FEHLERHAND \_ \_ HANDLE EOF**
</dt> <dd>

Das Ende der Sicherungsdatei wurde erreicht.

</dd> </dl>

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

[**DsBackupOpenFile**](dsbackupopenfile.md)
</dt> <dt>

[**DsBackupPrepare**](dsbackupprepare.md)
</dt> <dt>

[**DsBackupFree**](dsbackupfree.md)
</dt> <dt>

[Sichern eines Active Directory-Servers](backing-up-an-active-directory-server.md)
</dt> <dt>

[Verzeichnissicherungsfunktionen](directory-backup-functions.md)
</dt> </dl>

 

