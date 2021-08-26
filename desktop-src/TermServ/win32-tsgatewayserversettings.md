---
title: Win32_TSGatewayServerSettings-Klasse
description: Stellt Methoden und Eigenschaften zum Anzeigen und Konfigurieren Remotedesktop Gateway-Servereinstellungen (RD-Gateway) bereit.
ms.assetid: f772bf71-68ef-4345-8123-f6ad50ee4d61
ms.tgt_platform: multiple
keywords:
- Win32_TSGatewayServerSettings-Klasse Remotedesktopdienste
- Win32_TSGatewayServerSettings-Klasse Remotedesktopdienste beschrieben
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings
- Win32_TSGatewayServerSettings.MaxConnections
- Win32_TSGatewayServerSettings.UnlimitedConnections
- Win32_TSGatewayServerSettings.MaximumAllowedConnectionsBySku
- Win32_TSGatewayServerSettings.SkuName
- Win32_TSGatewayServerSettings.MaxProtocols
- Win32_TSGatewayServerSettings.MaxLogEvents
- Win32_TSGatewayServerSettings.adminMessageText
- Win32_TSGatewayServerSettings.adminMessageStartTime
- Win32_TSGatewayServerSettings.adminMessageEndTime
- Win32_TSGatewayServerSettings.consentMessageText
- Win32_TSGatewayServerSettings.OnlyConsentCapableClients
- Win32_TSGatewayServerSettings.CentralCAPEnabled
- Win32_TSGatewayServerSettings.RequestSOH
- Win32_TSGatewayServerSettings.AuthenticationPluginName
- Win32_TSGatewayServerSettings.AuthenticationPluginCLSID
- Win32_TSGatewayServerSettings.AuthenticationPluginDescription
- Win32_TSGatewayServerSettings.AuthorizationPluginName
- Win32_TSGatewayServerSettings.AuthorizationPluginCLSID
- Win32_TSGatewayServerSettings.AuthorizationPluginDescription
- Win32_TSGatewayServerSettings.SslBridging
- Win32_TSGatewayServerSettings.IsConfigured
- Win32_TSGatewayServerSettings.CertHash
- Win32_TSGatewayServerSettings.EnforceChannelBinding
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00c199b4b8e98832dcc8dbe65b8fc2ef636df71c8bd6e3c096670e6333f83a75
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008520"
---
# <a name="win32_tsgatewayserversettings-class"></a>Win32 \_ TSGatewayServerSettings-Klasse

Stellt Methoden und Eigenschaften zum Anzeigen und Konfigurieren Remotedesktop Gateway-Servereinstellungen (RD-Gateway) bereit. Ein Administrator kann diese Klasse verwenden, um einen Satz von Protokollen, den Satz von Ereignissen, die in das Ereignisprotokoll geschrieben werden, und die maximale Anzahl von Verbindungen über das RD-Gateway zu konfigurieren.

## <a name="syntax"></a>Syntax

``` syntax
[dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayServerSettings
{
  uint32  MaxConnections;
  boolean UnlimitedConnections;
  uint32  MaximumAllowedConnectionsBySku;
  string  SkuName;
  uint32  MaxProtocols;
  uint32  MaxLogEvents;
  string  adminMessageText;
  string  adminMessageStartTime;
  string  adminMessageEndTime;
  string  consentMessageText;
  boolean OnlyConsentCapableClients;
  boolean CentralCAPEnabled;
  boolean RequestSOH;
  string  AuthenticationPluginName;
  string  AuthenticationPluginCLSID;
  string  AuthenticationPluginDescription;
  string  AuthorizationPluginName;
  string  AuthorizationPluginCLSID;
  string  AuthorizationPluginDescription;
  uint32  SslBridging;
  boolean IsConfigured;
  uint8   CertHash[];
  boolean EnforceChannelBinding;
};
```

## <a name="members"></a>Member

Die **Win32 \_ TSGatewayServerSettings-Klasse** verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **Win32 \_ TSGatewayServerSettings-Klasse** verfügt über diese Methoden.



