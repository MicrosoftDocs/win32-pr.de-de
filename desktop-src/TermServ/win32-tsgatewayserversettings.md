---
title: Win32_TSGatewayServerSettings-Klasse
description: Stellt Methoden und Eigenschaften zum Anzeigen und Konfigurieren von Remotedesktop Gateway-Servereinstellungen (RD-Gateway) bereit.
ms.assetid: f772bf71-68ef-4345-8123-f6ad50ee4d61
ms.tgt_platform: multiple
keywords:
- Win32_TSGatewayServerSettings-Klasse Remotedesktopdienste
- Win32_TSGatewayServerSettings Klasse Remotedesktopdienste, beschrieben
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
ms.openlocfilehash: 0c0fb9b93f75c47760da8778e4aef8bed7f4e022
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478813"
---
# <a name="win32_tsgatewayserversettings-class"></a>Win32-Klasse "t- \_ gatewayserversettings"

Stellt Methoden und Eigenschaften zum Anzeigen und Konfigurieren von Remotedesktop Gateway-Servereinstellungen (RD-Gateway) bereit. Administratoren können diese Klasse verwenden, um einen Satz von Protokollen, den Satz von Ereignissen, die in das Ereignisprotokoll geschrieben werden, und die maximale Anzahl von Verbindungen durch RD-Gateway zu konfigurieren.

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

Die Win32-Klasse "t- **\_ gatewayserversettings** " verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die Win32-Klasse "t- **\_ gatewayserversettings** " verfügt über diese Methoden.



