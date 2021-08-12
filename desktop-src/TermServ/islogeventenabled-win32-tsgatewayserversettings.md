---
title: IsLogEventEnabled-Methode der Win32_TSGatewayServerSettings-Klasse
description: Gibt an, ob der angegebene Ereignisprotokolltyp aktiviert ist.
ms.assetid: 4abfc56f-871a-44ef-9998-da88949a0a2d
ms.tgt_platform: multiple
keywords:
- IsLogEventEnabled-Methode Remotedesktopdienste
- IsLogEventEnabled-Methode Remotedesktopdienste , Win32_TSGatewayServerSettings-Klasse
- Win32_TSGatewayServerSettings-Klasse Remotedesktopdienste , IsLogEventEnabled-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.IsLogEventEnabled
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7130578287e313e03caf8b63c2e187f401608ad1cdbd575ae9e6bb6450e1adf9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118606059"
---
# <a name="islogeventenabled-method-of-the-win32_tsgatewayserversettings-class"></a>IsLogEventEnabled-Methode der Win32 \_ TSGatewayServerSettings-Klasse

Gibt an, ob der angegebene Ereignisprotokolltyp aktiviert ist.

## <a name="syntax"></a>Syntax


```mof
uint32 IsLogEventEnabled(
  [in]  string  EventName,
  [out] boolean Enabled
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*EventName* \[ In\]
</dt> <dd>

Name des Ereignisprotokolltyps. Dieser Wert sollte mithilfe der [**GetLogEventName-Methode**](getlogeventname-win32-tsgatewayserversettings.md) abgerufen werden.

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

*Aktiviert* \[ out\]
</dt> <dd>

Gibt an, ob der angegebene Ereignisprotokolltyp aktiviert ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, gibt sie 0 (null) zurück. Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben. Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste WMI-Anbieterfehlercodes.](terminal-services-wmi-provider-error-codes.md)

## <a name="remarks"></a>Hinweise

Sie müssen Mitglied der Gruppe Administratoren sein, um diese Methode aufzurufen.

Managed Object Format -Dateien (MOF) enthalten die Definitionen für WMI-Klassen (Windows Management Instrumentation). MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

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

 

