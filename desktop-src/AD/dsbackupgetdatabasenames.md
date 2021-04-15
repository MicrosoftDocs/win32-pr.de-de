---
title: Dsbackupgetdatabasenames-Funktion (ntdsbcli. h)
description: Ruft die Liste der Datenbankdateien ab, die für den angegebenen Sicherungs Kontext gesichert werden sollen.
ms.assetid: ba0447a1-38b0-4c0a-8c63-abaefb5b908f
ms.tgt_platform: multiple
keywords:
- Dsbackupgetdatabasenames-Funktion Active Directory
topic_type:
- apiref
api_name:
- DsBackupGetDatabaseNames
- DsBackupGetDatabaseNamesA
- DsBackupGetDatabaseNamesW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6643b17a85727f6e0df4e8deea9609f73afd1e76
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477136"
---
# <a name="dsbackupgetdatabasenames-function"></a>Dsbackupgetdatabasenames-Funktion

\[Diese Funktion ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Verwenden Sie ab Windows Vista [Volumeschattenkopie-Dienst (VSS)](../vss/volume-shadow-copy-service-overview.md) .\]

Die **dsbackupgetdatabasenames** -Funktion Ruft die Liste der Datenbankdateien ab, die für den angegebenen Sicherungs Kontext gesichert werden sollen.

## <a name="syntax"></a>Syntax


```C++
HRESULT DsBackupGetDatabaseNames(
  _In_  HBC     hbc,
  _Out_ LPTSTR  *pszAttachmentInfo,
  _Out_ LPDWORD pcbSize
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*HBC* \[ in\]
</dt> <dd>

Enthält das Sicherungs Kontext Handle, das mit der [**dsbackupprepare**](dsbackupprepare.md) -Funktion abgerufen wurde.

</dd> <dt>

*pszattachmentinfo* \[ vorgenommen\]
</dt> <dd>

Zeiger auf einen Zeichen folgen Zeiger, der die Liste der Daten Bank Dateinamen als UNC-Pfade empfängt. Dieser Wert muss vor dem Aufrufen von **dsbackupgetdatabasenames** mit **null** initialisiert werden.

Diese Liste empfängt eine mit NULL endend beendete Liste mit einzelnen null-terminierten Zeichen folgen.

Dieser Puffer wird von der **dsbackupgetdatabasenames** -Funktion zugeordnet und muss freigegeben werden, wenn er durch Aufrufen der [**dsbackupfree**](dsbackupfree.md) -Funktion nicht mehr benötigt wird.

Das erste Zeichen jedes Datei namens enthält eine der [**bft-Konstanten**](bft-constants.md) , die den Typ des Namens identifiziert. Die [**dsrestoregetdatabaselocations**](dsrestoregetdatabaselocations.md) -Funktion liefert nur die folgenden Typen von Namen.

<dt>

<span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>

<span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>**bft- \_ NTDS- \_ Datenbank**


</dt> <dd>

Die Datei ist eine NTDS-Datenbankdatei. Diese Datei muss in die als **bft \_ NTDS- \_ Datenbank** identifizierte Datei kopiert werden, wenn die Daten wieder hergestellt werden.

</dd> <dt>

<span id="BFT_LOG"></span><span id="bft_log"></span>

<span id="BFT_LOG"></span><span id="bft_log"></span>**bft- \_ Protokoll**


</dt> <dd>

Bei der Datei handelt es sich um eine Protokolldatei. Alle Protokolldateien werden in das Verzeichnis kopiert, das beim Wiederherstellen der Daten als **bft- \_ Protokoll \_** Verzeichnis identifiziert wird.

</dd> <dt>

<span id="BFT_PATCH_FILE"></span><span id="bft_patch_file"></span>

<span id="BFT_PATCH_FILE"></span><span id="bft_patch_file"></span>**bft \_ - \_ Patchdatei**


</dt> <dd>

Bei der Datei handelt es sich um eine Patchdatei. Alle Patchdateien werden beim Wiederherstellen der Daten in **\_ das als \_ bft** -Prüf Punkt Verzeichnis identifizierte Verzeichnis kopiert.

</dd> </dl> </dd> <dt>

*pcbSize* \[ vorgenommen\]
</dt> <dd>

Zeiger auf den **DWORD** -Wert, der die Größe des *pszattachmentinfo* -Puffers in Bytes empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **S \_ OK** zurück, wenn die Funktion erfolgreich ist, andernfalls ein Win32-oder RPC-Fehlercode. In der folgenden Liste sind andere mögliche Fehlercodes aufgeführt.

<dl> <dt>

**Fehler \_ Zugriff \_ verweigert**
</dt> <dd>

Der Aufrufer verfügt nicht über die erforderlichen Zugriffsberechtigungen, um diese Funktion aufzurufen. Die [**dssetauthidentity**](dssetauthidentity.md) -Funktion kann verwendet werden, um die Anmelde Informationen festzulegen, die für die Sicherungs-und Wiederherstellungs Funktionen verwendet werden sollen.

</dd> <dt>

**Fehler bei \_ ungültigem \_ Parameter**
</dt> <dd>

*HBC*, *pszattachmentinfo* oder *pcbSize* sind ungültig.

</dd> <dt>

**Fehler \_ nicht \_ genügend Arbeits \_ Speicher**
</dt> <dd>

Es ist ein Fehler bei der Speicher Belegung aufgetreten.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **dsbackupgetdatabasenames** -Funktion stellt eine Liste der für eine Sicherung erforderlichen Datenbankdateien bereit. Eine vollständige Sicherung besteht aus den Datenbankdateien und den Protokolldateien, die von der [**dsbackupgetbackuplogs**](dsbackupgetbackuplogs.md) -Funktion bereitgestellt werden. Inkrementelle Sicherungen von Active Directory Servern werden nicht unterstützt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                              |
| Header<br/>                   | <dl> <dt>Ntdsbcli. h</dt> </dl>       |
| Bibliothek<br/>                  | <dl> <dt>Ntdsbcli. lib</dt> </dl>     |
| DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl>     |
| Unicode- und ANSI-Name<br/>   | **Dsbackupgetdatabasenamesw** (Unicode) und **dsbackupgetdatabasenamesa** (ANSI)<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Dsbackupprepare**](dsbackupprepare.md)
</dt> <dt>

[**Dsbackupfree**](dsbackupfree.md)
</dt> <dt>

[**Dsbackupgetbackuplogs**](dsbackupgetbackuplogs.md)
</dt> <dt>

[**Bft-Konstanten**](bft-constants.md)
</dt> <dt>

[Sichern eines Active Directory Servers](backing-up-an-active-directory-server.md)
</dt> <dt>

[Verzeichnis Sicherungsfunktionen](directory-backup-functions.md)
</dt> </dl>

 

