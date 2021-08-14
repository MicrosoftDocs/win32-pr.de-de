---
title: DsBackupPrepare-Funktion (Ntdsbcli.h)
description: Bereitet das Verzeichnis auf dem angegebenen Server für die Onlinesicherung vor und gibt ein Sicherungskontexthandle zurück, das in nachfolgenden Aufrufen anderer Sicherungsfunktionen verwendet wird.
ms.assetid: 18c6dbcf-b707-4674-9af5-40f2178e6d2b
ms.tgt_platform: multiple
keywords:
- Active Directory-Funktion "DsBackupPrepare"
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
ms.openlocfilehash: ea1f24c6cbf3f05ce69d8a71900bfe4d1b08899b98590dc75410b9d5ed92d90a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118191836"
---
# <a name="dsbackupprepare-function"></a>DsBackupPrepare-Funktion

\[Diese Funktion ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Verwenden Sie ab Windows Vista stattdessen [Volumeschattenkopie-Dienst (VSS).](../vss/volume-shadow-copy-service-overview.md)\]

Die **DsBackupPrepare-Funktion** bereitet das Verzeichnis auf dem angegebenen Server für die Onlinesicherung vor und gibt ein Sicherungskontexthandle zurück, das in nachfolgenden Aufrufen anderer Sicherungsfunktionen verwendet wird.

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

*szBackupServer* \[ In\]
</dt> <dd>

Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des zu sichernden Servers enthält. Die vorangehenden umgekehrten Schrägstriche sind optional. Der Server muss derselbe Computer sein, von dem diese Funktion aufgerufen wird. Der Servername darf keinen Unterstrich \_ () enthalten. Ein Beispiel für einen Servernamen ist \\ \\ "server1".

</dd> <dt>

*grbit* \[ In\]
</dt> <dd>

Bestimmt, ob die Protokolldateien gesichert werden. Dieser Wert sollte immer 0 sein, da inkrementelle Sicherungen nicht unterstützt werden.

</dd> <dt>

*btBackupType* \[ In\]
</dt> <dd>

Gibt den Sicherungstyp an. Dies kann einer der folgenden Werte sein.

<dt>

<span id="BACKUP_TYPE_FULL"></span><span id="backup_type_full"></span>

<span id="BACKUP_TYPE_FULL"></span><span id="backup_type_full"></span>**BACKUP \_ TYPE \_ FULL**


</dt> <dd>

Gibt eine vollständige Sicherung an. Das vollständige Verzeichnis (DIT, Protokolldateien und Updatedateien) wird gesichert. Alle Daten werden gesichert, und Transaktionsprotokolldateien werden abgeschnitten. Es werden nur vollständige Sicherungen unterstützt.

</dd> <dt>

<span id="BACKUP_TYPE_LOGS_ONLY"></span><span id="backup_type_logs_only"></span>

<span id="BACKUP_TYPE_LOGS_ONLY"></span><span id="backup_type_logs_only"></span>**\_NUR \_ SICHERUNGSTYPPROTOKOLLE \_**


</dt> <dd>

Dieser Wert wird nicht unterstützt. Gibt an, dass nur die Datenbankprotokolle und nicht die Datenbank selbst gesichert werden. Dies wird normalerweise beim Ausführen einer differenziellen oder inkrementellen Sicherung verwendet.

</dd> <dt>

<span id="BACKUP_TYPE_INCREMENTAL"></span><span id="backup_type_incremental"></span>

<span id="BACKUP_TYPE_INCREMENTAL"></span><span id="backup_type_incremental"></span>**SICHERUNGSTYP \_ \_ INKREMENTELL**


</dt> <dd>

Dieser Wert wird nicht unterstützt. **DsBackupPrepare** gibt **ERROR \_ INVALID \_ PARAMETER** zurück.

</dd> </dl> </dd> <dt>

*ppvExpiryToken* \[ out\]
</dt> <dd>

