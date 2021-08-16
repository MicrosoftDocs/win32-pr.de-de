---
title: DsBackupGetDatabaseNames-Funktion (Ntdsbcli.h)
description: Ruft die Liste der Datenbankdateien ab, die für den angegebenen Sicherungskontext gesichert werden sollen.
ms.assetid: ba0447a1-38b0-4c0a-8c63-abaefb5b908f
ms.tgt_platform: multiple
keywords:
- DsBackupGetDatabaseNames-Funktion Active Directory
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
ms.openlocfilehash: 620ad77f84aa2cb52a7bd99a96a22e7de560b53b2c3ba2022598609dde3737fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118191856"
---
# <a name="dsbackupgetdatabasenames-function"></a>DsBackupGetDatabaseNames-Funktion

\[Diese Funktion ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Verwenden Sie ab Windows Vista stattdessen [Volumeschattenkopie-Dienst (VSS).](../vss/volume-shadow-copy-service-overview.md)\]

Die **DsBackupGetDatabaseNames-Funktion** ruft die Liste der Datenbankdateien ab, die für den angegebenen Sicherungskontext gesichert werden sollen.

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

*hbc* \[ In\]
</dt> <dd>

Enthält das Sicherungskontexthandle, das mit der [**DsBackupPrepare-Funktion**](dsbackupprepare.md) abgerufen wurde.

</dd> <dt>

*pszAttachmentInfo* \[ out\]
</dt> <dd>

Zeiger auf einen Zeichenfolgenzeiger, der die Liste der Datenbankdateinamen als UNC-Pfade empfängt. Dieser Wert muss vor dem Aufrufen von **DsBackupGetDatabaseNames** mit **NULL** initialisiert werden.

Diese Liste empfängt eine doppelt auf NULL endende Liste einzelner null-terminierte Zeichenfolgen.

Dieser Puffer wird von der **DsBackupGetDatabaseNames-Funktion** zugeordnet und muss freigegeben werden, wenn er nicht mehr benötigt wird, indem die [**DsBackupFree-Funktion**](dsbackupfree.md) aufgerufen wird.

Das erste Zeichen jedes Dateinamens enthält eine der [**BFT-Konstanten,**](bft-constants.md) die den Typ des Namens identifiziert. Die [**DsRestoreGetDatabaseLocations-Funktion**](dsrestoregetdatabaselocations.md) stellt nur die folgenden Namentypen bereit.

<dt>

<span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>

<span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>**BFT \_ NTDS \_ DATABASE**


</dt> <dd>

Die Datei ist eine NTDS-Datenbankdatei. Diese Datei sollte in die Datei kopiert werden, die beim Wiederherstellen der Daten als **BFT \_ NTDS \_ DATABASE** identifiziert wird.

</dd> <dt>

<span id="BFT_LOG"></span><span id="bft_log"></span>

<span id="BFT_LOG"></span><span id="bft_log"></span>**BFT \_ LOG**


</dt> <dd>

Die Datei ist eine Protokolldatei. Alle Protokolldateien werden in das Verzeichnis kopiert, das beim Wiederherstellen der Daten als **BFT \_ LOG \_ DIR** identifiziert wird.

</dd> <dt>

<span id="BFT_PATCH_FILE"></span><span id="bft_patch_file"></span>

<span id="BFT_PATCH_FILE"></span><span id="bft_patch_file"></span>**\_BFT-PATCHDATEI \_**


</dt> <dd>

Die Datei ist eine Patchdatei. Alle Patchdateien werden in das Verzeichnis kopiert, das beim Wiederherstellen der Daten als **BFT \_ CHECKPOINT \_ DIR** identifiziert wird.

</dd> </dl> </dd> <dt>

*layoutSize* \[ out\]
</dt> <dd>

Zeiger auf den **DWORD-Wert,** der die Größe des *pszAttachmentInfo-Puffers* in Bytes empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **S \_ OK** zurück, wenn die Funktion erfolgreich ist oder andernfalls ein Win32- oder RPC-Fehlercode vorliegt. In der folgenden Liste sind weitere mögliche Fehlercodes aufgeführt.

<dl> <dt>

**FEHLERZUGRIFF \_ \_ VERWEIGERT**
</dt> <dd>

Der Aufrufer verfügt nicht über die richtigen Zugriffsberechtigungen zum Aufrufen dieser Funktion. Die [**DsSetAuthIdentity-Funktion**](dssetauthidentity.md) kann verwendet werden, um die Anmeldeinformationen festzulegen, die für die Sicherungs- und Wiederherstellungsfunktionen verwendet werden sollen.

</dd> <dt>

**FEHLER: \_ UNGÜLTIGER \_ PARAMETER**
</dt> <dd>

*hbc,* *pszAttachmentInfo* oder *designsSize* sind ungültig.

</dd> <dt>

**FEHLER \_ NICHT \_ GENÜGEND \_ ARBEITSSPEICHER**
</dt> <dd>

Fehler bei der Speicherbelegung.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **DsBackupGetDatabaseNames-Funktion** stellt eine Liste der Datenbankdateien bereit, die für eine Sicherung erforderlich sind. Eine vollständige Sicherung besteht aus den Datenbankdateien und den Protokolldateien, die von der [**DsBackupGetBackupLogs-Funktion**](dsbackupgetbackuplogs.md) bereitgestellt werden. Inkrementelle Sicherungen von Active Directory-Servern werden nicht unterstützt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                              |
| Header<br/>                   | <dl> <dt>Ntdsbcli.h</dt> </dl>       |
| Bibliothek<br/>                  | <dl> <dt>Ntdsbcli.lib</dt> </dl>     |
| DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl>     |
| Unicode- und ANSI-Name<br/>   | **DsBackupGetDatabaseNamesW** (Unicode) und **DsBackupGetDatabaseNamesA** (ANSI)<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**DsBackupPrepare**](dsbackupprepare.md)
</dt> <dt>

[**DsBackupFree**](dsbackupfree.md)
</dt> <dt>

[**DsBackupGetBackupLogs**](dsbackupgetbackuplogs.md)
</dt> <dt>

[**BFT-Konstanten**](bft-constants.md)
</dt> <dt>

[Sichern eines Active Directory-Servers](backing-up-an-active-directory-server.md)
</dt> <dt>

[Verzeichnissicherungsfunktionen](directory-backup-functions.md)
</dt> </dl>

 

