---
title: DsRestoreGetDatabaseLocations-Funktion (Ntdsbcli.h)
description: Erhält die Speicherorte, an denen Sicherungsdateien während eines Wiederherstellungsvorgang kopiert werden sollen.
ms.assetid: f91d701c-72cf-418a-8d1c-6bf6ef41c2c1
ms.tgt_platform: multiple
keywords:
- DsRestoreGetDatabaseLocations-Funktion Active Directory
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
ms.openlocfilehash: f3c5626e2e0dc679a4669bb5d8be8096b6ae0629aeed7c833f397b5f9bca45db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118429992"
---
# <a name="dsrestoregetdatabaselocations-function"></a>DsRestoreGetDatabaseLocations-Funktion

\[Diese Funktion ist für die Verwendung in den Im Abschnitt Anforderungen angegebenen Betriebssystemen verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Ab Windows Vista verwenden Sie stattdessen [Volumeschattenkopie-Dienst (VSS).](../vss/volume-shadow-copy-service-overview.md)\]

Die **Funktion DsRestoreGetDatabaseLocations** erhält die Speicherorte, an denen Sicherungsdateien während eines Wiederherstellungsvorgang kopiert werden sollen.

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

*hbc* \[ In\]
</dt> <dd>

Enthält das Wiederherstellungskontexthand handle, das mit der [**DsRestorePrepare-Funktion ermittelt**](dsrestoreprepare.md) wurde.

</dd> <dt>

*pszDatabaseLocationList* \[ out\]
</dt> <dd>

Zeiger auf einen Zeichenfolgenzeiger, der die Liste der Datenbankstandorte als UNC-Pfade empfängt. Diese Liste empfängt eine doppelte Null-Terminierungsliste mit einzelnen Zeichenfolgen, die mit NULL beendet werden.

Dieser Puffer wird von der **DsRestoreGetDatabaseLocations-Funktion** zugeordnet und muss durch Aufrufen der [**DsBackupFree-Funktion**](dsbackupfree.md) wieder frei werden, wenn er nicht mehr benötigt wird.

Das erste Zeichen jedes Dateinamens enthält eine der [**BFT-Konstanten,**](bft-constants.md) die den Namenstyp identifiziert. Die **DsRestoreGetDatabaseLocations-Funktion** stellt nur die folgenden Namenstypen zur Verfügung.

<dt>

<span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>

<span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>**BFT \_ \_ NTDS-DATENBANK**


</dt> <dd>

Die NTDS-Datenbankdatei sollte in diese Datei kopiert werden. Dies ist die Datei, die beim Durchführen der Sicherung **als BFT \_ NTDS \_ DATABASE** identifiziert wurde.

</dd> <dt>

<span id="BFT_LOG_DIR"></span><span id="bft_log_dir"></span>

<span id="BFT_LOG_DIR"></span><span id="bft_log_dir"></span>**BFT \_ LOG \_ DIR**


</dt> <dd>

Alle Protokolldateien werden in dieses Verzeichnis kopiert. Die Protokolldateien wurden als **BFT \_ LOG identifiziert,** als die Sicherung durchgeführt wurde.

</dd> <dt>

<span id="BFT_CHECKPOINT_DIR"></span><span id="bft_checkpoint_dir"></span>

<span id="BFT_CHECKPOINT_DIR"></span><span id="bft_checkpoint_dir"></span>**BFT \_ CHECKPOINT \_ DIR**


</dt> <dd>

Alle Patchdateien werden in dieses Verzeichnis kopiert. Die Patchdateien wurden als **BFT \_ PATCH FILE \_ identifiziert,** als die Sicherung durchgeführt wurde.

</dd> </dl> </dd> <dt>

*besize* \[ out\]
</dt> <dd>

Zeiger auf **den DWORD-Wert,** der die Größe des *Puffers pszDatabaseLocationList* in Bytes empfängt.

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

*hbc,* *pszDatabaseLocationList* *oderize sind* ungültig.

</dd> <dt>

**FEHLER: \_ NICHT \_ GENÜGEND \_ ARBEITSSPEICHER**
</dt> <dd>

Es ist ein Speicherbelegungsfehler aufgetreten.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **Funktion DsRestoreGetDatabaseLocations** kann verwendet werden, um die Wiederherstellungsverzeichnisse ohne Zugriff auf die sichern Daten zu erhalten. Rufen Sie hierzu [**DsRestorePrepare**](dsrestoreprepare.md) mit **NULL für** den parameter *pvExpiryToken* auf. Dadurch gibt **DsRestorePrepare** ein eingeschränktes Kontexthand handle zurück, das nur mit der **DsRestoreGetDatabaseLocations-Funktion verwendet werden** kann.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                                        |
| Header<br/>                   | <dl> <dt>Ntdsbcli.h</dt> </dl>                 |
| Bibliothek<br/>                  | <dl> <dt>Ntdsbcli.lib</dt> </dl>               |
| DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl>               |
| Unicode- und ANSI-Name<br/>   | **DsRestoreGetDatabaseLocationsW** (Unicode) und **DsRestoreGetDatabaseLocationsA** (ANSI)<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**DsRestorePrepare**](dsrestoreprepare.md)
</dt> <dt>

[**DsBackupFree**](dsbackupfree.md)
</dt> <dt>

[Verzeichnissicherungsfunktionen](directory-backup-functions.md)
</dt> <dt>

[Wiederherstellen von Active Directory](restoring-an-active-directory-server.md)
</dt> </dl>

 