| Methode                                                                                                                                             | BESCHREIBUNG                                                                                                                                                                                                                                                      |
|:---------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Konfigurieren**](configure-win32-tsgatewayserversettings.md)                                                                                       | Konfiguriert die IIS-und RPC-Einstellungen, die für den RD-Gateway-Dienst erforderlich sind.<br/> **Windows Server 2008:** Diese Methode ist vor Windows Server 2008 R2 nicht verfügbar.<br/>                                                                               |
| [**Enablecentralcap**](enablecentralcap-win32-tsgatewayserversettings.md)                                                                         | Aktiviert oder deaktiviert die **centralcapused** -Eigenschaft, mit der gesteuert wird, ob Zentrale Remotedesktop Verbindungs Autorisierungs Richtlinien-Server (RD-CAP) zum Steuern von Verbindungs Autorisierungs Richtlinien für diesen Server verwendet werden.<br/>                    |
| [**Enablelogevent**](enablelogevent-win32-tsgatewayserversettings.md)                                                                             | Aktiviert oder deaktiviert die Protokollierung des angegebenen Ereignis Typs.<br/>                                                                                                                                                                                              |
| [**Enableonlygenehmicapableclients**](enableonlyconsentcapableclients-win32-tsgatewayserversettings.md)                                           | Legt die **onlygenehmicapableclients** -Eigenschaft fest.<br/> **Windows Server 2008:** Diese Methode ist vor Windows Server 2008 R2 nicht verfügbar.<br/>                                                                                                      |
| [**Enablerequestsoh**](win32-tsgatewayserversettings-enablerequestsoh.md)                                                                         | Diese Methode wird ab Windows Server 2016 nicht unterstützt.<br/> **Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 und Windows Server 2008:** Aktiviert oder deaktiviert Anforderungen für ein Statement of Health (SoH).<br/> <br/> |
| [**Enabletransport**](enabletransport-win32-tsgatewayserversettings.md)                                                                           | Aktiviert oder deaktiviert den angegebenen Transport.<br/> **Windows Server 2008 R2 und Windows Server 2008:** Diese Methode ist vor Windows Server 2012 nicht verfügbar.<br/>                                                                                  |
| [**Enumauthenticationplugins**](enumauthenticationplugins-win32-tsgatewayserversettings.md)                                                       | Listet alle registrierten Authentifizierungs-Plug-Ins auf.<br/> **Windows Server 2008:** Diese Methode ist nicht verfügbar.<br/>                                                                                                                                  |
| [**Enumauthorizationplugins**](enumauthorizationplugins-win32-tsgatewayserversettings.md)                                                         | Listet alle registrierten Autorisierungs-Plug-Ins auf.<br/> **Windows Server 2008:** Diese Methode ist vor Windows Server 2008 R2 nicht verfügbar.<br/>                                                                                                     |
| [**Getipandport**](getipandport-win32-tsgatewayserversettings.md)                                                                                 | Ruft die Abhör-IP-Adresse und die Portnummer für den angegebenen Transport ab.<br/> **Windows Server 2008 R2 und Windows Server 2008:** Diese Methode ist vor Windows Server 2012 nicht verfügbar.<br/>                                                 |
| [**Getlogeventname**](getlogeventname-win32-tsgatewayserversettings.md)                                                                           | Gibt den Protokoll Ereignis Namen für den angegebenen Protokoll Ereignis Index zurück.<br/>                                                                                                                                                                                         |
| [**Getprotocolname**](getprotocolname-win32-tsgatewayserversettings.md)                                                                           | Gibt den Protokollnamen für den angegebenen Protokoll Index zurück.<br/>                                                                                                                                                                                           |
| [**Islogeventaktivierte**](islogeventenabled-win32-tsgatewayserversettings.md)                                                                       | Gibt an, ob der angegebene Ereignis protokolllistyp aktiviert ist.<br/>                                                                                                                                                                                            |
| [**Istransportenabled**](istransportenabled-win32-tsgatewayserversettings.md)                                                                     | Bestimmt, ob der angegebene Transport aktiviert ist.<br/> **Windows Server 2008 R2 und Windows Server 2008:** Diese Methode ist vor Windows Server 2012 nicht verfügbar.<br/>                                                                        |
| [**Querycertcontext**](win32-tsgatewayserversettings-querycertcontext.md)                                                                         | Gibt an, ob das angegebene Zertifikat installiert ist.<br/>                                                                                                                                                                                             |
| [**Recyclerpcapplicationpools**](recyclerpcapplicationpools-win32-tsgatewayserversettings.md)                                                     | Wiederverwendungen der RPC-Anwendungs Pools in IIS.<br/> **Windows Server 2008:** Diese Methode ist vor Windows Server 2008 R2 nicht verfügbar.<br/>                                                                                                            |
| [**Aktualisierbaren Kontext**](win32-tsgatewayserversettings-refreshcertcontext.md)                                                                     | Aktualisiert das Zertifikat, das vom RD-Gateway-Server verwendet wird.<br/>                                                                                                                                                                                      |
| [**Setauthenticationplugin**](setauthenticationplugin-win32-tsgatewayserversettings.md)                                                           | Legt das aktuelle Authentifizierungs-Plug-in für den RD-Gateway Server fest.<br/> **Windows Server 2008:** Diese Methode ist vor Windows Server 2008 R2 nicht verfügbar.<br/>                                                                                    |
| [**Setauthenticationpluginandrecyclerpcapplicationpools**](setauthenticationpluginandrecyclerpcapplicationpools-win32-tsgatewayserversettings.md) | Legt das aktuelle Authentifizierungs-Plug-in für den RD-Gateway Server fest und wieder verwendet die RPC-Anwendungs Pools in IIS.<br/> **Windows Server 2008:** Diese Methode ist vor Windows Server 2008 R2 nicht verfügbar.<br/>                                      |
| [**Setauthorizationplugin**](setauthorizationplugin-win32-tsgatewayserversettings.md)                                                             | Legt das aktuelle Autorisierungs-Plug-in für den RD-Gateway Server fest.<br/> **Windows Server 2008:** Diese Methode ist vor Windows Server 2008 R2 nicht verfügbar.<br/>                                                                                     |
| [**SetCertificate**](setcertificate-win32-tsgatewayserversettings.md)                                                                             | Legt den Zertifikat Hash für die HTTPS-Bindung an Port 443 in IIS fest.<br/> **Windows Server 2008:** Diese Methode ist vor Windows Server 2008 R2 nicht verfügbar.<br/>                                                                                       |
| [**Setcertificateacl**](setcertificateacl-win32-tsgatewayserversettings.md)                                                                       | Legt die Zertifikat-Zugriffs Steuerungs Listen (ACLs) für diesen Server fest.<br/>                                                                                                                                                                                     |
| [**Setdefaultpluginsandrecyclerpcapplicationpools**](setdefaultpluginsandrecyclerpcapplicationpools-win32-tsgatewayserversettings.md)             | Legt die aktuellen Authentifizierungs-und Autorisierungs-Plug-Ins für den RD-Gateway Server fest und wieder verwendet die RPC-Anwendungs Pools in IIS.<br/> **Windows Server 2008:** Diese Methode ist vor Windows Server 2008 R2 nicht verfügbar.<br/>                   |
| [**"Tenforcechannelbinding"**](setenforcechannelbinding-win32-tsgatewayserversettings.md)                                                         | Legt die **enforcechannelbinding** -Eigenschaft fest.<br/> **Windows Server 2008 R2 und Windows Server 2008:** Diese Methode ist vor Windows Server 2012 nicht verfügbar.<br/>                                                                                  |
| [**"Seetipandport"**](setipandport-win32-tsgatewayserversettings.md)                                                                                 | Legt die Abhör-IP-Adresse und die Portnummer für den angegebenen Transport fest.<br/> **Windows Server 2008 R2 und Windows Server 2008:** Diese Methode ist vor Windows Server 2012 nicht verfügbar.<br/>                                                    |
| [**Setmaxconnections**](setmaxconnections-win32-tsgatewayserversettings.md)                                                                       | Legt die maximale Anzahl zulässiger Verbindungen über RD-Gateway fest. Mit dieser Methode werden die Eigenschaften " **MaxConnections** " und " **UnlimitedConnections** " geändert.<br/>                                                                                                |
| [**Setsslbridging**](setsslbridging-win32-tsgatewayserversettings.md)                                                                             | Legt den Typ des SSL-Bridging fest, der vom RD-Gateway Server verwendet werden soll.<br/> **Windows Server 2008:** Diese Methode ist vor Windows Server 2008 R2 nicht verfügbar.<br/>                                                                                    |
| [**"T"**](tsgremoveadminmsg-win32-tsgatewayserversettings.md)                                                                       | Entfernt die administrative Meldung für den Gatewayserver.<br/> **Windows Server 2008:** Diese Methode ist vor Windows Server 2008 R2 nicht verfügbar.<br/>                                                                                            |
| [**"T"**](tsgremoveconsentmsg-win32-tsgatewayserversettings.md)                                                                   | Entfernt die administrative Meldung für den Gatewayserver.<br/> **Windows Server 2008:** Diese Methode ist vor Windows Server 2008 R2 nicht verfügbar.<br/>                                                                                            |
| [**"GS storeadminmsg"**](tsgstoreadminmsg-win32-tsgatewayserversettings.md)                                                                         | Aktualisiert die administrative Meldung für den Gatewayserver.<br/> **Windows Server 2008:** Diese Methode ist vor Windows Server 2008 R2 nicht verfügbar.<br/>                                                                                            |
| [**"GS-storeconsentmsg"**](tsgstoreconsentmsg-win32-tsgatewayserversettings.md)                                                                     | Aktualisiert die Zustimmungs Nachricht für den Gatewayserver.<br/> **Windows Server 2008:** Diese Methode ist vor Windows Server 2008 R2 nicht verfügbar.<br/>                                                                                                   |



 

