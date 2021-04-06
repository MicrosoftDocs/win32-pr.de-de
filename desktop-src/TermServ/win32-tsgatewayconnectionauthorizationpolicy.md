---
title: Win32_TSGatewayConnectionAuthorizationPolicy-Klasse
description: Beschreibt eine Remotedesktop Verbindungs Autorisierungs Richtlinie (RD \ 160; Cap). RD \ 160; Mithilfe von Caps kann festgestellt werden, ob ein Benutzer eine Verbindung mit dem Remotedesktop Gateway-Server (RD-Gateway) herstellen darf.
ms.assetid: 50ff3f97-0818-4e9c-9db7-a822cfed0e82
ms.tgt_platform: multiple
keywords:
- Win32_TSGatewayConnectionAuthorizationPolicy-Klasse Remotedesktopdienste
- Win32_TSGatewayConnectionAuthorizationPolicy Klasse Remotedesktopdienste, beschrieben
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
ms.openlocfilehash: 27384ec3a5f17c3e41fe0ceccf0ee1f7f9d08044
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858838"
---
# <a name="win32_tsgatewayconnectionauthorizationpolicy-class"></a>Win32-Klasse "t- \_ gatewayconnectionauthorizationpolicy"

Beschreibt eine Remotedesktop Verbindungs Autorisierungs Richtlinie (RD-CAP). RD-CAPs werden verwendet, um zu bestimmen, ob ein Benutzer eine Verbindung mit dem Remotedesktop Gateway-Server (RD-Gateway) herstellen darf.

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

Die Win32-Klasse " **\_ zgatewayconnectionauthorizationpolicy** " verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die Win32-Klasse " **\_ zgatewayconnectionauthorizationpolicy** " verfügt über diese Methoden.



