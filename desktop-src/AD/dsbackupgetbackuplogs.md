---
title: Dsbackupgetbackuplogs-Funktion (ntdsbcli. h)
description: Ruft die Liste der Protokolldateien ab, die für den angegebenen Sicherungs Kontext gesichert werden müssen.
ms.assetid: 09b3fdac-41ea-471c-a0dd-54414181f6fe
ms.tgt_platform: multiple
keywords:
- Dsbackupgetbackuplogs-Funktion Active Directory
topic_type:
- apiref
api_name:
- DsBackupGetBackupLogs
- DsBackupGetBackupLogsA
- DsBackupGetBackupLogsW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a02c5c7234810623a95dea030f0c623cca92293
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956588"
---
# <a name="dsbackupgetbackuplogs-function"></a>Dsbackupgetbackuplogs-Funktion

\[Diese Funktion ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Verwenden Sie ab Windows Vista [Volumeschattenkopie-Dienst (VSS)](../vss/volume-shadow-copy-service-overview.md) .\]

Die **dsbackupgetbackuplogs** -Funktion Ruft die Liste der Protokolldateien ab, die für den angegebenen Sicherungs Kontext gesichert werden müssen.

## <a name="syntax"></a>Syntax


```C++
HRESULT DsBackupGetBackupLogs(
  _In_  HBC     hbc,
  _Out_ LPTSTR  *pszBackupLogFiles,
  _Out_ LPDWORD pcbSize
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*HBC* \[ in\]
</dt> <dd>

Enthält das Sicherungs Kontext Handle, das mit der [**dsbackupprepare**](dsbackupprepare.md) -Funktion abgerufen wurde.

</dd> <dt>

*pszbackuplogfiles* \[ vorgenommen\]
</dt> <dd>

Zeiger auf einen Zeichen folgen Zeiger, der die Liste der Protokoll Dateinamen als UNC-Pfade empfängt. Initialisieren Sie diesen Wert vor dem Aufrufen von **dsbackupgetbackuplogs** in **null** .

Diese Liste empfängt eine mit NULL endend beendete Liste mit einzelnen null-terminierten Zeichen folgen.

Dieser Puffer wird von der **dsbackupgetbackuplogs** -Funktion zugewiesen und muss freigegeben werden, wenn er durch Aufrufen der [**dsbackupfree**](dsbackupfree.md) -Funktion nicht mehr benötigt wird.

Das erste Zeichen jedes Datei namens enthält eine der [**bft-Konstanten**](bft-constants.md) , die den Typ des Namens identifiziert.

</dd> <dt>

*pcbSize* \[ vorgenommen\]
</dt> <dd>

Zeiger auf den **DWORD** -Wert, der die Größe des *pszbackuplogfiles* -Puffers in Bytes empfängt.

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

*HBC*, *pszbackuplogfiles* oder *pcbSize* ist ungültig.

</dd> <dt>

**Fehler \_ nicht \_ genügend Arbeits \_ Speicher**
</dt> <dd>

Es ist ein Fehler bei der Speicher Belegung aufgetreten.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die Funktion **dsbackupgetbackuplogs** enthält eine Liste der Protokolldateien, die für eine Sicherung erforderlich sind. Eine vollständige Sicherung besteht aus den Datenbankdateien, die von der Funktion [**dsbackupgetdatabasenames**](dsbackupgetdatabasenames.md) und den Protokolldateien bereitgestellt werden. Inkrementelle Sicherungen von Active Directory Servern werden nicht unterstützt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Ntdsbcli. h</dt> </dl>   |
| Bibliothek<br/>                  | <dl> <dt>Ntdsbcli. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **Dsbackupgetbackuplogsw** (Unicode) und **dsbackupgetbackuplogsa** (ANSI)<br/>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Dsbackupfree**](dsbackupfree.md)
</dt> <dt>

[**Dsbackupgetdatabasenames**](dsbackupgetdatabasenames.md)
</dt> <dt>

[**Bft-Konstanten**](bft-constants.md)
</dt> <dt>

[Sichern eines Active Directory Servers](backing-up-an-active-directory-server.md)
</dt> <dt>

[Verzeichnis Sicherungsfunktionen](directory-backup-functions.md)
</dt> </dl>

 

