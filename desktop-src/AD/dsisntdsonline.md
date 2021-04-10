---
title: Dsisntdsonline-Funktion (ntdsbcli. h)
description: Bestimmt, ob Active Directory Domain Services auf dem angegebenen Server online sind.
ms.assetid: 8f46e4d8-6d05-402c-a5b4-291fd2d6609b
ms.tgt_platform: multiple
keywords:
- Dsisntdsonline-Funktion Active Directory
topic_type:
- apiref
api_name:
- DsIsNTDSOnline
- DsIsNTDSOnlineA
- DsIsNTDSOnlineW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57f6728f4481eb8820055b48f10cfa0f94c7aaa1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103797"
---
# <a name="dsisntdsonline-function"></a>Dsisntdsonline-Funktion

\[Diese Funktion ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Verwenden Sie ab Windows Vista [Volumeschattenkopie-Dienst (VSS)](../vss/volume-shadow-copy-service-overview.md) .\]

Die **dsisntdsonline** -Funktion bestimmt, ob Active Directory Domain Services auf dem angegebenen Server online sind.

## <a name="syntax"></a>Syntax


```C++
HRESULT DsIsNTDSOnline(
  _In_  LPCTSTR szServerName,
  _Out_ BOOL    *pfNTDSOnline
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*szservername* \[ in\]
</dt> <dd>

Zeiger auf eine mit NULL endenden Zeichenfolge, die den Namen des zu testenden Servers enthält. Vorangehende umgekehrte Schrägstriche sind optional. Der Server muss derselbe Computer sein, von dem diese Funktion aufgerufen wird. Der Servername darf keine Unterstriche ( \_ ) enthalten. Ein Beispiel für einen Servernamen ist " \\ \\ Server1".

</dd> <dt>

*pfntdsonline* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen **booleschen** Wert, der das Ergebnis empfängt. Empfängt **true** , wenn der Verzeichnisdienst Online ist, oder **false** , wenn der Verzeichnisdienst offline ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **S \_ OK** zurück, wenn die Funktion erfolgreich ist, andernfalls einen Fehlercode. In der folgenden Liste sind die möglichen Fehlercodes aufgeführt.

<dl> <dt>

**Fehler \_ Zugriff \_ verweigert**
</dt> <dd>

Der Aufrufer verfügt nicht über die erforderlichen Zugriffsberechtigungen, um diese Funktion aufzurufen. Die [**dssetauthidentity**](dssetauthidentity.md) -Funktion kann verwendet werden, um die Anmelde Informationen festzulegen, die für die Sicherungs-und Wiederherstellungs Funktionen verwendet werden sollen.

</dd> <dt>

**hrcouldnotconnect**
</dt> <dd>

Der Server in " *szservername* " kann nicht gefunden werden, ist kein Domänen Controller, oder " *szservername* " ist nicht ordnungsgemäß formatiert. Dieser Wert wird in "ntdsbmsg. h" definiert.

</dd> <dt>

**\_ungültige RPC S- \_ \_ Bindung**
</dt> <dd>

Die [**dsisntdsonline**](dsisntdsonline.md) -Funktion wird Remote aufgerufen, oder der Server in " *szservername* " ist kein Domänen Controller.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Rufen Sie diese Funktion auf, bevor Sie eine der Verzeichnis Sicherungs-oder Wiederherstellungs Funktionen aufrufen. Das Verzeichnis muss online sein, um eine Sicherung ausführen zu können. Das Verzeichnis muss offline sein, um eine Wiederherstellung auszuführen.

Diese Funktion kann nur von einem Domänen Controller aufgerufen werden, der auch der in " *szservername*" angegebene Zielserver ist. Diese Funktion kann nicht remote aufgerufen werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Ntdsbcli. h</dt> </dl>   |
| Bibliothek<br/>                  | <dl> <dt>Ntdsbcli. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **Dsisntdsonlinew** (Unicode) und **dsisntdsonlinea** (ANSI)<br/>                 |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Dssetauthidentity**](dssetauthidentity.md)
</dt> <dt>

[Verzeichnis Sicherungsfunktionen](directory-backup-functions.md)
</dt> <dt>

[Sichern und Wiederherstellen eines Active Directory Servers](backing-up-and-restoring-an-active-directory-server.md)
</dt> </dl>

 

