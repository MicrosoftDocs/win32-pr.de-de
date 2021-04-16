---
title: Dsbackuptruneurelogs-Funktion (ntdsbcli. h)
description: Verkürzt die zuvor gelesenen Sicherungs Protokolle.
ms.assetid: fae2e19f-08b8-410f-a735-dd4d41fc71a6
ms.tgt_platform: multiple
keywords:
- Dsbackuptruneurelogs-Funktion Active Directory
topic_type:
- apiref
api_name:
- DsBackupTruncateLogs
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 051ced828656c6b6e5af156e2d1a69c3b741cdce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517666"
---
# <a name="dsbackuptruncatelogs-function"></a>Dsbackuptruneurelogs-Funktion

\[Diese Funktion ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Verwenden Sie ab Windows Vista [Volumeschattenkopie-Dienst (VSS)](../vss/volume-shadow-copy-service-overview.md) .\]

Die **dsbackuptruneurelogs** -Funktion verkürzt die zuvor gelesenen Sicherungs Protokolle.

## <a name="syntax"></a>Syntax


```C++
HRESULT DsBackupTruncateLogs(
  _In_ HBC hbc
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*HBC* \[ in\]
</dt> <dd>

Enthält das Sicherungs Kontext Handle, das mit der [**dsbackupprepare**](dsbackupprepare.md) -Funktion abgerufen wurde.

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

*HBC* ist ungültig.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Verwenden Sie die Funktion **dsbackuptruneurelogs** , wenn eine vollständige oder inkrementelle Sicherung erfolgreich abgeschlossen wurde.

> [!Caution]  
> Wenn diese Funktion nach einer differenziellen Sicherung aufgerufen wird, gehen alle Informationen zur inkrementellen Sicherung verloren.

 

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

[**Dsbackupprepare**](dsbackupprepare.md)
</dt> <dt>

[**Dsbackupgetbackuplogs**](dsbackupgetbackuplogs.md)
</dt> <dt>

[**Dssetcurrentbackuplog**](dssetcurrentbackuplog.md)
</dt> <dt>

[Sichern eines Active Directory Servers](backing-up-an-active-directory-server.md)
</dt> <dt>

[Verzeichnis Sicherungsfunktionen](directory-backup-functions.md)
</dt> </dl>

 