| Methode                                                                                                                                             | BESCHREIBUNG                                                                                                                                                                                                                                                      |
|:---------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Konfigurieren**](configure-win32-tsgatewayserversettings.md)                                                                                       | Konfiguriert die IIS- und RPC-Einstellungen, die für den RD-Gatewaydienst erforderlich sind.<br/> **Windows Server 2008:** Diese Methode ist vor Windows Server 2008 R2 nicht verfügbar.<br/>                                                                               |
| [**EnableCentralCAP**](enablecentralcap-win32-tsgatewayserversettings.md)                                                                         | Aktiviert oder deaktiviert die **CentralCAPEnabled-Eigenschaft,** die steuert, ob zentrale Remotedesktop Verbindungsautorisierungsrichtlinienserver (RD CAP) zum Steuern von Verbindungsautorisierungsrichtlinien für diesen Server verwendet werden.<br/>                    |
| [**EnableLogEvent**](enablelogevent-win32-tsgatewayserversettings.md)                                                                             | Aktiviert oder deaktiviert die Protokollierung des angegebenen Ereignistyps.<br/>                                                                                                                                                                                              |
| [**EnableOnlyConsentCapableClients**](enableonlyconsentcapableclients-win32-tsgatewayserversettings.md)                                           | Legt die **OnlyConsentCapableClients-Eigenschaft** fest.<br/> **Windows Server 2008:** Diese Methode ist vor Windows Server 2008 R2 nicht verfügbar.<br/>                                                                                                      |
| [**EnableRequestSOH**](win32-tsgatewayserversettings-enablerequestsoh.md)                                                                         | Diese Methode wird ab Windows Server 2016 nicht unterstützt.<br/> **Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 und Windows Server 2008:** Aktiviert oder deaktiviert Anforderungen für eine Integritätsaufforderung (Statement of Health, SoH).<br/> <br/> |
| [**EnableTransport**](enabletransport-win32-tsgatewayserversettings.md)                                                                           | Aktiviert oder deaktiviert den angegebenen Transport.<br/> **Windows Server 2008 R2 und Windows Server 2008:** Diese Methode ist vor Windows Server 2012 nicht verfügbar.<br/>                                                                                  |
| [**EnumAuthenticationPlugins**](enumauthenticationplugins-win32-tsgatewayserversettings.md)                                                       | Listet alle registrierten Authentifizierungs-Plug-Ins auf.<br/> **Windows Server 2008:** Diese Methode ist nicht verfügbar.<br/>                                                                                                                                  |
| [**EnumAuthorizationPlugins**](enumauthorizationplugins-win32-tsgatewayserversettings.md)                                                         | Listet alle registrierten Autorisierungs-Plug-Ins auf.<br/> **Windows Server 2008:** Diese Methode ist vor Windows Server 2008 R2 nicht verfügbar.<br/>                                                                                                     |
| [**GetIPAndPort**](getipandport-win32-tsgatewayserversettings.md)                                                                                 | Ruft die lauschende IP-Adresse und portnummer für den angegebenen Transport ab.<br/> **Windows Server 2008 R2 und Windows Server 2008:** Diese Methode ist vor Windows Server 2012 nicht verfügbar.<br/>                                                 |
| [**GetLogEventName**](getlogeventname-win32-tsgatewayserversettings.md)                                                                           | Gibt den Protokollereignisnamen für den angegebenen Protokollereignisindex zurück.<br/>                                                                                                                                                                                         |
| [**GetProtocolName**](getprotocolname-win32-tsgatewayserversettings.md)                                                                           | Gibt den Protokollnamen für den angegebenen Protokollindex zurück.<br/>                                                                                                                                                                                           |
| [**IsLogEventEnabled**](islogeventenabled-win32-tsgatewayserversettings.md)                                                                       | Gibt an, ob der angegebene Ereignisprotokolltyp aktiviert ist.<br/>                                                                                                                                                                                            |
| [**IsTransportEnabled**](istransportenabled-win32-tsgatewayserversettings.md)                                                                     | Bestimmt, ob der angegebene Transport aktiviert ist.<br/> **Windows Server 2008 R2 und Windows Server 2008:** Diese Methode ist vor Windows Server 2012 nicht verfügbar.<br/>                                                                        |
| [**QueryCertContext**](win32-tsgatewayserversettings-querycertcontext.md)                                                                         | Gibt an, ob das angegebene Zertifikat installiert ist.<br/>                                                                                                                                                                                             |
| [**RecycleRpcApplicationPools**](recyclerpcapplicationpools-win32-tsgatewayserversettings.md)                                                     | Wiederverwendet die RPC-Anwendungspools in IIS.<br/> **Windows Server 2008:** Diese Methode ist vor Windows Server 2008 R2 nicht verfügbar.<br/>                                                                                                            |
| [**RefreshCertContext**](win32-tsgatewayserversettings-refreshcertcontext.md)                                                                     | Aktualisiert das Zertifikat, das vom RD-Gatewayserver verwendet wird.<br/>                                                                                                                                                                                      |
| [**SetAuthenticationPlugin**](setauthenticationplugin-win32-tsgatewayserversettings.md)                                                           | Legt das aktuelle Authentifizierungs-Plug-In für den RD-Gatewayserver fest.<br/> **Windows Server 2008:** Diese Methode ist vor Windows Server 2008 R2 nicht verfügbar.<br/>                                                                                    |
| [**SetAuthenticationPluginAndRecycleRpcApplicationPools**](setauthenticationpluginandrecyclerpcapplicationpools-win32-tsgatewayserversettings.md) | Legt das aktuelle Authentifizierungs-Plug-In für den RD-Gatewayserver fest und verwendet die RPC-Anwendungspools in IIS wieder.<br/> **Windows Server 2008:** Diese Methode ist vor Windows Server 2008 R2 nicht verfügbar.<br/>                                      |
| [**SetAuthorizationPlugin**](setauthorizationplugin-win32-tsgatewayserversettings.md)                                                             | Legt das aktuelle Autorisierungs-Plug-In für den RD-Gatewayserver fest.<br/> **Windows Server 2008:** Diese Methode ist vor Windows Server 2008 R2 nicht verfügbar.<br/>                                                                                     |
| [**Setcertificate**](setcertificate-win32-tsgatewayserversettings.md)                                                                             | Legt den Zertifikathash für die HTTPS-Bindung an Port 443 in IIS fest.<br/> **Windows Server 2008:** Diese Methode ist vor Windows Server 2008 R2 nicht verfügbar.<br/>                                                                                       |
| [**SetCertificateACL**](setcertificateacl-win32-tsgatewayserversettings.md)                                                                       | Legt die Zertifikatzugriffssteuerungslisten (ACLs) für diesen Server fest.<br/>                                                                                                                                                                                     |
| [**SetDefaultPluginsAndRecycleRpcApplicationPools**](setdefaultpluginsandrecyclerpcapplicationpools-win32-tsgatewayserversettings.md)             | Legt die aktuellen Authentifizierungs- und Autorisierungs-Plug-Ins für den RD-Gatewayserver fest und verwendet die RPC-Anwendungspools in IIS wieder.<br/> **Windows Server 2008:** Diese Methode ist vor Windows Server 2008 R2 nicht verfügbar.<br/>                   |
| [**SetEnforceChannelBinding**](setenforcechannelbinding-win32-tsgatewayserversettings.md)                                                         | Legt die **EnforceChannelBinding-Eigenschaft** fest.<br/> **Windows Server 2008 R2 und Windows Server 2008:** Diese Methode ist vor Windows Server 2012 nicht verfügbar.<br/>                                                                                  |
| [**SetIPAndPort**](setipandport-win32-tsgatewayserversettings.md)                                                                                 | Legt die lauschende IP-Adresse und portnummer für den angegebenen Transport fest.<br/> **Windows Server 2008 R2 und Windows Server 2008:** Diese Methode ist vor Windows Server 2012 nicht verfügbar.<br/>                                                    |
| [**SetMaxConnections**](setmaxconnections-win32-tsgatewayserversettings.md)                                                                       | Legt die maximale Anzahl zulässiger Verbindungen über das RD-Gateway fest. Diese Methode ändert die Eigenschaften **MaxConnections** und **UnlimitedConnections.**<br/>                                                                                                |
| [**SetSslBridging**](setsslbridging-win32-tsgatewayserversettings.md)                                                                             | Legt den Typ des SSL-Bridgings fest, der vom RD-Gatewayserver verwendet werden soll.<br/> **Windows Server 2008:** Diese Methode ist vor Windows Server 2008 R2 nicht verfügbar.<br/>                                                                                    |
| [**TSGRemoveAdminMsg**](tsgremoveadminmsg-win32-tsgatewayserversettings.md)                                                                       | Entfernt die Administrative Meldung für den Gatewayserver.<br/> **Windows Server 2008:** Diese Methode ist vor Windows Server 2008 R2 nicht verfügbar.<br/>                                                                                            |
| [**TSGRemoveConsentMsg**](tsgremoveconsentmsg-win32-tsgatewayserversettings.md)                                                                   | Entfernt die Administrative Meldung für den Gatewayserver.<br/> **Windows Server 2008:** Diese Methode ist vor Windows Server 2008 R2 nicht verfügbar.<br/>                                                                                            |
| [**TSGStoreAdminMsg**](tsgstoreadminmsg-win32-tsgatewayserversettings.md)                                                                         | Aktualisiert die Administrative Meldung für den Gatewayserver.<br/> **Windows Server 2008:** Diese Methode ist vor Windows Server 2008 R2 nicht verfügbar.<br/>                                                                                            |
| [**TSGStoreConsentMsg**](tsgstoreconsentmsg-win32-tsgatewayserversettings.md)                                                                     | Aktualisiert die Zustimmungsmeldung für den Gatewayserver.<br/> **Windows Server 2008:** Diese Methode ist vor Windows Server 2008 R2 nicht verfügbar.<br/>                                                                                                   |



 

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ TSGatewayServerSettings-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**adminMessageEndTime**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Endzeit der Administrativen Nachricht.

