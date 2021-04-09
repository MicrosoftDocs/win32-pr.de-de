---
title: Dsrestoregetdatabaselocations-Funktion (ntdsbcli. h)
description: Ruft die Speicherorte ab, an denen Sicherungsdateien bei einem Wiederherstellungs Vorgang kopiert werden sollen.
ms.assetid: f91d701c-72cf-418a-8d1c-6bf6ef41c2c1
ms.tgt_platform: multiple
keywords:
- Dsrestoregetdatabaselocations-Funktion Active Directory
topic_type:
- apiref
api_name:
- DsRestoreGetDatabaseLocations
- DsRestoreGetDatabaseLocationsA
- DsRestoreGetDatabaseLocationsW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bcebb9f3822332269e1db09f3246c128e4ad1f2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859060"
---
# <a name="dsrestoregetdatabaselocations-function"></a>Dsrestoregetdatabaselocations-Funktion

\[Diese Funktion ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Verwenden Sie ab Windows Vista [Volumeschattenkopie-Dienst (VSS)](../vss/volume-shadow-copy-service-overview.md) .\]

Die **dsrestoregetdatabaselocations** -Funktion Ruft die Speicherorte ab, an denen Sicherungsdateien bei einem Wiederherstellungs Vorgang kopiert werden sollen.

## <a name="syntax"></a>Syntax


```C++
HRESULT DsRestoreGetDatabaseLocations(
  _In_  HBC     hbc,
  _Out_ LPWSTR  *pszDatabaseLocationList,
  _Out_ LPDWORD pcbSize
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*HBC* \[ in\]
</dt> <dd>

Enthält das Wiederherstellungs Kontext Handle, das mit der [**dsrestoreprepare**](dsrestoreprepare.md) -Funktion abgerufen wurde.

</dd> <dt>

*pszdatabaselocationlist* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen Zeichen folgen Zeiger, der die Liste der Daten Bank Speicherorte als UNC-Pfade empfängt. Diese Liste empfängt eine mit NULL endend beendete Liste mit einzelnen null-terminierten Zeichen folgen.

Dieser Puffer wird durch die Funktion **dsrestoregetdatabaselocations** zugewiesen und muss freigegeben werden, wenn er durch Aufrufen der [**dsbackupfree**](dsbackupfree.md) -Funktion nicht mehr benötigt wird.

Das erste Zeichen jedes Datei namens enthält eine der [**bft-Konstanten**](bft-constants.md) , die den Namenstyp identifiziert. Die **dsrestoregetdatabaselocations** -Funktion stellt nur die folgenden namens Typen bereit.

<dt>

<span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>

<span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>**bft- \_ NTDS- \_ Datenbank**


</dt> <dd>

Die NTDS-Datenbankdatei sollte in diese Datei kopiert werden. Dies ist die Datei, die beim Durchführen der Sicherung als **bft \_ NTDS- \_ Datenbank** identifiziert wurde.

</dd> <dt>

<span id="BFT_LOG_DIR"></span><span id="bft_log_dir"></span>

<span id="BFT_LOG_DIR"></span><span id="bft_log_dir"></span>**bft- \_ Protokoll Verzeichnis \_**


</dt> <dd>

Alle Protokolldateien werden in dieses Verzeichnis kopiert. Die Protokolldateien wurden als **bft- \_ Protokoll** identifiziert, als die Sicherung durchgeführt wurde.

</dd> <dt>

<span id="BFT_CHECKPOINT_DIR"></span><span id="bft_checkpoint_dir"></span>

<span id="BFT_CHECKPOINT_DIR"></span><span id="bft_checkpoint_dir"></span>**bft-Prüf Punkt Verzeichnis \_ \_**


</dt> <dd>

Alle Patchdateien werden in dieses Verzeichnis kopiert. Die Patchdateien wurden als **bft- \_ \_ Patchdatei** identifiziert, als die Sicherung durchgeführt wurde.

</dd> </dl> </dd> <dt>

*pcbSize* \[ vorgenommen\]
</dt> <dd>

Zeiger auf den **DWORD** -Wert, der die Größe des *pszdatabaselocationlist* -Puffers in Bytes empfängt.

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

*HBC*, *pszdatabaselocationlist* oder *pcbSize* sind ungültig.

</dd> <dt>

**Fehler \_ nicht \_ genügend Arbeits \_ Speicher**
</dt> <dd>

Es ist ein Fehler bei der Speicher Belegung aufgetreten.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **dsrestoregetdatabaselocations** -Funktion kann verwendet werden, um die Wiederherstellungs Verzeichnisse zu erhalten, ohne auf die gesicherten Daten zuzugreifen. Aufrufen Sie hierzu [**dsrestoreprepare**](dsrestoreprepare.md) mit **null** für den *pvexpiriytoken* -Parameter. Dies bewirkt, dass **dsrestoreprepare** ein eingeschränktes Kontext Handle zurückgibt, das nur mit der **dsrestoregetdatabaselocations** -Funktion verwendet werden kann.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                                        |
| Header<br/>                   | <dl> <dt>Ntdsbcli. h</dt> </dl>                 |
| Bibliothek<br/>                  | <dl> <dt>Ntdsbcli. lib</dt> </dl>               |
| DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl>               |
| Unicode- und ANSI-Name<br/>   | **Dsrestoregetdatabaselocationsw** (Unicode) und **dsrestoregetdatabaselocationsa** (ANSI)<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Dsrestoreprepare**](dsrestoreprepare.md)
</dt> <dt>

[**Dsbackupfree**](dsbackupfree.md)
</dt> <dt>

[Verzeichnis Sicherungsfunktionen](directory-backup-functions.md)
</dt> <dt>

[Wiederherstellen von Active Directory](restoring-an-active-directory-server.md)
</dt> </dl>

 

