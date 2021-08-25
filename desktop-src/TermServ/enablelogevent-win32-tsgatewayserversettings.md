---
title: EnableLogEvent-Methode der Win32_TSGatewayServerSettings-Klasse
description: Aktiviert oder deaktiviert die Protokollierung des angegebenen Ereignistyps.
ms.assetid: e901ef51-2ae2-4123-902a-ac359f3eb959
ms.tgt_platform: multiple
keywords:
- EnableLogEvent-Methode Remotedesktopdienste
- EnableLogEvent-Methode Remotedesktopdienste , Win32_TSGatewayServerSettings-Klasse
- Win32_TSGatewayServerSettings Klasse Remotedesktopdienste , EnableLogEvent-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.EnableLogEvent
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd70902649f6fadc66308ad35ce165a6d2fdb4654b73e056c3bc38f1850b3e07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119871720"
---
# <a name="enablelogevent-method-of-the-win32_tsgatewayserversettings-class"></a>EnableLogEvent-Methode der Win32 \_ TSGatewayServerSettings-Klasse

Aktiviert oder deaktiviert die Protokollierung des angegebenen Ereignistyps.

## <a name="syntax"></a>Syntax


```mof
uint32 EnableLogEvent(
  [in] string  EventName,
  [in] boolean Enabled
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*EventName* \[ In\]
</dt> <dd>

Name der Veranstaltung. Dieser Wert sollte mithilfe der [**GetLogEventName-Methode**](getlogeventname-win32-tsgatewayserversettings.md) abgerufen werden.

<dt>

LogChannelDisconnect
</dt> <dd>

Der Benutzer hat die Verbindung mit der Ressource erfolgreich getrennt.

</dd> <dt>

LogFailedChannelConnect
</dt> <dd>

Der Benutzer konnte keine Verbindung mit der Ressource herstellen.

</dd> <dt>

LogFailureNetworkAccessCheck
</dt> <dd>

Fehler bei der Verbindungsautorisierung des Benutzers.

</dd> <dt>

LogFailureResourceAccessCheck
</dt> <dd>

Fehler bei der Ressourcenautorisierung durch den Benutzer.

</dd> <dt>

LogSuccessChannelConnect
</dt> <dd>

Der Benutzer hat erfolgreich eine Verbindung mit der Ressource hergestellt.

</dd> <dt>

LogSuccessfulNetworkAccessCheck
</dt> <dd>

Der Benutzer hat die Verbindungsautorisierung erfolgreich bestanden.

</dd> <dt>

LogSuccessfulResourceAccessCheck
</dt> <dd>

Der Benutzer hat die Ressourcenautorisierung erfolgreich bestanden.

</dd> </dl> </dd> <dt>

*Aktiviert* \[ In\]
</dt> <dd>

Gibt an, ob das Ereignis aktiviert oder deaktiviert werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, gibt sie 0 (null) zurück. Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben. Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste WMI-Anbieterfehlercodes.](terminal-services-wmi-provider-error-codes.md)

## <a name="remarks"></a>Hinweise

Sie müssen Mitglied der Gruppe Administratoren sein, um diese Methode aufzurufen.

Managed Object Format -Dateien (MOF) enthalten die Definitionen für Windows Management Instrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                           |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ TSGatewayServerSettings**](win32-tsgatewayserversettings.md)
</dt> <dt>

[**GetLogEventName**](getlogeventname-win32-tsgatewayserversettings.md)
</dt> </dl>

 