**Windows Server 2008:** Diese Eigenschaft ist vor Windows Server 2008 R2 nicht verfügbar.

</dd> <dt>

**adminMessageStartTime**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Startzeit der administrativen Nachricht.

**Windows Server 2008:** Diese Eigenschaft ist vor Windows Server 2008 R2 nicht verfügbar.

</dd> <dt>

**adminMessageText**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Text der Administrativen Nachricht.

**Windows Server 2008:** Diese Eigenschaft ist vor Windows Server 2008 R2 nicht verfügbar.

</dd> <dt>

**AuthenticationPluginCLSID**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die CLSID des aktuellen Authentifizierungs-Plug-Ins.

**Windows Server 2008:** Diese Eigenschaft ist vor Windows Server 2008 R2 nicht verfügbar.

</dd> <dt>

**AuthenticationPluginDescription**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Beschreibung des aktuellen Authentifizierungs-Plug-Ins.

**Windows Server 2008:** Diese Eigenschaft ist vor Windows Server 2008 R2 nicht verfügbar.

</dd> <dt>

**AuthenticationPluginName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name des aktuellen Authentifizierungs-Plug-Ins.

**Windows Server 2008:** Diese Eigenschaft ist vor Windows Server 2008 R2 nicht verfügbar.

</dd> <dt>

