---
title: DsRestoreRegister-Funktion (Ntdsbcli.h)
description: Registriert einen Wiederherstellungsvorgang.
ms.assetid: 83a56985-89be-4a95-9a8d-7c6f78d61c9a
ms.tgt_platform: multiple
keywords:
- DsRestoreRegister-Funktion Active Directory
topic_type:
- apiref
api_name:
- DsRestoreRegister
- DsRestoreRegisterA
- DsRestoreRegisterW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3e878a5d2b9567ae7a483344a2240d3480620ea00706db1ed0c834fd2c5553a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962459"
---
# <a name="dsrestoreregister-function"></a>DsRestoreRegister-Funktion

\[Diese Funktion ist für die Verwendung in den Im Abschnitt Anforderungen angegebenen Betriebssystemen verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Ab Windows Vista verwenden Sie stattdessen [Volumeschattenkopie-Dienst (VSS).](../vss/volume-shadow-copy-service-overview.md)\]

Die **DsRestoreRegister-Funktion** registriert einen Wiederherstellungsvorgang. Diese Funktion interlockt alle nachfolgenden Wiederherstellungsvorgänge und verhindert, dass das Wiederherstellungsziel gestartet wird, bis die [**DsRestoreRegisterComplete-Funktion**](dsrestoreregistercomplete.md) aufgerufen wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT DsRestoreRegister(
  _In_ HBC        hbc,
  _In_ LPCTSTR    szCheckPointFilePath,
  _In_ LPCTSTR    szLogPath,
  _In_ EDB_RSTMAP rgrstmap[],
  _In_ LONG       crstmap,
  _In_ LPCTSTR    szBackupLogPath,
  _In_ ULONG      genLow,
  _In_ ULONG      genHigh
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hbc* \[ In\]
</dt> <dd>

Enthält das Wiederherstellungskontexthand handle, das mit der [**DsRestorePrepare-Funktion ermittelt**](dsrestoreprepare.md) wurde.

</dd> <dt>

*szCheckPointFilePath* \[ In\]
</dt> <dd>

Zeiger auf eine auf NULL beendete Zeichenfolge, die den Pfad zur Prüfpunktdatei enthält. Dieser Pfad wird von der [**DsRestoreGetDatabaseLocations-Funktion**](dsrestoregetdatabaselocations.md) bereitgestellt und hat den **BFT-Wert** **BFT \_ CHECKPOINT \_ DIR**. In der Regel ist dies mit dem Pfad der Systemdatenbank identisch. Dieser Pfad ist für die ordnungsgemäße Sicherungswiederherstellungsfunktion erforderlich. Dieser Parameter darf nicht **NULL sein.** Die Übergabe von **NULL** in diesem Parameter verursacht während des Wiederherstellungsprozesses einen Fehler.

</dd> <dt>

*szLogPath* \[ In\]
</dt> <dd>

Zeiger auf eine auf NULL beendete Zeichenfolge, die den Pfad enthält, in dem die Protokolldateien wiederhergestellt werden. Dieser Pfad wird von der [**DsRestoreGetDatabaseLocations-Funktion**](dsrestoregetdatabaselocations.md) bereitgestellt und hat den **BFT-Wert** **BFT \_ LOG \_ DIR**. Wenn der Pfad auf ein leeres Verzeichnis verweist, werden dort neue Protokolldateien erstellt. Dieser Parameter darf nicht **NULL sein.**

</dd> <dt>

*rgrstmap* \[ In\]
</dt> <dd>

Ein Array von [**EDB-RSTMAP-Strukturen, \_**](edb-rstmap.md) das die alten und neuen Pfade für jede Datenbank enthält. Es gibt eine Struktur für jede Datenbank. Für das Verzeichnis gibt es eine Struktur für die Systemdatenbank und eine andere Struktur für die Verzeichnisdatenbank. Die Reihenfolge der Elemente im Array spielt keine Rolle. Der *crstmap-Parameter* enthält die Anzahl der Elemente im Array.

</dd> <dt>

*crstmap* \[ In\]
</dt> <dd>

Enthält die Anzahl der Elemente im *rgrstmap-Array.*

</dd> <dt>

*szBackupLogPath* \[ In\]
</dt> <dd>

Zeiger auf eine auf NULL beendete Zeichenfolge, die den Pfad enthält, in dem sich die sichern Protokolldateien derzeit befinden. Dieser Parameter darf nicht **NULL sein.**

</dd> <dt>

*genLow* \[ In\]
</dt> <dd>

Enthält die niedrigste Protokollnummer, die in dieser Wiederherstellungssitzung wiederhergestellt werden soll. Dies ist eine Hexadezimalzahl im Bereich von 0x00000 bis 0xFFFFF.

</dd> <dt>

*genHigh* \[ In\]
</dt> <dd>

Enthält die höchste Protokollnummer, die in dieser Wiederherstellungssitzung wiederhergestellt werden soll. Dies ist eine Hexadezimalzahl im Bereich von 0x00000 bis 0xFFFFF.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **S \_ OK zurück,** wenn die Funktion erfolgreich ist, andernfalls ein Win32- oder RPC-Fehlercode. In der folgenden Liste sind mögliche Fehlercodes aufgeführt.

<dl> <dt>

**FEHLER \_ BEIM \_ ZUGRIFF VERWEIGERT**
</dt> <dd>

Der Aufrufer verfügt nicht über die richtigen Zugriffsberechtigungen zum Aufrufen dieser Funktion. Mit [**der DsSetAuthIdentity-Funktion**](dssetauthidentity.md) können die Anmeldeinformationen festgelegt werden, die für die Sicherungs- und Wiederherstellungsfunktionen verwendet werden sollen.

</dd> <dt>

**FEHLER \_ UNGÜLTIGER \_ PARAMETER**
</dt> <dd>

Mindestens ein Parameter ist ungültig.

</dd> <dt>

**hrMissingExpiryToken**
</dt> <dd>

Das für [**DsRestorePrepare angegebene Ablauftoken war**](dsrestoreprepare.md) ungültig. Dieser Wert wird in Ntdsbmsg.h definiert.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Ntdsbcli.h</dt> </dl>   |
| Bibliothek<br/>                  | <dl> <dt>Ntdsbcli.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **DsRestoreRegisterW** (Unicode) und **DsRestoreRegisterA** (ANSI)<br/>           |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**DsRestoreRegisterComplete**](dsrestoreregistercomplete.md)
</dt> <dt>

[**DsRestorePrepare**](dsrestoreprepare.md)
</dt> <dt>

[**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md)
</dt> <dt>

[**DsRestoreEnd**](dsrestoreend.md)
</dt> <dt>

[**EDB \_ RSTMAP**](edb-rstmap.md)
</dt> <dt>

[Wiederherstellen von Active Directory](restoring-an-active-directory-server.md)
</dt> <dt>

[Verzeichnissicherungsfunktionen](directory-backup-functions.md)
</dt> </dl>

 

