---
title: Win32_TSGatewayConnectionAuthorizationPolicy-Klasse
description: Beschreibt eine Remotedesktop Verbindungsautorisierungsrichtlinie (RD \ 160; CAP). RD \ 160; CAPs werden verwendet, um zu bestimmen, ob ein Benutzer eine Verbindung mit dem Remotedesktop Gateway-Server (RD-Gateway) herstellen darf.
ms.assetid: 50ff3f97-0818-4e9c-9db7-a822cfed0e82
ms.tgt_platform: multiple
keywords:
- Win32_TSGatewayConnectionAuthorizationPolicy-Klassen-Remotedesktopdienste
- Win32_TSGatewayConnectionAuthorizationPolicy-Klasse Remotedesktopdienste beschrieben
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy
- Win32_TSGatewayConnectionAuthorizationPolicy.Name
- Win32_TSGatewayConnectionAuthorizationPolicy.Order
- Win32_TSGatewayConnectionAuthorizationPolicy.SmartcardAllowed
- Win32_TSGatewayConnectionAuthorizationPolicy.PasswordAllowed
- Win32_TSGatewayConnectionAuthorizationPolicy.SecureIdAllowed
- Win32_TSGatewayConnectionAuthorizationPolicy.CookieAuthenticationAllowed
- Win32_TSGatewayConnectionAuthorizationPolicy.Enabled
- Win32_TSGatewayConnectionAuthorizationPolicy.IdleTimeout
- Win32_TSGatewayConnectionAuthorizationPolicy.SessionTimeout
- Win32_TSGatewayConnectionAuthorizationPolicy.SessionTimeoutAction
- Win32_TSGatewayConnectionAuthorizationPolicy.DeviceRedirectionType
- Win32_TSGatewayConnectionAuthorizationPolicy.DiskDrivesDisabled
- Win32_TSGatewayConnectionAuthorizationPolicy.PrintersDisabled
- Win32_TSGatewayConnectionAuthorizationPolicy.SerialPortsDisabled
- Win32_TSGatewayConnectionAuthorizationPolicy.ClipboardDisabled
- Win32_TSGatewayConnectionAuthorizationPolicy.PlugAndPlayDevicesDisabled
- Win32_TSGatewayConnectionAuthorizationPolicy.UserGroupNames
- Win32_TSGatewayConnectionAuthorizationPolicy.ComputerGroupNames
- Win32_TSGatewayConnectionAuthorizationPolicy.HasNapAttributes
- Win32_TSGatewayConnectionAuthorizationPolicy.AllowOnlySDRServers
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bfaefb0a3062db27622afe90023928507c6d127c64edb60041347f73c1b261c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118349245"
---
# <a name="win32_tsgatewayconnectionauthorizationpolicy-class"></a>Win32 \_ TSGatewayConnectionAuthorizationPolicy-Klasse

Beschreibt eine Remotedesktop Verbindungsautorisierungsrichtlinie (RD CAP). RD-CAPs werden verwendet, um zu bestimmen, ob ein Benutzer eine Verbindung mit dem Remotedesktop Gateway-Server (RD-Gateway) herstellen darf.

## <a name="syntax"></a>Syntax

``` syntax
[dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayConnectionAuthorizationPolicy
{
  string  Name;
  uint32  Order;
  boolean SmartcardAllowed;
  boolean PasswordAllowed;
  boolean SecureIdAllowed;
  boolean CookieAuthenticationAllowed;
  boolean Enabled;
  uint32  IdleTimeout;
  uint32  SessionTimeout;
  uint32  SessionTimeoutAction;
  uint32  DeviceRedirectionType;
  boolean DiskDrivesDisabled;
  boolean PrintersDisabled;
  boolean SerialPortsDisabled;
  boolean ClipboardDisabled;
  boolean PlugAndPlayDevicesDisabled;
  string  UserGroupNames;
  string  ComputerGroupNames;
  boolean HasNapAttributes;
  boolean AllowOnlySDRServers;
};
```

## <a name="members"></a>Member

Die **Win32 \_ TSGatewayConnectionAuthorizationPolicy-Klasse** verfügt über folgende Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **Win32 \_ TSGatewayConnectionAuthorizationPolicy-Klasse** verfügt über diese Methoden.