### <a name="properties"></a>Eigenschaften

Die Win32-Klasse "t- **\_ gatewayserversettings** " verfügt über diese Eigenschaften.

<dl> <dt>

**adminmessageendtime**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Endzeit der administrativen Nachricht.

**Windows Server 2008:** Diese Eigenschaft ist vor Windows Server 2008 R2 nicht verfügbar.

</dd> <dt>

**adminmessagestarttime**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Startzeit der administrativen Nachricht.

**Windows Server 2008:** Diese Eigenschaft ist vor Windows Server 2008 R2 nicht verfügbar.

</dd> <dt>

**adminmessagetext**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Text der administrativen Nachricht.

**Windows Server 2008:** Diese Eigenschaft ist vor Windows Server 2008 R2 nicht verfügbar.

</dd> <dt>

**Authenticationpluginclsid**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die CLSID des aktuellen Authentifizierungs-Plug-ins.

**Windows Server 2008:** Diese Eigenschaft ist vor Windows Server 2008 R2 nicht verfügbar.

</dd> <dt>

**Authenticationplugindescription**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Beschreibung des aktuellen Authentifizierungs-Plug-ins.

**Windows Server 2008:** Diese Eigenschaft ist vor Windows Server 2008 R2 nicht verfügbar.

</dd> <dt>

**Authenticationpluginname**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name des aktuellen Authentifizierungs-Plug-ins.

**Windows Server 2008:** Diese Eigenschaft ist vor Windows Server 2008 R2 nicht verfügbar.

</dd> <dt>

**Authorizationpluginclsid**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die CLSID des aktuellen Autorisierungs-Plug-ins.

**Windows Server 2008:** Diese Eigenschaft ist vor Windows Server 2008 R2 nicht verfügbar.

</dd> <dt>

**Authorizationplugindescription**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Beschreibung des aktuellen Autorisierungs-Plug-ins.

**Windows Server 2008:** Diese Eigenschaft ist vor Windows Server 2008 R2 nicht verfügbar.

</dd> <dt>

**Authorizationpluginname**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name des aktuellen Autorisierungs-Plug-ins.

**Windows Server 2008:** Diese Eigenschaft ist vor Windows Server 2008 R2 nicht verfügbar.