| Methode                                                                                                                | BESCHREIBUNG                                                                                                                                                                     |
|:----------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Addcomputergroupnames**](addcomputergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)                   | Fügt die angegebenen Computer Gruppennamen der **computergroupnames** -Eigenschaft hinzu.<br/>                                                                                      |
| [**Addusergroupnames**](addusergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)                           | Fügt die angegebenen Benutzergruppen Namen der **usergroupnames** -Eigenschaft hinzu.<br/>                                                                                              |
| [**Stelle**](create-win32-tsgatewayconnectionauthorizationpolicy.md)                                                 | Erstellt eine RD-Obergrenze.<br/>                                                                                                                                                   |
| [**Lösch**](delete-win32-tsgatewayconnectionauthorizationpolicy.md)                                                 | Löscht die aktuelle RD-Obergrenze.<br/>                                                                                                                                          |
| [**Disableclipboard**](disableclipboard-win32-tsgatewayconnectionauthorizationpolicy.md)                             | Legt die **clipboarddeaktiviert** -Eigenschaft fest.<br/>                                                                                                                             |
| [**Disablediskdrives**](disablediskdrives-win32-tsgatewayconnectionauthorizationpolicy.md)                           | Legt die **diskdrivesdeaktivierte** Eigenschaft fest.<br/>                                                                                                                            |
| [**Disableplugandplaydevices**](disableplugandplaydevices-win32-tsgatewayconnectionauthorizationpolicy.md)           | Legt die **plugandplaydevicesdeaktiviert** -Eigenschaft fest.<br/>                                                                                                                    |
| [**Disableprinter**](disableprinters-win32-tsgatewayconnectionauthorizationpolicy.md)                               | Legt die **printersdeaktiviert** -Eigenschaft fest.<br/>                                                                                                                              |
| [**Disableserialports**](disableserialports-win32-tsgatewayconnectionauthorizationpolicy.md)                         | Legt die **serialportsdeaktiviert** -Eigenschaft fest.<br/>                                                                                                                           |
| [**Enablezugewonlysdrservers**](win32-tsgatewayconnectionauthorizationpolicy-enableallowonlysdrservers.md)           | Dient **zum Umschalten der Eigenschaft** "" der Eigenschaft "Eigenschaft".<br/> **Windows Server 2008:** Diese Methode ist vor Windows Server 2008 R2 nicht verfügbar.<br/>                  |
| [**Nach unten**](movedown-win32-tsgatewayconnectionauthorizationpolicy.md)                                             | Verschiebt die aktuelle RD-Obergrenze in der Liste um eine Position nach unten.<br/>                                                                                                              |
| [**MoveUp**](moveup-win32-tsgatewayconnectionauthorizationpolicy.md)                                                 | Verschiebt die aktuelle RD-Obergrenze in der Liste um eine Position nach oben.<br/>                                                                                                                |
| [**Removecomputergroupnames**](removecomputergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)             | Entfernt die angegebenen Computer Gruppennamen aus der **computergroupnames** -Eigenschaft.<br/>                                                                                 |
| [**Removeusergroupnames**](removeusergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)                     | Entfernt die angegebenen Benutzergruppen Namen aus der **usergroupnames** -Eigenschaft.<br/>                                                                                             |
| [**Setcomputergroupnames**](setcomputergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)                   | Legt die **computergroupnames** -Eigenschaft fest.<br/>                                                                                                                            |
| [**Setcookieauthenticationallowed**](setcookieauthenticationallowed-win32-tsgatewayconnectionauthorizationpolicy.md) | Legt die **cookieauthenticationallowed** -Eigenschaft fest.<br/> **Windows Server 2008:** Diese Methode ist nicht verfügbar.<br/>                                                 |
| [**Setdeviceredirectiontype**](setdeviceredirectiontype-win32-tsgatewayconnectionauthorizationpolicy.md)             | Legt die **deviceredirectiontype** -Eigenschaft fest.<br/>                                                                                                                         |
| [**Abgeleitete**](setenabled-win32-tsgatewayconnectionauthorizationpolicy.md)                                         | Aktiviert oder deaktiviert das aktuelle RD-CAP.<br/>                                                                                                                              |
| [**"-Timeout"**](setidletimeout-win32-tsgatewayconnectionauthorizationpolicy.md)                                 | Legt die **IdleTimeout** -Eigenschaft fest.<br/> **Windows Server 2008:** Diese Methode ist vor Windows Server 2008 R2 nicht verfügbar.<br/>                                   |
| [**SetName**](setname-win32-tsgatewayconnectionauthorizationpolicy.md)                                               | Legt einen neuen Namen für diese RD-Obergrenze fest. Mit dieser Methode wird sichergestellt, dass die Namen eindeutig sind.<br/>                                                                                      |
| [**Setpasswordallowed**](setpasswordallowed-win32-tsgatewayconnectionauthorizationpolicy.md)                         | Legt die **passwordallowed** -Eigenschaft fest.<br/>                                                                                                                               |
| [**Setsecureidallowed zulässig**](setsecureidallowed-win32-tsgatewayconnectionauthorizationpolicy.md)                         | Legt die Eigenschaft " **secureidallowed** " fest.<br/> **Windows Server 2008:** Diese Methode ist für die zukünftige Verwendung reserviert.<br/>                                                   |
| [**-Sitzungs Timeout**](setsessiontimeout-win32-tsgatewayconnectionauthorizationpolicy.md)                           | Legt die Eigenschaften **sessiontimeout** und **sessiontimeoutaction** fest.<br/> **Windows Server 2008:** Diese Methode ist vor Windows Server 2008 R2 nicht verfügbar.<br/> |
| [**"Abkto" ist zulässig.**](setsmartcardallowed-win32-tsgatewayconnectionauthorizationpolicy.md)                       | Legt die **smartcardallowed** -Eigenschaft fest.<br/>                                                                                                                              |
| [**Setusergroupnames**](setusergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)                           | Legt die **usergroupnames** -Eigenschaft fest.<br/>                                                                                                                                |
| [**Aktualisieren**](update-win32-tsgatewayconnectionauthorizationpolicy.md)                                                 | Aktualisiert das aktuelle RD-CAP.<br/>                                                                                                                                          |



 

