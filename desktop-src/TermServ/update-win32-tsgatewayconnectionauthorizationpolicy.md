---
title: Update-Methode der Win32_TSGatewayConnectionAuthorizationPolicy-Klasse
description: Aktualisiert die aktuelle Remotedesktop Verbindungs Autorisierungs Richtlinie (RD \ 160; Cap).
ms.assetid: 6d13d1b7-1c7d-4d22-b42c-36e0f4446e86
ms.tgt_platform: multiple
keywords:
- Update-Methode Remotedesktopdienste
- Update-Methode Remotedesktopdienste, Win32_TSGatewayConnectionAuthorizationPolicy-Klasse
- Win32_TSGatewayConnectionAuthorizationPolicy-Klasse Remotedesktopdienste, Update-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.Update
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87b982030170e954342dc5ff99754dcb89afd0e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040682"
---
# <a name="update-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a>Update-Methode der Win32-Klasse "t- \_ gatewayconnectionauthorizationpolicy"

Aktualisiert die aktuelle Remotedesktop Verbindungs Autorisierungs Richtlinie (RD-CAP).

## <a name="syntax"></a>Syntax


```mof
uint32 Update(
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

*Name* \[ in\]
</dt> <dd>

Name der RD-Obergrenze. Der Name muss 64 Zeichen oder kleiner, eindeutig (Groß-/Kleinschreibung wird ignoriert) sein und darf die folgenden reservierten Zeichen nicht enthalten:

<> :; " / \\ \| ? \*\[Registerkarte\]

</dd> <dt>

*Usergroupnames* \[ in\]
</dt> <dd>

Liste von durch Semikolon getrennten Benutzergruppen Namen. Die Namen weisen das Format *Domäne \\ usergroupname* auf. Wenn der Benutzer zu einer dieser Benutzergruppen gehört, erhält der Benutzer Zugriff auf den RD-Gateway Server.

</dd> <dt>

*Computer groupnames* \[ in\]
</dt> <dd>

Liste von durch Semikolons getrennten Computer Gruppennamen. Dieser Wert kann leer sein. Die Namen weisen das Format *Domäne \\ computergroupname* auf. Wenn ein Wert angegeben wird, muss der Client Computer zu einer dieser Computer Gruppen gehören, damit der Benutzer auf den RD-Gateway Server zugreifen kann.

</dd> <dt>

*Smartcard* \[ in\]
</dt> <dd>

Gibt an, ob Smartcards zum Authentifizieren beim RD-Gateway Server verwendet werden können.

</dd> <dt>

*Kennwort* \[ in\]
</dt> <dd>

Gibt an, ob Kenn Wörter verwendet werden können, um sich beim RD-Gateway Server zu authentifizieren.

</dd> <dt>

*SecureID* \[ in\]
</dt> <dd>

Dieser Parameter ist für die zukünftige Verwendung reserviert.

</dd> <dt>

*Aktiviert* \[ in\]
</dt> <dd>

Gibt an, ob dieses RD-CAP aktiviert ist.

</dd> <dt>

*Deviceredirectiontype* \[ in\]
</dt> <dd>

Gibt an, welche Gerätetypen umgeleitet werden.

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

Angegebene Geräte werden nicht umgeleitet. Die Parameter *diskdrivesdebug*, *printersdeaktiviert*, *serialportsdeaktiviert*, *clipboarddeaktiviert* und *plugandplaydevicesdeaktiviert* steuern, welche Geräte nicht umgeleitet werden.

</dd> </dl> </dd> <dt>

*Diskdrivesdeaktivierte* \[ in\]
</dt> <dd>

Gibt an, ob die Laufwerk Umleitung deaktiviert werden soll, wenn der *deviceredirectiontype* -Parameter den Wert "2" aufweist.

</dd> <dt>

" *Printersdeaktiviert* \[ " in\]
</dt> <dd>

Gibt an, ob die Drucker Umleitung deaktiviert werden soll, wenn der *deviceredirectiontype* -Parameter den Wert "2" aufweist.

</dd> <dt>

*Serialportsdeaktiviert* \[ in\]
</dt> <dd>

Gibt an, ob die serielle Port Umleitung deaktiviert werden soll, wenn der *deviceredirectiontype* -Parameter "2" ist.

</dd> <dt>

*Clipboarddeaktiviert* \[ in\]
</dt> <dd>

Gibt an, ob die Zwischenablage Umleitung deaktiviert werden soll, wenn der *deviceredirectiontype* -Parameter "2" ist.

</dd> <dt>

*Plugandplaydevicesdeaktiviert* \[ in\]
</dt> <dd>

Gibt an, ob die Umleitung von Plug & Play Geräten deaktiviert werden soll, wenn der *deviceredirectiontype* -Parameter "2" ist.

</dd> <dt>

*IdleTimeout* \[ in\]
</dt> <dd>

Leerlauf Timeout Wert in Minuten

</dd> <dt>

*Sessiontimeout* \[ in\]
</dt> <dd>

Sitzungs Timeout Wert in Minuten

</dd> <dt>

*Sessiontimeoutaction* \[ in\]
</dt> <dd>

Sitzungs Timeout Aktion in Minuten

</dd> <dt>

" *Zuweisung der Server* \[ " in\]
</dt> <dd>

Gibt an, ob Verbindungen nur für Server mit SZR zulässig sind

</dd> <dt>

*Cookieauthentifizierung* \[ in\]
</dt> <dd>

Gibt an, ob für die Verbindung mit dem Terminaldienstegateway-Server eine Cookie-Authentifizierung

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück. Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben. Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Bemerkungen

Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.

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

[**Win32- \_ faigatewayconnectionauthorizationpolicy**](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