</dd> <dt>

**Centralcapaktivierte**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob zentrale RD-CAP-Server zum Steuern dieses Servers verwendet werden. Diese Eigenschaft kann durch Aufrufen der [**enablecentralcap**](enablecentralcap-win32-tsgatewayserversettings.md) -Methode geändert werden.

</dd> <dt>

**CertHash**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt den Zertifikat Hash für die HTTPS-Bindung an Port 443 in IIS an.

**Windows Server 2008:** Diese Eigenschaft ist vor Windows Server 2008 R2 nicht verfügbar.

</dd> <dt>

**genehmimessagetext**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Zustimmungs Meldungs Text.

**Windows Server 2008:** Diese Eigenschaft ist vor Windows Server 2008 R2 nicht verfügbar.

</dd> <dt>

**Enforcechannelbinding**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die kanalbindung für den HTTP-Transport erzwungen wird. Dieser Eigenschafts Wert kann mithilfe der Methode " [**settenforcechannelbinding**](setenforcechannelbinding-win32-tsgatewayserversettings.md) " geändert werden.

**Windows Server 2008 R2 und Windows Server 2008:** Diese Eigenschaft ist vor Windows Server 2012 nicht verfügbar.

</dd> <dt>

**IsConfigured**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die für den RD-Gateway Dienst erforderlichen IIS-und RPC-Einstellungen konfiguriert sind.

**Windows Server 2008:** Diese Eigenschaft ist vor Windows Server 2008 R2 nicht verfügbar.

</dd> <dt>

**MaxConnections**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Gibt die maximale Anzahl von Verbindungen zurück, die durch RD-Gateway zugelassen werden. Diese Eigenschaft kann mit der [**setmaxconnections**](setmaxconnections-win32-tsgatewayserversettings.md) -Methode festgelegt werden.

</dd> <dt>

**Maximumallowedconnectionsbysku**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Maximale Anzahl von Verbindungen, die die Stock Keeping Unit (SKU) zulässt.

</dd> <dt>

**Maxlogevents**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt die maximale Anzahl von Protokoll Ereignissen zurück.

</dd> <dt>

**Maxprotokolle**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Anzahl von Protokollen, die von RD-Gateway unterstützt werden.

</dd> <dt>

**Onlygenehmicapableclients**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob nur Clients, die Nachrichten unterstützen können, eine Verbindung mit dem RD-Gateway herstellen dürfen.

**Windows Server 2008:** Diese Eigenschaft ist vor Windows Server 2008 R2 nicht verfügbar.

<dt>

ungleich NULL
</dt> <dd>

Nur Genehmigungs Nachrichten fähige Clients können eine Verbindung herstellen.

</dd> <dt>

Null
</dt> <dd>

Clients, die keine Zustimmungs Nachrichten fähig sind, können auch eine Verbindung herstellen.

</dd> </dl>

</dd> <dt>

**Requestsoh**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Diese Eigenschaft wird ab Windows Server 2016 nicht unterstützt.

* * Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 und Windows Server 2008: * *

Gibt an, ob der Server ein Statement of Health (SoH) vom Client anfordern muss. Diese Eigenschaft kann mithilfe der [**enablerequestsoh**](win32-tsgatewayserversettings-enablerequestsoh.md) -Methode geändert werden.

</dd> <dt>

**SkuName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Name der SKU

</dd> <dt>

**Sslbridging**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, welcher Typ von SSL-Bridging vom RD-Gateway Server verwendet werden soll. Dies kann einer der folgenden Werte sein:

**Windows Server 2008:** Diese Eigenschaft ist vor Windows Server 2008 R2 nicht verfügbar.

<dt>

0
</dt> <dd>

Keine SSL-Überbrückung.

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

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob eine unbegrenzte Anzahl von Verbindungen durch RD-Gateway zulässig ist. Diese Eigenschaft kann mit der [**setmaxconnections**](setmaxconnections-win32-tsgatewayserversettings.md) -Methode festgelegt werden.

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

[**Win32- \_ faigatewayconnectionauthorizationpolicy**](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> <dt>

[**Win32-"t- \_ gatewayloadbalancer"**](win32-tsgatewayloadbalancer.md)
</dt> <dt>

[**Win32-"t- \_ gatewayradiusserver"**](win32-tsgatewayradiusserver.md)
</dt> <dt>

[**Win32- \_ faigatewayresourceauthorizationpolicy**](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> <dt>

[**Win32-Datei " \_ zgatewayresourcegroup"**](win32-tsgatewayresourcegroup.md)
</dt> </dl>

 