### <a name="properties"></a>Eigenschaften

Die Win32-Klasse "t- **\_ gatewayconnectionauthorizationpolicy** " verfügt über diese Eigenschaften.

<dl> <dt>

**"Zuweisung der Server"**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob Verbindungen nur für die Sicherung von RDS-Servern (Geräte Umleitung) zulässig sind. Diese Eigenschaft kann mithilfe der [**enablezugewonlysdrservers**](win32-tsgatewayconnectionauthorizationpolicy-enableallowonlysdrservers.md) -Methode festgelegt werden.

**Windows Server 2008:** Diese Eigenschaft ist vor Windows Server 2008 R2 nicht verfügbar.

</dd> <dt>

**Clipboarddeaktiviert**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die Umleitung der Zwischenablage deaktiviert wird. Diese Eigenschaft hat nur dann Auswirkungen, wenn die **deviceredirectiontype** -Eigenschaft den Wert "2" aufweist.

</dd> <dt>

**Computer groupnames**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Liste von durch Semikolons getrennten Computer Gruppennamen. Dieser Wert kann leer sein. Die Namen weisen das Format *Domäne \\ computergroupname* auf. Wenn ein Wert angegeben wird, muss der Client Computer zu einer dieser Computer Gruppen gehören, damit der Benutzer auf den RD-Gateway Server zugreifen kann.

</dd> <dt>

**Cookieauthenticationallowed**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob eine Cookie-Authentifizierung zum Herstellen einer Verbindung mit dem RD-Gateway Server verwendet werden kann. Diese Eigenschaft kann mit der [**setcookieauthenticationallowed**](setcookieauthenticationallowed-win32-tsgatewayconnectionauthorizationpolicy.md) -Methode festgelegt werden.

**Windows Server 2008:** Diese Eigenschaft ist nicht verfügbar.

</dd> <dt>

**Deviceredirectiontype**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
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

Keine Geräte werden umgeleitet.

</dd> <dt>

2
</dt> <dd>

Angegebene Geräte werden nicht umgeleitet. Die Eigenschaften **diskdrivesdeaktiviert**, **printersdeaktiviert**, **serialportsdeaktiviert**, **clipboarddeaktiviert** und **plugandplaydevicesdeaktiviert** steuern, welche Geräte nicht umgeleitet werden.

</dd> </dl>

</dd> <dt>

**Diskdrivesdeaktivierte**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die Laufwerk Umleitung deaktiviert wird. Diese Eigenschaft hat nur dann Auswirkungen, wenn die **deviceredirectiontype** -Eigenschaft den Wert "2" aufweist.

</dd> <dt>

**Aktiviert**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob dieses RD-CAP zum Auswerten eines Benutzers für die Autorisierung verwendet wird.

</dd> <dt>

**Hasnapattributes**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die RD-Abdeckung Network Access Protection (NAP)-Attribute verwendet.

</dd> <dt>

**IdleTimeout**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Wert für das Leerlauf Timeout (in Minuten). Der Wert 0 bedeutet, dass kein Timeout vorliegt. Diese Eigenschaft kann mit der [**setidletimeout**](setidletimeout-win32-tsgatewayconnectionauthorizationpolicy.md) -Methode festgelegt werden.

**Windows Server 2008:** Diese Eigenschaft ist nicht verfügbar.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Name der RD-Obergrenze.

</dd> <dt>

**Order**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Auswertungs Reihenfolge für die RD-CAP. Das erste ausgewertete RD-CAP weist den Wert "1" auf. Die **Order** -Eigenschaft kann geändert werden, wenn die Methoden [**Create**](create-win32-tsgatewayconnectionauthorizationpolicy.md), [**Delete**](delete-win32-tsgatewayconnectionauthorizationpolicy.md), [**moveUp**](moveup-win32-tsgatewayconnectionauthorizationpolicy.md)oder [**muvedown**](movedown-win32-tsgatewayconnectionauthorizationpolicy.md) aufgerufen werden.

