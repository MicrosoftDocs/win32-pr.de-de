---
title: Dsbackupread-Funktion (ntdsbcli. h)
description: Liest einen Datenblock aus der aktuellen geöffneten Datei in einen Puffer.
ms.assetid: 01576d41-3cd6-4540-966b-7d98561f7b8c
ms.tgt_platform: multiple
keywords:
- Dsbackupread-Funktion Active Directory
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
ms.openlocfilehash: 409c2a7d93503aad4edff88070c0458efc961d23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949783"
---
# <a name="dsbackupread-function"></a>Dsbackupread-Funktion

\[Diese Funktion ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Verwenden Sie ab Windows Vista [Volumeschattenkopie-Dienst (VSS)](../vss/volume-shadow-copy-service-overview.md) .\]

Die **dsbackupread** -Funktion liest einen Datenblock aus der aktuellen geöffneten Datei in einen Puffer. Es wird erwartet, dass die Client Anwendung diese Funktion wiederholt aufruft, bis die gesamte Sicherungsdatei empfangen wurde. Die [**dsbackupopenfile**](dsbackupopenfile.md) -Funktion stellt die gesamte Größe der Sicherungsdatei bereit.

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

*HBC* \[ in\]
</dt> <dd>

Enthält das Sicherungs Kontext Handle, das mit der [**dsbackupprepare**](dsbackupprepare.md) -Funktion abgerufen wurde.

</dd> <dt>

*pvbuffer* \[ in\]
</dt> <dd>

Zeiger auf einen Puffer, der die Daten empfängt. Dieser Puffer muss mindestens eine Größe von *cbbuffer* Bytes aufweisen.

</dd> <dt>

*cbbuffer* \[ in\]
</dt> <dd>

Enthält die Größe (in Bytes) des Puffers bei *pvbuffer*. Dieser Wert muss ein Vielfaches von 8192 sein und muss größer oder gleich 24576 sein.

</dd> <dt>

*pcbread* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen **DWORD** -Wert, der die tatsächliche Anzahl von gelesenen Bytes empfängt. Dies kann weniger als die Anzahl der angeforderten Bytes sein, da einige Transporte den übertragenen Puffer fragmentieren, anstatt den gesamten Puffer mit Daten zu füllen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **S \_ OK** zurück, wenn die Funktion erfolgreich ist, andernfalls ein Win32-oder RPC-Fehlercode. Folgende Fehlercodes sind möglich:

<dl> <dt>

**Fehler bei \_ ungültigem \_ Parameter**
</dt> <dd>

Mindestens ein Parameter ist ungültig.

</dd> <dt>

**Fehler \_ handle \_ EOF**
</dt> <dd>

Das Ende der Sicherungsdatei wurde erreicht.

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

[**Dsbackupfree**](dsbackupfree.md)
</dt> <dt>

[Sichern eines Active Directory Servers](backing-up-an-active-directory-server.md)
</dt> <dt>

[Verzeichnis Sicherungsfunktionen](directory-backup-functions.md)
</dt> </dl>

 

