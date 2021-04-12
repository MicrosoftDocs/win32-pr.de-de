---
title: Dsbackupopenfile-Funktion (ntdsbcli. h)
description: Öffnet die angegebene Datei und führt die Client-und Server Vorgänge aus, die erforderlich sind, um die Datei für die Sicherung vorzubereiten.
ms.assetid: 1ffb81ee-9e7e-4d88-91fc-f1857377d125
ms.tgt_platform: multiple
keywords:
- Dsbackupopenfile-Funktion Active Directory
topic_type:
- apiref
api_name:
- DsBackupOpenFile
- DsBackupOpenFileA
- DsBackupOpenFileW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2f9c4eac9c9825f510848583d7f707a2c244c52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104055"
---
# <a name="dsbackupopenfile-function"></a>Dsbackupopenfile-Funktion

\[Diese Funktion ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Verwenden Sie ab Windows Vista [Volumeschattenkopie-Dienst (VSS)](../vss/volume-shadow-copy-service-overview.md) .\]

Die **dsbackupopenfile** -Funktion öffnet die angegebene Datei und führt die Client-und Server Vorgänge aus, die erforderlich sind, um die Datei für die Sicherung vorzubereiten.

## <a name="syntax"></a>Syntax


```C++
HRESULT DsBackupOpenFile(
  _In_  HBC           hbc,
  _In_  LPCTSTR       szAttachmentName,
  _In_  DWORD         cbReadHintSize,
  _Out_ LARGE_INTEGER *pliFileSize
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*HBC* \[ in\]
</dt> <dd>

Enthält das Sicherungs Kontext Handle, das mit der [**dsbackupprepare**](dsbackupprepare.md) -Funktion abgerufen wurde.

</dd> <dt>

*szattachmentname* \[ in\]
</dt> <dd>

Zeiger auf eine mit NULL endenden Zeichenfolge, die den Namen der Sicherungsdatei angibt, die geöffnet werden soll.

</dd> <dt>

*cbreadhintsize* \[ in\]
</dt> <dd>

Enthält die mögliche Größe (in Bytes) des Puffers, der als *pvbuffer* -Argument in der [**dsbackupread**](dsbackupread.md) -Funktion übergeben wird. Die Sicherungsfunktionen verwenden diesen Wert als Hinweis, um den Netzwerk Datenverkehr zu optimieren. Dieser Wert muss ein Vielfaches von 8192 sein und muss größer oder gleich 24576 sein.

</dd> <dt>

*plifilesize* \[ vorgenommen\]
</dt> <dd>

Zeiger auf einen **großen \_ ganzzahligen** Wert, der die Größe der geöffneten Sicherungsdatei in Bytes empfängt.

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

" *HBC*", " *szattachmentname*" oder " *plifilesize* " sind ungültig.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Ntdsbcli. h</dt> </dl>   |
| Bibliothek<br/>                  | <dl> <dt>Ntdsbcli. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **Dsbackupopenfilew** (Unicode) und **dsbackupopenfilea** (ANSI)<br/>             |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Dsbackupread**](dsbackupread.md)
</dt> <dt>

[Sichern eines Active Directory Servers](backing-up-an-active-directory-server.md)
</dt> <dt>

[Verzeichnis Sicherungsfunktionen](directory-backup-functions.md)
</dt> </dl>

 