</dd> <dt>

**Passwordallowed**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob ein Kennwort zum Herstellen einer Verbindung mit dem RD-Gateway Server verwendet werden kann. Diese Eigenschaft kann mithilfe der [**setpasswordallowed**](setpasswordallowed-win32-tsgatewayconnectionauthorizationpolicy.md) -Methode geändert werden.

</dd> <dt>

**Plugandplaydevicesdeaktiviert**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die Umleitung von Plug & Play Geräten deaktiviert wird. Diese Eigenschaft hat nur dann Auswirkungen, wenn die **deviceredirectiontype** -Eigenschaft den Wert "2" aufweist.

</dd> <dt>

**"Printersdeaktiviert"**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die Drucker Umleitung deaktiviert wird. Diese Eigenschaft hat nur dann Auswirkungen, wenn die **deviceredirectiontype** -Eigenschaft den Wert "2" aufweist.

</dd> <dt>

**Secureidallowed zulässig**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob ein sicherer Bezeichner verwendet werden kann, um eine Verbindung mit dem RD-Gateway-Server herzustellen.

**Windows Server 2008:** Diese Eigenschaft wird nicht verwendet.

</dd> <dt>

**Serialportsdeaktiviert**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die serielle Port Umleitung deaktiviert wird. Diese Eigenschaft hat nur dann Auswirkungen, wenn die **deviceredirectiontype** -Eigenschaft den Wert "2" aufweist.

</dd> <dt>

**SessionTimeout**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Sitzungs Timeout Wert (in Minuten). Der Wert 0 bedeutet, dass kein Timeout vorliegt. Diese Eigenschaft kann mit der [**sezessiontimeout**](setsessiontimeout-win32-tsgatewayconnectionauthorizationpolicy.md) -Methode festgelegt werden.

**Windows Server 2008:** Diese Eigenschaft ist nicht verfügbar.

</dd> <dt>

**Sessiontimeoutaction**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt die Aktion an, die bei einem Sitzungs Timeout durchgeführt werden soll. Diese Eigenschaft kann mit der [**sezessiontimeout**](setsessiontimeout-win32-tsgatewayconnectionauthorizationpolicy.md) -Methode festgelegt werden.

Dies kann einer der folgenden Werte sein:

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

**Smartcardzulässig**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob eine Smartcard verwendet werden kann, um eine Verbindung mit dem RD-Gateway-Server herzustellen. Diese Eigenschaft kann mithilfe der Methode "* [**zmartcardallowed**](setsmartcardallowed-win32-tsgatewayconnectionauthorizationpolicy.md) " geändert werden.

</dd> <dt>

**Usergroupnames**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Liste von durch Semikolon getrennten Benutzergruppen Namen. Die Namen weisen das Format *Domäne \\ usergroupname* auf. Wenn der Benutzer zu einer dieser Benutzergruppen gehört, erhält der Benutzer Zugriff auf den RD-Gateway Server.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Klasse verwenden zu können.

Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                           |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                 |
| MOF<br/>                      | <dl> <dt>"T-Gateway. mof"</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32-"- \_ gatewayconnection"**](win32-tsgatewayconnection.md)
</dt> <dt>

[**Win32-"t- \_ gatewayloadbalancer"**](win32-tsgatewayloadbalancer.md)
</dt> <dt>

[**Win32-"t- \_ gatewayradiusserver"**](win32-tsgatewayradiusserver.md)
</dt> <dt>

[**Win32- \_ faigatewayresourceauthorizationpolicy**](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> <dt>

[**Win32-Datei " \_ zgatewayresourcegroup"**](win32-tsgatewayresourcegroup.md)
</dt> <dt>

[**Win32-Datei- \_ gatewayserversettings**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

