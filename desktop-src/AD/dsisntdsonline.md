---
title: DsIsNTDSOnline-Funktion (Ntdsbcli.h)
description: Bestimmt, ob Active Directory Domain Services auf dem angegebenen Server online sind.
ms.assetid: 8f46e4d8-6d05-402c-a5b4-291fd2d6609b
ms.tgt_platform: multiple
keywords:
- DsIsNTDSOnline-Funktion Active Directory
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
ms.openlocfilehash: 0bf65109b4c72e1d403ece18d82b189039d74d58043271e0f5bf317f5272f84d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118430022"
---
# <a name="dsisntdsonline-function"></a>DsIsNTDSOnline-Funktion

\[Diese Funktion ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Verwenden Sie ab Windows Vista stattdessen [Volumeschattenkopie-Dienst (VSS).](../vss/volume-shadow-copy-service-overview.md)\]

Die **DsIsNTDSOnline-Funktion** bestimmt, ob Active Directory Domain Services auf dem angegebenen Server online sind.

## <a name="syntax"></a>Syntax


```C++
HRESULT DsIsNTDSOnline(
  _In_  LPCTSTR szServerName,
  _Out_ BOOL    *pfNTDSOnline
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*szServerName* \[ In\]
</dt> <dd>

Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des zu testden Servers enthält. Die vorangehenden umgekehrten Schrägstriche sind optional. Der Server muss derselbe Computer sein, von dem diese Funktion aufgerufen wird. Der Servername darf keinen Unterstrich \_ () enthalten. Ein Beispiel für einen Servernamen ist \\ \\ "server1".

</dd> <dt>

*pfNTDSOnline* \[ out\]
</dt> <dd>

Zeiger auf den **BOOL-Wert,** der das Ergebnis empfängt. Empfängt **TRUE,** wenn der Verzeichnisdienst online ist, oder **FALSE,** wenn der Verzeichnisdienst offline ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **S \_ OK** zurück, wenn die Funktion erfolgreich ist, oder andernfalls ein Fehlercode. In der folgenden Liste sind mögliche Fehlercodes aufgeführt.

<dl> <dt>

**FEHLERZUGRIFF \_ \_ VERWEIGERT**
</dt> <dd>

Der Aufrufer verfügt nicht über die richtigen Zugriffsberechtigungen zum Aufrufen dieser Funktion. Die [**DsSetAuthIdentity-Funktion**](dssetauthidentity.md) kann verwendet werden, um die Anmeldeinformationen festzulegen, die für die Sicherungs- und Wiederherstellungsfunktionen verwendet werden sollen.

</dd> <dt>

**hrConnectNotConnect**
</dt> <dd>

Der Server in *szServerName* wurde nicht gefunden, ist kein Domänencontroller, oder *szServerName* ist nicht ordnungsgemäß formatiert. Dieser Wert ist in Ntdsbmsg.h definiert.

</dd> <dt>

**\_RPC S \_ UNGÜLTIGE \_ BINDUNG**
</dt> <dd>

Die [**DsIsNTDSOnline-Funktion**](dsisntdsonline.md) wird remote aufgerufen, oder der Server in *szServerName* ist kein Domänencontroller.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Rufen Sie diese Funktion auf, bevor Sie eine der Verzeichnissicherungs- oder -wiederherstellungsfunktionen aufrufen. Das Verzeichnis muss online sein, um eine Sicherung durchführen zu können. Das Verzeichnis muss offline sein, um eine Wiederherstellung durchzuführen.

Diese Funktion kann nur von einem Domänencontroller aufgerufen werden, der auch der in *szServerName* angegebene Zielserver ist. Diese Funktion kann nicht remote aufgerufen werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Ntdsbcli.h</dt> </dl>   |
| Bibliothek<br/>                  | <dl> <dt>Ntdsbcli.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **DsIsNTDSOnlineW** (Unicode) und **DsIsNTDSOnlineA** (ANSI)<br/>                 |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**DsSetAuthIdentity**](dssetauthidentity.md)
</dt> <dt>

[Verzeichnissicherungsfunktionen](directory-backup-functions.md)
</dt> <dt>

[Sichern und Wiederherstellen eines Active Directory-Servers](backing-up-and-restoring-an-active-directory-server.md)
</dt> </dl>

 