Zeiger auf einen **PVOID-Wert,** der einen Zeiger auf ein Ablauftoken empfängt, das dieser Sicherung zugeordnet ist. *"pwExpiryTokenSize"* empfängt die Größe dieser Daten in Bytes. Der Aufrufer muss den Inhalt dieses Tokens mit der Sicherung speichern, da das Token beim Wiederherstellen von Daten an [**DsRestorePrepare**](dsrestoreprepare.md) übergeben werden muss. Nachdem das Token gespeichert wurde und nicht mehr benötigt wird, sollte der Aufrufer den zugeordneten Arbeitsspeicher mithilfe von [**DsBackupFree**](dsbackupfree.md)freigeben.

</dd> <dt>

*pwExpiryTokenSize* \[ out\]
</dt> <dd>

Zeiger auf einen **DWORD-Wert,** der die Größe des Tokens in *ppvExpiryToken* in Bytes empfängt.

</dd> <dt>

*phbc* \[ out\]
</dt> <dd>

Zeiger auf einen **HBC-Wert,** der das Handle für die Sicherung empfängt. Dieses Handle wird verwendet, wenn andere Verzeichnisdienst-Sicherungsfunktionen wie [**DsBackupOpenFile**](dsbackupopenfile.md) und [**DsBackupEnd**](dsbackupend.md)aufgerufen werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **S \_ OK** zurück, wenn die Funktion erfolgreich ist, oder andernfalls ein Fehlercode. In der folgenden Liste sind weitere mögliche Fehlercodes aufgeführt.

<dl> <dt>

**FEHLERZUGRIFF \_ \_ VERWEIGERT**
</dt> <dd>

Der Aufrufer verfügt nicht über die richtigen Zugriffsberechtigungen zum Aufrufen dieser Funktion. Die [**DsSetAuthIdentity-Funktion**](dssetauthidentity.md) kann verwendet werden, um die Anmeldeinformationen festzulegen, die für die Sicherungs- und Wiederherstellungsfunktionen verwendet werden sollen.

</dd> <dt>

**FEHLER: \_ UNGÜLTIGER \_ PARAMETER**
</dt> <dd>

*szBackupServer* oder *phbcBackupContext* sind ungültig.

</dd> <dt>

**FEHLER \_ NICHT \_ GENÜGEND \_ ARBEITSSPEICHER**
</dt> <dd>

Fehler bei der Speicherbelegung.

</dd> <dt>

**hrConnectNotConnect**
</dt> <dd>

Der Server in *szBackupServer* wurde nicht gefunden, ist kein Domänencontroller, oder *szBackupServer* ist nicht ordnungsgemäß formatiert. Dieser Wert wird in ntdsbmsg.h definiert.

</dd> <dt>

**hrInvalidParam**
</dt> <dd>

*ppvExpiryToken* und/oder *pwExpiryTokenSize* sind ungültig. Dieser Wert ist in Ntdsbmsg.h definiert.

</dd> <dt>

**\_RPC S \_ UNGÜLTIGE \_ BINDUNG**
</dt> <dd>

Die Funktion wird remote aufgerufen, oder der Server in *szServerName* ist kein Domänencontroller.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Funktion erfordert, dass der Aufrufer über die **berechtigung SE \_ BACKUP \_ NAME** verfügt. Die [**DsSetAuthIdentity-Funktion**](dssetauthidentity.md) kann verwendet werden, um den Sicherheitskontext zu ändern, unter dem diese Funktion aufgerufen wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Ntdsbcli.h</dt> </dl>   |
| Bibliothek<br/>                  | <dl> <dt>Ntdsbcli.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **DsBackupPrepareW** (Unicode) und **DsBackupPrepareA** (ANSI)<br/>               |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**DsRestorePrepare**](dsrestoreprepare.md)
</dt> <dt>

[**DsBackupFree**](dsbackupfree.md)
</dt> <dt>

[**DsBackupOpenFile**](dsbackupopenfile.md)
</dt> <dt>

[**DsBackupEnd**](dsbackupend.md)
</dt> <dt>

[**DsSetAuthIdentity**](dssetauthidentity.md)
</dt> <dt>

[Sichern eines Active Directory-Servers](backing-up-an-active-directory-server.md)
</dt> <dt>

[Verzeichnissicherungsfunktionen](directory-backup-functions.md)
</dt> </dl>

 

