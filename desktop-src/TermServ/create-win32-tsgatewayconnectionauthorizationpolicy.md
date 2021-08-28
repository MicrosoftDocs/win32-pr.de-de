---
title: Create-Methode der Win32_TSGatewayConnectionAuthorizationPolicy Klasse
description: Erstellt eine Remotedesktop Verbindungsautorisierungsrichtlinie (RD \ 160; CAP) mithilfe der angegebenen Werte. Das neue RD \ 160; CAP wird oben auf rd \ 160 eingefügt. CAP-Auswertungsauftrag mit dem Order-Eigenschaftswert \0034;1 \ 0034;.
ms.assetid: 0010cd2b-9c23-488a-9337-d2ed338136d3
ms.tgt_platform: multiple
keywords:
- Erstellen einer Remotedesktopdienste
- Create method Remotedesktopdienste , Win32_TSGatewayConnectionAuthorizationPolicy class
- Win32_TSGatewayConnectionAuthorizationPolicy klasse Remotedesktopdienste , Create-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.Create
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b16bf9dadb2a76a46d607a6cf2554192e3658686b58a089c19c3604c0c510bc5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119871860"
---
# <a name="create-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a>Create-Methode der Win32 \_ TSGatewayConnectionAuthorizationPolicy-Klasse

Erstellt eine Remotedesktop-Verbindungsautorisierungsrichtlinie (RD CAP) mithilfe der angegebenen Werte. Die neue RD-CAP wird am Anfang der Rd CAP-Auswertungsauftrag eingefügt, mit dem **Order-Eigenschaftswert** "1".

## <a name="syntax"></a>Syntax


```mof
uint32 Create(
  [in] string  Name,
  [in] string  UserGroupNames,
  [in] string  ComputerGroupNames,
  [in] boolean SmartCard,
  [in] boolean Password,
  [in] boolean SecureId,
  [in] boolean Enabled,
  [in] uint32  DeviceRedirectionType,
  [in] boolean DiskDrivesDisabled,
  [in] boolean PrintersDisabled,
  [in] boolean SerialPortsDisabled,
  [in] boolean ClipboardDisabled,
  [in] boolean PlugAndPlayDevicesDisabled,
  [in] uint32  IdleTimeout,
  [in] uint32  SessionTimeout,
  [in] uint32  SessionTimeoutAction,
  [in] boolean AllowOnlySDRServers,
  [in] boolean CookieAuthentication
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Name* \[ In\]
</dt> <dd>

Name der RD-CAP. Der Name muss mindestens 64 Zeichen lang sein, muss eindeutig sein (case wird ignoriert) und darf nicht die folgenden reservierten Zeichen enthalten:

<> : ; " / \\ \| ? \*\[REGISTERKARTE\]

</dd> <dt>

*UserGroupNames* \[ In\]
</dt> <dd>

Liste der durch Semikolons getrennten Benutzergruppennamen für die neue RD-CAP.

</dd> <dt>

*ComputerGroupNames* \[ In\]
</dt> <dd>

Liste der Durch Semikolons getrennten Computergruppennamen für die neue RD-CAP.

</dd> <dt>

*SmartCard* \[ In\]
</dt> <dd>

Gibt an, ob Smartcards für die Authentifizierung beim RD-Gatewayserver verwendet werden können.

</dd> <dt>

*Kennwort* \[ In\]
</dt> <dd>

Gibt an, ob Kennwörter für die Authentifizierung beim RD-Gatewayserver verwendet werden können.

</dd> <dt>

*SecureId* \[ In\]
</dt> <dd>

Dieser Parameter ist für die zukünftige Verwendung reserviert.

</dd> <dt>

*Aktiviert* \[ In\]
</dt> <dd>

Gibt an, ob diese RD-CAP aktiviert ist.

</dd> <dt>

*DeviceRedirectionType* \[ In\]
</dt> <dd>

Gibt an, welche Gerätetypen umgeleitet werden.

<dt>

0
</dt> <dd>

Alle Geräte werden umgeleitet.

</dd> <dt>

1
</dt> <dd>

Es werden keine Geräte umgeleitet.

</dd> <dt>

2
</dt> <dd>

Angegebene Geräte werden nicht umgeleitet. Die *Parameter DiskDrivesDisabled,* *PrinterDisabled,* *SerialPortsDisabled,* *ClipboardDisabled* und *PlugAndPlayDevicesDisabled* steuern, welche Geräte nicht umgeleitet werden.

</dd> </dl> </dd> <dt>

*DiskDrivesDisabled* \[ In\]
</dt> <dd>

Gibt an, ob die Laufwerkumleitung deaktiviert werden soll, wenn *der DeviceRedirectionType-Parameter* "2" ist.

</dd> <dt>

*PrinterDisabled* \[ In\]
</dt> <dd>

Gibt an, ob die Druckerumleitung deaktiviert werden soll, wenn *der DeviceRedirectionType-Parameter* "2" ist.

</dd> <dt>

*SerialPortsDisabled* \[ In\]
</dt> <dd>

Gibt an, ob die Umleitung des seriellen Ports deaktiviert werden soll, wenn der *DeviceRedirectionType-Parameter* "2" ist.

</dd> <dt>

*ZwischenablageDeabled* \[ In\]
</dt> <dd>

Gibt an, ob die Umleitung der Zwischenablage deaktiviert werden soll, wenn der *DeviceRedirectionType-Parameter* "2" ist.

</dd> <dt>

*PlugAndPlayDevicesDisabled* \[ In\]
</dt> <dd>

Specifies whether to disable redirection of Plug and Play devices if the *DeviceRedirectionType* parameter is "2".

</dd> <dt>

*IdleTimeout* \[ In\]
</dt> <dd>

Leerlaufzeitüberschreitungswert in Minuten

</dd> <dt>

*SessionTimeout* \[ In\]
</dt> <dd>

Sitzungszeitüberschreitungswert in Minuten

</dd> <dt>

*SessionTimeoutAction* \[ In\]
</dt> <dd>

Sitzungszeitüberschreitungsaktion in Minuten

</dd> <dt>

*AllowOnlySDRServers* \[ In\]
</dt> <dd>

Gibt an, ob Verbindungen nur mit SDR-TS-Servern zulässig sind

</dd> <dt>

*CookieAuthentication* \[ In\]
</dt> <dd>

Gibt an, ob die Cookieauthentifizierung verwendet werden kann, um eine Verbindung mit dem TS-Gatewayserver herzustellen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, gibt sie 0 (null) zurück. Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben. Eine Liste der Fehlercodes finden Sie unter Remotedesktopdienste [WMI-Anbieterfehlercodes](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Hinweise

Sie müssen Mitglied der Gruppe Administratoren sein, um diese Methode aufrufen zu können.

Managed Object Format (MOF) enthalten die Definitionen für WMI-Klassen (Windows Management Instrumentation). MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                           |
| Namespace<br/>                | \\ \\ CiMv2-Stammterminaldienste<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ TSGatewayConnectionAuthorizationPolicy**](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

