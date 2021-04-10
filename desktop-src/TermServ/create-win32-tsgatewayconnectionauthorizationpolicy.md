---
title: Create-Methode der Win32_TSGatewayConnectionAuthorizationPolicy-Klasse
description: Erstellt eine Remotedesktop Verbindungs Autorisierungs Richtlinie (RD \ 160; Cap) unter Verwendung der angegebenen Werte. Die neue RD \ 160; Die Obergrenze wird am oberen Rand des RD \ 160; eingefügt. Cap-Auswertungs Reihenfolge mit einem Order-Eigenschafts Wert von \ 0034; 1 \ 0034;.
ms.assetid: 0010cd2b-9c23-488a-9337-d2ed338136d3
ms.tgt_platform: multiple
keywords:
- Create-Methode Remotedesktopdienste
- Create Method Remotedesktopdienste, Win32_TSGatewayConnectionAuthorizationPolicy-Klasse
- Win32_TSGatewayConnectionAuthorizationPolicy Klasse Remotedesktopdienste, Methode erstellen
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
ms.openlocfilehash: edc027c2f7fc90318bd1af6fd1254077a860a5d8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040273"
---
# <a name="create-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a>Create-Methode der Win32-Klasse "t- \_ gatewayconnectionauthorizationpolicy"

Erstellt eine Remotedesktop Verbindungs Autorisierungs Richtlinie (RD-CAP) mithilfe der angegebenen Werte. Die neue RD-Obergrenze wird am oberen Rand der Auswertungs Reihenfolge für die RD-CAP eingefügt, wobei der Wert für die **Order** -Eigenschaft "1" lautet.

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

*Name* \[ in\]
</dt> <dd>

Name der RD-Obergrenze. Der Name muss 64 Zeichen oder kleiner, eindeutig (Groß-/Kleinschreibung wird ignoriert) sein und darf die folgenden reservierten Zeichen nicht enthalten:

<> :; " / \\ \| ? \*\[Registerkarte\]

</dd> <dt>

*Usergroupnames* \[ in\]
</dt> <dd>

Eine Liste von Benutzergruppen Namen, die durch Semikolons getrennt sind, für die neue RD-Obergrenze.

</dd> <dt>

*Computer groupnames* \[ in\]
</dt> <dd>

Die Liste der Computer Gruppennamen, die durch Semikolons getrennt sind, für die neue RD-Obergrenze.

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

 

