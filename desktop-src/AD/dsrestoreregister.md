---
title: Dsrestoreregiester-Funktion (ntdsbcli. h)
description: Registriert einen Wiederherstellungs Vorgang.
ms.assetid: 83a56985-89be-4a95-9a8d-7c6f78d61c9a
ms.tgt_platform: multiple
keywords:
- Dsrestoreregiester-Funktion Active Directory
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
ms.openlocfilehash: 610d49c73ade9bab47c95e90af73bac606f4bd23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040727"
---
# <a name="dsrestoreregister-function"></a>Dsrestoreregiester-Funktion

\[Diese Funktion ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Verwenden Sie ab Windows Vista [Volumeschattenkopie-Dienst (VSS)](../vss/volume-shadow-copy-service-overview.md) .\]

Die **dsrestoreregiester** -Funktion registriert einen Wiederherstellungs Vorgang. Diese Funktion intersperrt alle nachfolgenden Wiederherstellungs Vorgänge und verhindert, dass das Wiederherstellungs Ziel gestartet wird, bis die [**dsrestoreregistercomplete**](dsrestoreregistercomplete.md) -Funktion aufgerufen wird.

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

*HBC* \[ in\]
</dt> <dd>

Enthält das Wiederherstellungs Kontext Handle, das mit der [**dsrestoreprepare**](dsrestoreprepare.md) -Funktion abgerufen wurde.

</dd> <dt>

*szcheckpointfilepath* \[ in\]
</dt> <dd>

Zeiger auf eine mit NULL endenden Zeichenfolge, die den Pfad der Prüf Punkt Datei enthält. Dieser Pfad wird von der [**dsrestoregetdatabaselocations**](dsrestoregetdatabaselocations.md) -Funktion bereitgestellt und verfügt über einen **bft** -Wert von **bft \_ Checkpoint \_ dir**. Dies entspricht in der Regel dem Pfad der Systemdatenbank. Dieser Pfad ist für eine ordnungsgemäße Sicherungs Wiederherstellungs Funktion erforderlich. Dieser Parameter darf nicht **null** sein. Wenn Sie **null** in diesem Parameter übergeben, tritt während des Wiederherstellungs Vorgangs ein Fehler auf.

</dd> <dt>

*szlogpath* \[ in\]
</dt> <dd>

Zeiger auf eine auf NULL endende Zeichenfolge, die den Pfad enthält, in dem die Protokolldateien wieder hergestellt werden. Dieser Pfad wird von der [**dsrestoregetdatabaselocations**](dsrestoregetdatabaselocations.md) -Funktion bereitgestellt und hat den **bft** -Wert **bft \_ log \_ dir**. Wenn der Pfad auf ein leeres Verzeichnis verweist, werden neue Protokolldateien erstellt. Dieser Parameter darf nicht **null** sein.

</dd> <dt>

*rgrstmap* \[ in\]
</dt> <dd>

Ein Array von [**EDB- \_ rstmap**](edb-rstmap.md) -Strukturen, das die alten und neuen Pfade für die einzelnen Datenbanken enthält. Es gibt eine Struktur für jede Datenbank. Für das Verzeichnis gibt es eine Struktur für die Systemdatenbank und eine andere Struktur für die Verzeichnis Datenbank. Die Reihenfolge der Elemente im Array spielt keine Rolle. Der *crstmap* -Parameter enthält die Anzahl der Elemente im Array.

</dd> <dt>

*crstmap* \[ in\]
</dt> <dd>

Enthält die Anzahl der Elemente im *rgrstmap* -Array.

</dd> <dt>

*szbackuplogpath* \[ in\]
</dt> <dd>

Zeiger auf eine mit NULL endenden Zeichenfolge, die den Pfad enthält, in dem sich die gesicherten Protokolldateien befinden. Dieser Parameter darf nicht **null** sein.

</dd> <dt>

*genlow* \[ in\]
</dt> <dd>

Enthält die niedrigste Protokollnummer, die in dieser Wiederherstellungs Sitzung wieder hergestellt werden soll. Dabei handelt es sich um eine hexadezimale Zahl im Bereich von 0x00000 bis 0xFFFFF.

</dd> <dt>

*genhoch* \[ in\]
</dt> <dd>

Enthält die höchste Protokollnummer, die in dieser Wiederherstellungs Sitzung wieder hergestellt werden soll. Dabei handelt es sich um eine hexadezimale Zahl im Bereich von 0x00000 bis 0xFFFFF.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **S \_ OK** zurück, wenn die Funktion erfolgreich ist, andernfalls ein Win32-oder RPC-Fehlercode. In der folgenden Liste sind die möglichen Fehlercodes aufgeführt.

<dl> <dt>

**Fehler \_ Zugriff \_ verweigert**
</dt> <dd>

Der Aufrufer verfügt nicht über die erforderlichen Zugriffsberechtigungen, um diese Funktion aufzurufen. Die [**dssetauthidentity**](dssetauthidentity.md) -Funktion kann verwendet werden, um die Anmelde Informationen festzulegen, die für die Sicherungs-und Wiederherstellungs Funktionen verwendet werden sollen.

</dd> <dt>

**Fehler bei \_ ungültigem \_ Parameter**
</dt> <dd>

Mindestens ein Parameter ist ungültig.

</dd> <dt>

**hrmissingexpirytoken**
</dt> <dd>

Das für [**dsrestoreprepare**](dsrestoreprepare.md) bereitgestellte Ablauf Token war ungültig. Dieser Wert wird in "ntdsbmsg. h" definiert.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Ntdsbcli. h</dt> </dl>   |
| Bibliothek<br/>                  | <dl> <dt>Ntdsbcli. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **Dsrestoreregisterw** (Unicode) und **dsrestoreregistera** (ANSI)<br/>           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Dsrestoreregistercomplete**](dsrestoreregistercomplete.md)
</dt> <dt>

[**Dsrestoreprepare**](dsrestoreprepare.md)
</dt> <dt>

[**Dsrestoregetdatabaselocations**](dsrestoregetdatabaselocations.md)
</dt> <dt>

[**Dsrestoreend**](dsrestoreend.md)
</dt> <dt>

[**EDB- \_ rstmap**](edb-rstmap.md)
</dt> <dt>

[Wiederherstellen von Active Directory](restoring-an-active-directory-server.md)
</dt> <dt>

[Verzeichnis Sicherungsfunktionen](directory-backup-functions.md)
</dt> </dl>

 

