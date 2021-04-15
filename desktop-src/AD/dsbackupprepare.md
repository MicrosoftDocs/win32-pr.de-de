---
title: Dsbackupprepare-Funktion (ntdsbcli. h)
description: Bereitet das Verzeichnis auf dem angegebenen Server für die Online Sicherung vor und gibt ein Sicherungs Kontext Handle zurück, das bei nachfolgenden Aufrufen anderer Sicherungsfunktionen verwendet wird.
ms.assetid: 18c6dbcf-b707-4674-9af5-40f2178e6d2b
ms.tgt_platform: multiple
keywords:
- Dsbackupprepare-Funktions Active Directory
topic_type:
- apiref
api_name:
- DsBackupPrepare
- DsBackupPrepareA
- DsBackupPrepareW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa561a7e41164ece68fb18fd882a8b05d6357cec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477133"
---
# <a name="dsbackupprepare-function"></a>Dsbackupprepare-Funktion

\[Diese Funktion ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Verwenden Sie ab Windows Vista [Volumeschattenkopie-Dienst (VSS)](../vss/volume-shadow-copy-service-overview.md) .\]

Die **dsbackupprepare** -Funktion bereitet das Verzeichnis auf dem angegebenen Server für die Online Sicherung vor und gibt ein Sicherungs Kontext Handle zurück, das bei nachfolgenden Aufrufen anderer Sicherungsfunktionen verwendet wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT DsBackupPrepare(
  _In_  LPCTSTR szBackupServer,
  _In_  ULONG   grbit,
  _In_  ULONG   btBackupType,
  _Out_ PVOID   *ppvExpiryToken,
  _Out_ LPDWORD pcbExpiryTokenSize,
  _Out_ HBC     *phbc
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*szbackupserver* \[ in\]
</dt> <dd>

Zeiger auf eine mit NULL endenden Zeichenfolge, die den Namen des zu sichernden Servers enthält. Vorangehende umgekehrte Schrägstriche sind optional. Der Server muss derselbe Computer sein, von dem diese Funktion aufgerufen wird. Der Servername darf keinen Unterstrich ( \_ ) enthalten. Ein Beispiel für einen Servernamen ist " \\ \\ Server1".

</dd> <dt>

*grbit* \[ in\]
</dt> <dd>

Bestimmt, ob die Protokolldateien gesichert werden. Dieser Wert sollte immer 0 sein, da inkrementelle Sicherungen nicht unterstützt werden.

</dd> <dt>

*btbackuptype* \[ in\]
</dt> <dd>

Gibt den Sicherungstyp an. Dies kann einer der folgenden Werte sein:

<dt>

<span id="BACKUP_TYPE_FULL"></span><span id="backup_type_full"></span>

<span id="BACKUP_TYPE_FULL"></span><span id="backup_type_full"></span>**\_Sicherungstyp \_ voll**


</dt> <dd>

Gibt eine vollständige Sicherung an. Das komplette Verzeichnis (DIT, Protokolldateien und Update Dateien) wird gesichert. Alle Daten werden gesichert, und die Transaktionsprotokoll Dateien werden abgeschnitten. Es werden nur vollständige Sicherungen unterstützt.

</dd> <dt>

<span id="BACKUP_TYPE_LOGS_ONLY"></span><span id="backup_type_logs_only"></span>

<span id="BACKUP_TYPE_LOGS_ONLY"></span><span id="backup_type_logs_only"></span>**\_nur Sicherungs Typen \_ Protokolle \_**


</dt> <dd>

Dieser Wert wird nicht unterstützt. Gibt an, dass nur die Daten Bank Protokolle und nicht die Datenbank selbst gesichert werden. Dies wird normalerweise beim Ausführen einer differenziellen oder inkrementellen Sicherung verwendet.

</dd> <dt>

<span id="BACKUP_TYPE_INCREMENTAL"></span><span id="backup_type_incremental"></span>

<span id="BACKUP_TYPE_INCREMENTAL"></span><span id="backup_type_incremental"></span>**\_Sicherungstyp \_**


</dt> <dd>

Dieser Wert wird nicht unterstützt. **Dsbackupprepare** gibt **einen \_ ungültigen \_ Parameter** zurück.

</dd> </dl> </dd> <dt>

*ppvexpiriytoken* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen **pVoid** -Wert, der einen Zeiger auf ein Ablauf Token empfängt, das dieser Sicherung zugeordnet ist. *pcbexpirytekensize* erhält die Größe dieser Daten in Bytes. Der Aufrufer muss den Inhalt dieses Tokens mit der Sicherung speichern, da das Token an [**dsrestoreprepare**](dsrestoreprepare.md) übergeben werden muss, wenn versucht wird, Daten wiederherzustellen. Nachdem das Token gespeichert wurde und nicht mehr benötigt wird, muss der Aufrufer den zugeordneten Arbeitsspeicher mithilfe von [**dsbackupfree**](dsbackupfree.md)freigeben.

</dd> <dt>

*pcbexpirytekensize* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen **DWORD** -Wert, der die Größe des Tokens in *ppvexpiriytoken* in Bytes empfängt.

</dd> <dt>

*phbC* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen **HBC** -Wert, der das Handle für die Sicherung empfängt. Dieses Handle wird verwendet, wenn andere Verzeichnisdienst-Sicherungsfunktionen aufgerufen werden, wie z. b. [**dsbackupopenfile**](dsbackupopenfile.md) und [**dsbackupend**](dsbackupend.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **S \_ OK** zurück, wenn die Funktion erfolgreich ist, andernfalls einen Fehlercode. In der folgenden Liste sind andere mögliche Fehlercodes aufgeführt.

<dl> <dt>

**Fehler \_ Zugriff \_ verweigert**
</dt> <dd>

Der Aufrufer verfügt nicht über die erforderlichen Zugriffsberechtigungen, um diese Funktion aufzurufen. Die [**dssetauthidentity**](dssetauthidentity.md) -Funktion kann verwendet werden, um die Anmelde Informationen festzulegen, die für die Sicherungs-und Wiederherstellungs Funktionen verwendet werden sollen.

</dd> <dt>

**Fehler bei \_ ungültigem \_ Parameter**
</dt> <dd>

" *szbackupserver* " oder " *phbcbackupcontext* " sind ungültig.

</dd> <dt>

**Fehler \_ nicht \_ genügend Arbeits \_ Speicher**
</dt> <dd>

Es ist ein Fehler bei der Speicher Belegung aufgetreten.

</dd> <dt>

**hrcouldnotconnect**
</dt> <dd>

Der Server in " *szbackupserver* " wurde nicht gefunden, ist kein Domänen Controller, oder " *szbackupserver* " ist nicht ordnungsgemäß formatiert. Dieser Wert wird in "ntdsbmsg. h" definiert.

</dd> <dt>

**hrinvalidparam**
</dt> <dd>

*ppvexpiriytoken* und/oder *pcbexpirytokensize* sind ungültig. Dieser Wert wird in "ntdsbmsg. h" definiert.

</dd> <dt>

**\_ungültige RPC S- \_ \_ Bindung**
</dt> <dd>

Die Funktion wird Remote aufgerufen, oder der Server in " *szservername* " ist kein Domänen Controller.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Funktion erfordert, dass der Aufrufer über die Berechtigung " **SE \_ Backup \_ Name** " verfügt. Die [**dssetauthidentity**](dssetauthidentity.md) -Funktion kann verwendet werden, um den Sicherheitskontext zu ändern, in dem diese Funktion aufgerufen wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Ntdsbcli. h</dt> </dl>   |
| Bibliothek<br/>                  | <dl> <dt>Ntdsbcli. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **Dsbackuppreparew** (Unicode) und **dsbackuppreparea** (ANSI)<br/>               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Dsrestoreprepare**](dsrestoreprepare.md)
</dt> <dt>

[**Dsbackupfree**](dsbackupfree.md)
</dt> <dt>

[**Dsbackupopenfile**](dsbackupopenfile.md)
</dt> <dt>

[**Dsbackupend**](dsbackupend.md)
</dt> <dt>

[**Dssetauthidentity**](dssetauthidentity.md)
</dt> <dt>

[Sichern eines Active Directory Servers](backing-up-an-active-directory-server.md)
</dt> <dt>

[Verzeichnis Sicherungsfunktionen](directory-backup-functions.md)
</dt> </dl>

 