| Methode                                                                                                                | BESCHREIBUNG                                                                                                                                                                     |
|:----------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddComputerGroupNames**](addcomputergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)                   | Fügt der **ComputerGroupNames-Eigenschaft** die angegebenen Computergruppennamen hinzu.<br/>                                                                                      |
| [**AddUserGroupNames**](addusergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)                           | Fügt der **UserGroupNames-Eigenschaft** die angegebenen Benutzergruppennamen hinzu.<br/>                                                                                              |
| [**Erstellen**](create-win32-tsgatewayconnectionauthorizationpolicy.md)                                                 | Erstellt eine RD-CAP.<br/>                                                                                                                                                   |
| [**Löschen**](delete-win32-tsgatewayconnectionauthorizationpolicy.md)                                                 | Löscht die aktuelle RD-CAP.<br/>                                                                                                                                          |
| [**DisableClipboard**](disableclipboard-win32-tsgatewayconnectionauthorizationpolicy.md)                             | Legt die **ClipboardDisabled-Eigenschaft fest.**<br/>                                                                                                                             |
| [**DisableDiskDrives**](disablediskdrives-win32-tsgatewayconnectionauthorizationpolicy.md)                           | Legt die **DiskDrivesDisabled-Eigenschaft fest.**<br/>                                                                                                                            |
| [**DisablePlugAndPlayDevices**](disableplugandplaydevices-win32-tsgatewayconnectionauthorizationpolicy.md)           | Legt die **PlugAndPlayDevicesDisabled-Eigenschaft fest.**<br/>                                                                                                                    |
| [**DisablePrinters**](disableprinters-win32-tsgatewayconnectionauthorizationpolicy.md)                               | Legt die **PrinterDisabled-Eigenschaft fest.**<br/>                                                                                                                              |
| [**DisableSerialPorts**](disableserialports-win32-tsgatewayconnectionauthorizationpolicy.md)                         | Legt die **SerialPortsDisabled-Eigenschaft fest.**<br/>                                                                                                                           |
| [**EnableAllowOnlySDRServers**](win32-tsgatewayconnectionauthorizationpolicy-enableallowonlysdrservers.md)           | Wird verwendet, um die **AllowOnlySDRServers-Eigenschaft** umzuschalten.<br/> **Windows Server 2008:** Diese Methode ist vor Windows Server 2008 R2 nicht verfügbar.<br/>                  |
| [**Movedown**](movedown-win32-tsgatewayconnectionauthorizationpolicy.md)                                             | Verschiebt die aktuelle RD-CAP um eine Position nach unten in der Liste.<br/>                                                                                                              |
| [**MoveUp**](moveup-win32-tsgatewayconnectionauthorizationpolicy.md)                                                 | Verschiebt die aktuelle RD-CAP um eine Position nach oben in der Liste.<br/>                                                                                                                |
| [**RemoveComputerGroupNames**](removecomputergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)             | Entfernt die angegebenen Computergruppennamen aus der **ComputerGroupNames-Eigenschaft.**<br/>                                                                                 |
| [**RemoveUserGroupNames**](removeusergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)                     | Entfernt angegebene Benutzergruppennamen aus der **UserGroupNames-Eigenschaft.**<br/>                                                                                             |
| [**SetComputerGroupNames**](setcomputergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)                   | Legt die **ComputerGroupNames-Eigenschaft** fest.<br/>                                                                                                                            |
| [**SetCookieAuthenticationAllowed**](setcookieauthenticationallowed-win32-tsgatewayconnectionauthorizationpolicy.md) | Legt die **CookieAuthenticationAllowed-Eigenschaft** fest.<br/> **Windows Server 2008:** Diese Methode ist nicht verfügbar.<br/>                                                 |
| [**SetDeviceRedirectionType**](setdeviceredirectiontype-win32-tsgatewayconnectionauthorizationpolicy.md)             | Legt die **DeviceRedirectionType-Eigenschaft** fest.<br/>                                                                                                                         |
| [**SetEnabled**](setenabled-win32-tsgatewayconnectionauthorizationpolicy.md)                                         | Aktiviert oder deaktiviert die aktuelle RD-CAP.<br/>                                                                                                                              |
| [**SetIdleTimeout**](setidletimeout-win32-tsgatewayconnectionauthorizationpolicy.md)                                 | Legt die **IdleTimeout-Eigenschaft** fest.<br/> **Windows Server 2008:** Diese Methode ist vor Windows Server 2008 R2 nicht verfügbar.<br/>                                   |
| [**SetName**](setname-win32-tsgatewayconnectionauthorizationpolicy.md)                                               | Legt einen neuen Namen für diese RD-CAP fest. Diese Methode stellt sicher, dass Namen eindeutig sind.<br/>                                                                                      |
| [**SetPasswordAllowed**](setpasswordallowed-win32-tsgatewayconnectionauthorizationpolicy.md)                         | Legt die **PasswordAllowed-Eigenschaft** fest.<br/>                                                                                                                               |
| [**SetSecureIdAllowed**](setsecureidallowed-win32-tsgatewayconnectionauthorizationpolicy.md)                         | Legt die **SecureIdAllowed-Eigenschaft** fest.<br/> **Windows Server 2008:** Diese Methode ist für die zukünftige Verwendung reserviert.<br/>                                                   |
| [**SetSessionTimeout**](setsessiontimeout-win32-tsgatewayconnectionauthorizationpolicy.md)                           | Legt die **Eigenschaften SessionTimeout** und **SessionTimeoutAction** fest.<br/> **Windows Server 2008:** Diese Methode ist vor Windows Server 2008 R2 nicht verfügbar.<br/> |
| [**SetSmartcardAllowed**](setsmartcardallowed-win32-tsgatewayconnectionauthorizationpolicy.md)                       | Legt die **SmartcardAllowed-Eigenschaft** fest.<br/>                                                                                                                              |
| [**SetUserGroupNames**](setusergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)                           | Legt die **UserGroupNames-Eigenschaft** fest.<br/>                                                                                                                                |
| [**Aktualisieren**](update-win32-tsgatewayconnectionauthorizationpolicy.md)                                                 | Aktualisiert die aktuelle RD-CAP.<br/>                                                                                                                                          |



 

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ TSGatewayConnectionAuthorizationPolicy-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**AllowOnlySDRServers**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob Verbindungen nur zum Sichern von SDR-RDS-Servern (Device Redirection) zulässig sind. Diese Eigenschaft kann mit der [**EnableAllowOnlySDRServers-Methode**](win32-tsgatewayconnectionauthorizationpolicy-enableallowonlysdrservers.md) festgelegt werden.