**AuthorizationPluginCLSID**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die CLSID des aktuellen Autorisierungs-Plug-Ins.

**Windows Server 2008:** Diese Eigenschaft ist vor Windows Server 2008 R2 nicht verfügbar.

</dd> <dt>

**AuthorizationPluginDescription**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Beschreibung des aktuellen Autorisierungs-Plug-Ins.

**Windows Server 2008:** Diese Eigenschaft ist vor Windows Server 2008 R2 nicht verfügbar.

</dd> <dt>

**AuthorizationPluginName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name des aktuellen Autorisierungs-Plug-Ins.

**Windows Server 2008:** Diese Eigenschaft ist vor Windows Server 2008 R2 nicht verfügbar.

</dd> <dt>

**CentralCAPEnabled**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob zentrale RD-CAP-Server zum Steuern dieses Servers verwendet werden. Diese Eigenschaft kann durch Aufrufen der [**EnableCentralCAP-Methode**](enablecentralcap-win32-tsgatewayserversettings.md) geändert werden.

</dd> <dt>

**CertHash**
</dt> <dd> <dl> <dt>

Datentyp: **uint8-Array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt den Zertifikathash für die HTTPS-Bindung an Port 443 in IIS an.

**Windows Server 2008:** Diese Eigenschaft ist vor Windows Server 2008 R2 nicht verfügbar.

</dd> <dt>

**consentMessageText**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Text der Zustimmungsnachricht.

**Windows Server 2008:** Diese Eigenschaft ist vor Windows Server 2008 R2 nicht verfügbar.

</dd> <dt>