**Windows Server 2008:** Diese Eigenschaft ist vor Windows Server 2008 R2 nicht verfügbar.

</dd> <dt>

**ClipboardDisabled**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die Umleitung in der Zwischenablage deaktiviert wird. Diese Eigenschaft hat nur dann eine Auswirkung, wenn die **DeviceRedirectionType-Eigenschaft** den Wert "2" hat.

</dd> <dt>

**ComputerGroupNames**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Liste der durch Semikolons getrennten Computergruppennamen. Dieser Wert kann leer sein. Die Namen haben das Format *Domain \\ ComputerGroupName*. Wenn ein Wert angegeben wird, muss der Clientcomputer einer dieser Computergruppen angehören, damit der Benutzer auf den RD-Gatewayserver zugreifen kann.

</dd> <dt>

**CookieAuthenticationAllowed**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die Cookieauthentifizierung verwendet werden kann, um eine Verbindung mit dem RD-Gatewayserver herzustellen. Diese Eigenschaft kann mithilfe der [**SetCookieAuthenticationAllowed-Methode**](setcookieauthenticationallowed-win32-tsgatewayconnectionauthorizationpolicy.md) festgelegt werden.

**Windows Server 2008:** Diese Eigenschaft ist nicht verfügbar.

</dd> <dt>

**DeviceRedirectionType**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, welche Geräte umgeleitet werden.

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

Angegebene Geräte werden nicht umgeleitet. Die Eigenschaften **DiskDrivesDisabled,** **PrinterDisabled,** **SerialPortsDisabled,** **ClipboardDisabled** und **PlugAndPlayDevicesDisabled** steuern, welche Geräte nicht umgeleitet werden.

</dd> </dl>

</dd> <dt>

**DiskDrivesDisabled**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die Umleitung des Laufwerks deaktiviert wird. Diese Eigenschaft hat nur dann eine Auswirkung, wenn die **DeviceRedirectionType-Eigenschaft** den Wert "2" hat.

</dd> <dt>

**Aktiviert**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob diese RD-CAP verwendet wird, um einen Benutzer für die Autorisierung auszuwerten.

</dd> <dt>

**HasNapAttributes**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die RD-CAP NAP-Attribute (Network Access Protection) verwendet.

</dd> <dt>

**IdleTimeout**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Leerlauftimeoutwert in Minuten. Der Wert 0 bedeutet, dass kein Timeout vorhanden ist. Diese Eigenschaft kann mithilfe der [**SetIdleTimeout-Methode**](setidletimeout-win32-tsgatewayconnectionauthorizationpolicy.md) festgelegt werden.

**Windows Server 2008:** Diese Eigenschaft ist nicht verfügbar.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Name der RD-CAP.

</dd> <dt>

**Order**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Auswertungsreihenfolge der RD-CAP. Die erste ausgewertete RD-CAP hat den Wert "1". Die **Order-Eigenschaft** kann geändert werden, wenn die Methoden [**Create,**](create-win32-tsgatewayconnectionauthorizationpolicy.md) [**Delete,**](delete-win32-tsgatewayconnectionauthorizationpolicy.md) [**MoveUp**](moveup-win32-tsgatewayconnectionauthorizationpolicy.md)oder [**MoveDown**](movedown-win32-tsgatewayconnectionauthorizationpolicy.md) aufgerufen werden.

</dd> <dt>

**PasswordAllowed**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob ein Kennwort zum Herstellen einer Verbindung mit dem RD-Gatewayserver verwendet werden kann. Diese Eigenschaft kann mithilfe der [**SetPasswordAllowed-Methode**](setpasswordallowed-win32-tsgatewayconnectionauthorizationpolicy.md) geändert werden.

</dd> <dt>

**PlugAndPlayDevicesDisabled**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die Umleitung von Plug & Play Geräten deaktiviert wird. Diese Eigenschaft hat nur dann eine Auswirkung, wenn die **DeviceRedirectionType-Eigenschaft** den Wert "2" hat.

</dd> <dt>

**DruckerDisabled**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die Druckerumleitung deaktiviert wird. Diese Eigenschaft hat nur dann eine Auswirkung, wenn die **DeviceRedirectionType-Eigenschaft** den Wert "2" hat.

</dd> <dt>

**SecureIdAllowed**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob ein sicherer Bezeichner zum Herstellen einer Verbindung mit dem RD-Gatewayserver verwendet werden kann.

**Windows Server 2008:** Diese Eigenschaft wird nicht verwendet.

</dd> <dt>

**SerialPortsDisabled**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die Umleitung des seriellen Ports deaktiviert wird. Diese Eigenschaft hat nur dann eine Auswirkung, wenn die **DeviceRedirectionType-Eigenschaft** den Wert "2" hat.

</dd> <dt>

**SessionTimeout**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Sitzungstimeoutwert in Minuten. Der Wert 0 bedeutet, dass kein Timeout vorhanden ist. Diese Eigenschaft kann mithilfe der [**SetSessionTimeout-Methode**](setsessiontimeout-win32-tsgatewayconnectionauthorizationpolicy.md) festgelegt werden.

**Windows Server 2008:** Diese Eigenschaft ist nicht verfügbar.

</dd> <dt>

**SessionTimeoutAction**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt die Aktion an, die bei einem Sitzungstimeout ausgeführt werden soll. Diese Eigenschaft kann mithilfe der [**SetSessionTimeout-Methode**](setsessiontimeout-win32-tsgatewayconnectionauthorizationpolicy.md) festgelegt werden.

Dies kann einer der folgenden Werte sein.

**Windows Server 2008:** Diese Eigenschaft ist nicht verfügbar.

<dt>

0
</dt> <dd>

Trennen Sie die Sitzung.

</dd> <dt>

1
</dt> <dd>

Versuchen Sie, die Sitzung erneut zu autorisieren.

</dd> </dl>

</dd> <dt>

**SmartcardAllowed**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob eine Smartcard zum Herstellen einer Verbindung mit dem RD-Gatewayserver verwendet werden kann. Diese Eigenschaft kann mithilfe der [**SetSmartcardAllowed-Methode**](setsmartcardallowed-win32-tsgatewayconnectionauthorizationpolicy.md) geändert werden.

</dd> <dt>

**UserGroupNames**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Liste der durch Semikolons getrennten Benutzergruppennamen. Die Namen haben das Format *Domain \\ UserGroupName*. Wenn der Benutzer einer dieser Benutzergruppen angehört, wird dem Benutzer der Zugriff auf den RD-Gatewayserver gewährt.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Sie müssen Mitglied der Gruppe Administratoren sein, um diese Klasse verwenden zu können.

Managed Object Format -Dateien (MOF) enthalten die Definitionen für Windows Management Instrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                           |
| Namespace<br/>                | \\ \\ CiMv2-Stammterminaldienste<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ TSGatewayConnection**](win32-tsgatewayconnection.md)
</dt> <dt>

[**Win32 \_ TSGatewayLoadBalancer**](win32-tsgatewayloadbalancer.md)
</dt> <dt>

[**Win32 \_ TSGatewayRADIUSServer**](win32-tsgatewayradiusserver.md)
</dt> <dt>

[**Win32 \_ TSGatewayResourceAuthorizationPolicy**](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> <dt>

[**Win32 \_ TSGatewayResourceGroup**](win32-tsgatewayresourcegroup.md)
</dt> <dt>

[**Win32 \_ TSGatewayServerSettings**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