**EnforceChannelBinding**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die Kanalbindung für den HTTP-Transport erzwungen wird. Dieser Eigenschaftswert kann mithilfe der [**SetEnforceChannelBinding-Methode**](setenforcechannelbinding-win32-tsgatewayserversettings.md) geändert werden.

**Windows Server 2008 R2 und Windows Server 2008:** Diese Eigenschaft ist vor Windows Server 2012 nicht verfügbar.

</dd> <dt>

**IsConfigured**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob iis- und RPC-Einstellungen konfiguriert sind, die vom RD-Gatewaydienst benötigt werden.

**Windows Server 2008:** Diese Eigenschaft ist vor Windows Server 2008 R2 nicht verfügbar.

</dd> <dt>

**MaxConnections**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Gibt die maximale Anzahl von Verbindungen zurück, die über das RD-Gateway zulässig sind. Diese Eigenschaft kann mithilfe der [**SetMaxConnections-Methode**](setmaxconnections-win32-tsgatewayserversettings.md) festgelegt werden.

</dd> <dt>

**MaximumAllowedConnectionsBySku**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Maximale Anzahl von Verbindungen, die die Lagerhaltungseinheit (Stock-Keeping Unit, SKU) zulässt.

</dd> <dt>

**MaxLogEvents**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt die maximale Anzahl von Protokollereignissen zurück.

</dd> <dt>

**MaxProtocols**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Anzahl der vom RD-Gateway unterstützten Protokolle.

</dd> <dt>

**OnlyConsentCapableClients**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob nur Clients, die Einwilligungsmeldungen zulassen können, eine Verbindung mit dem RD-Gateway herstellen dürfen.

**Windows Server 2008:** Diese Eigenschaft ist vor Windows Server 2008 R2 nicht verfügbar.

<dt>

Nonzero
</dt> <dd>

Nur Clients, die nachrichtenfähig sind, können eine Verbindung herstellen.

</dd> <dt>

Null
</dt> <dd>

Clients, die keine Einwilligungsmeldung unterstützen, können ebenfalls eine Verbindung herstellen.

</dd> </dl>

</dd> <dt>

**RequestSOH**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Diese Eigenschaft wird ab diesem Windows Server 2016.

**Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 und Windows Server 2008: **

Gibt an, ob der Server eine SoH (Statement of Health) vom Client anfordern muss. Diese Eigenschaft kann mithilfe der [**EnableRequestSOH-Methode geändert**](win32-tsgatewayserversettings-enablerequestsoh.md) werden.

</dd> <dt>

**SkuName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Name der SKU

</dd> <dt>

**SslBridging**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, welcher SSL-Bridgingtyp vom RD-Gatewayserver verwendet werden soll. Dies kann einer der folgenden Werte sein.

**Windows Server 2008:** Diese Eigenschaft ist vor Windows Server 2008 R2 nicht verfügbar.

<dt>

0
</dt> <dd>

Kein SSL-Bridging.

</dd> <dt>

1
</dt> <dd>

HTTPS-zu-HTTP-Bridging.

</dd> <dt>

2
</dt> <dd>

HTTPS-zu-HTTPS-Bridging.

</dd> </dl>

</dd> <dt>

**UnlimitedConnections**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob eine unbegrenzte Anzahl von Verbindungen über das RD-Gateway zulässig ist. Diese Eigenschaft kann mithilfe der [**SetMaxConnections-Methode festgelegt**](setmaxconnections-win32-tsgatewayserversettings.md) werden.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Sie müssen Mitglied der Gruppe Administratoren sein, um diese Klasse verwenden zu können.

Managed Object Format -Dateien (MOF) enthalten die Definitionen für Windows WMI-Klassen (Management Instrumentation). MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

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

[**Win32 \_ TSGatewayConnection**](win32-tsgatewayconnection.md)
</dt> <dt>

[**Win32 \_ TSGatewayConnectionAuthorizationPolicy**](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> <dt>

[**Win32 \_ TSGatewayLoadBalancer**](win32-tsgatewayloadbalancer.md)
</dt> <dt>

[**Win32 \_ TSGatewayRADIUSServer**](win32-tsgatewayradiusserver.md)
</dt> <dt>

[**Win32 \_ TSGatewayResourceAuthorizationPolicy**](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> <dt>

[**Win32 \_ TSGatewayResourceGroup**](win32-tsgatewayresourcegroup.md)
</dt> </dl>

 

