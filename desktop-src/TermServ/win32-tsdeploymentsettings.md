---
title: Win32_TSDeploymentSettings-Klasse
description: Definiert die Standardeinstellungen, die der RemoteApp-Manager beim Erstellen von Remotedesktopprotokoll (RDP)-Dateien verwendet.
ms.assetid: b3eeef86-e6cb-40ea-99f8-200c5993f31e
ms.tgt_platform: multiple
keywords:
- Win32_TSDeploymentSettings-Remotedesktopdienste
- Win32_TSDeploymentSettings klasse Remotedesktopdienste , beschrieben
topic_type:
- apiref
api_name:
- Win32_TSDeploymentSettings
- Win32_TSDeploymentSettings.Caption
- Win32_TSDeploymentSettings.Description
- Win32_TSDeploymentSettings.InstallDate
- Win32_TSDeploymentSettings.Name
- Win32_TSDeploymentSettings.Status
- Win32_TSDeploymentSettings.Port
- Win32_TSDeploymentSettings.FarmName
- Win32_TSDeploymentSettings.GatewayUsage
- Win32_TSDeploymentSettings.GatewayName
- Win32_TSDeploymentSettings.GatewayAuthMode
- Win32_TSDeploymentSettings.GatewayUseCachedCreds
- Win32_TSDeploymentSettings.RequireServerAuth
- Win32_TSDeploymentSettings.ColorBitDepth
- Win32_TSDeploymentSettings.AllowFontSmoothing
- Win32_TSDeploymentSettings.UseMultimon
- Win32_TSDeploymentSettings.RedirectionOptions
- Win32_TSDeploymentSettings.HasCertificate
- Win32_TSDeploymentSettings.CertificateHash
- Win32_TSDeploymentSettings.CertificateIssuedTo
- Win32_TSDeploymentSettings.CertificateIssuedBy
- Win32_TSDeploymentSettings.CertificateExpiresOn
- Win32_TSDeploymentSettings.CustomRDPSettings
- Win32_TSDeploymentSettings.DeploymentRDPSettings
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a3f5b5cde779cbd9b8120fa648138611236935080f3517a28a6f19dcee8864b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118349308"
---
# <a name="win32_tsdeploymentsettings-class"></a>Win32 \_ TSDeploymentSettings-Klasse

Definiert die Standardeinstellungen, die der RemoteApp-Manager beim Erstellen von Remotedesktopprotokoll (RDP)-Dateien verwendet. Diese Einstellungen wirken sich nicht auf veröffentlichte Anwendungen oder Desktops aus.

## <a name="syntax"></a>Syntax

``` syntax
class Win32_TSDeploymentSettings : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  sint32   Port;
  string   FarmName;
  sint32   GatewayUsage;
  string   GatewayName;
  sint32   GatewayAuthMode;
  boolean  GatewayUseCachedCreds;
  boolean  RequireServerAuth;
  sint32   ColorBitDepth;
  boolean  AllowFontSmoothing;
  boolean  UseMultimon;
  sint32   RedirectionOptions;
  boolean  HasCertificate;
  uint8    CertificateHash[];
  string   CertificateIssuedTo;
  string   CertificateIssuedBy;
  string   CertificateExpiresOn;
  string   CustomRDPSettings;
  string   DeploymentRDPSettings;
};
```

## <a name="members"></a>Member

Die **Win32 \_ TSDeploymentSettings-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ TSDeploymentSettings-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**AllowFontSmoothing**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob die Schriftartglättung zulässig ist.

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Kurze Beschreibung (einzeilenbasierte Zeichenfolge) des Objekts.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt.**](cim-managedsystemelement.md)

</dd> <dt>

**CertificateExpiresOn**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Das Datum, an dem das Zertifikat abläuft. Dieser Wert wird als [**64-Bit-FILETIME-Format**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) gespeichert.

</dd> <dt>

**CertificateHash**
</dt> <dd> <dl> <dt>

Datentyp: **uint8 array**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Der Fingerabdruck des Zertifikats, das zum Signieren von RDP-Dateien verwendet wird.

</dd> <dt>

**CertificateIssuedBy**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, von wem das Zertifikat ausgestellt wird.

</dd> <dt>

**CertificateIssuedTo**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, für wen das Zertifikat ausgestellt wird.

</dd> <dt>

**ColorBitDepth**
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Die Farbbittiefe der Anzeige. Mögliche Werte sind 4, 8, 15, 16, 24 und 32.

</dd> <dt>

**CustomRDPSettings**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Der Inhalt der RDP-Datei, die dem benutzerdefinierten RDP-Einstellungen in RemoteApp-Manager.

</dd> <dt>

**DeploymentRDPSettings**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Der Inhalt der RDP-Datei, die den Bereitstellungseinstellungen in RemoteApp-Manager. Wenn dieser Wert festgelegt ist, werden die Standardeinstellungen in dieser Klasse durch die RDP-Bereitstellungseinstellungen ersetzt. Wenn Sie beispielsweise die **GatewayAuthMode-Eigenschaft** in dieser Klasse und die **DeploymentRDPSettings-Eigenschaft** festlegen, wird die **GatewayAuthMode-Eigenschaft** dieser Klasse ignoriert, und der **GatewayAuthMode-Wert** aus **DeploymentRDPSettings** wird verwendet.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Beschreibung des Objekts.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt.**](cim-managedsystemelement.md)

</dd> <dt>

**FarmName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Der Name des RD-Sitzungshost Servers oder der vollqualifizierte Domänenname (Fully Qualified Domain Name, FQDN) der RD-Sitzungshost Serverfarm.

</dd> <dt>

**GatewayAuthMode**
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Die RD-Gatewayauthentifizierungsmethode. Die folgenden Werte sind möglich.

<dt>

0
</dt> <dd>

Kennwort

</dd> <dt>

1
</dt> <dd>

Smartcard

</dd> <dt>

4
</dt> <dd>

Ermöglicht dem Benutzer die Auswahl während der Verbindung.

</dd> </dl>

</dd> <dt>

**GatewayName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Der Name des zu verwendenden RD-Gatewayservers.

</dd> <dt>

**GatewayUsage**
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob ein RD-Gatewayserver verwendet werden soll, um eine Verbindung mit dem Zielserver RD-Sitzungshost firewallübergreifend herzustellen. Die folgenden Werte sind möglich.

<dt>

0
</dt> <dd>

Verwenden Sie keinen RD-Gatewayserver.

</dd> <dt>

1
</dt> <dd>

Verwenden Sie einen RD-Gatewayserver. Umgehen Sie den RD-Gatewayserver für lokale Adressen.

</dd> <dt>

2
</dt> <dd>

Verwenden Sie einen RD-Gatewayserver.

</dd> <dt>

3
</dt> <dd>

Automatisches Erkennen von RD-Gatewayservereinstellungen.

</dd> </dl>

</dd> <dt>

**GatewayUseCachedCreds**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Verwenden Sie nach Möglichkeit die gleichen Benutzeranmeldeinformationen für den RD-Gatewayserver und den RD-Sitzungshost Server.

</dd> <dt>

**HasCertificate**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob ein Zertifikat zum Signieren der RDP-Dateien verwendet werden soll.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001.5")
</dt> </dl>

Das Datum, an dem das Objekt installiert wurde. Ein fehlender Wert gibt nicht an, dass das Objekt nicht installiert ist.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt.**](cim-managedsystemelement.md)

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name des Objekts.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt.**](cim-managedsystemelement.md)

</dd> <dt>

**Port**
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Der zu verwendende RDP-Port.

</dd> <dt>

**RedirectionOptions**
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt die Geräte- und Ressourcenumleitungsoptionen für RemoteApp-Verbindungen an. Flags für **RedirectionOptions können** kombiniert werden. Die folgenden Werte sind möglich.

<dt>

0
</dt> <dd>

Keine Geräte- oder Ressourcenumleitung.

</dd> <dt>

1
</dt> <dd>

Umleiten von Laufwerken.

</dd> <dt>

2
</dt> <dd>

Umleiten von Druckern.

</dd> <dt>

4
</dt> <dd>

Leiten Sie die Zwischenablage um.

</dd> <dt>

8
</dt> <dd>

Leiten Sie unterstützte Plug & Play um.

</dd> <dt>

16
</dt> <dd>

Umleiten von Smartcards.

</dd> <dt>

32
</dt> <dd>

Umleiten von Audio.

</dd> <dt>

64
</dt> <dd>

Serielle Anschlüsse umleiten.

</dd> </dl>

</dd> <dt>

**RequireServerAuth**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob eine Serverauthentifizierung erforderlich ist.

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)
</dt> </dl>

Aktueller Status des Objekts. Es können verschiedene betriebsbereite und nicht betriebsbereite Status definiert werden. Folgende Betriebsstatus sind möglich: "OK", "Heruntergestuft" und "Fehler vor dem Ausfall" (ein Element, z. B. ein SMART-fähiges Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber es wird in naher Zukunft ein Fehler vorhergesagt). Nicht operative Status sind: "Error", "Starting", "Stopping" und "Service". Letzteres, "Dienst", kann während der Spiegelung eines Datenträgers, beim erneuten Laden einer Benutzerberechtigungsliste oder bei anderen administrativen Aufgaben angewendet werden. Nicht alle diese Arbeiten sind online, aber das verwaltete Element befindet sich weder in "OK" noch in einem der anderen Zustände.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt.**](cim-managedsystemelement.md)

<dt>



 ("OK")


</dt> <dd></dd> <dt>



 ("Fehler")


</dt> <dd></dd> <dt>



 ("Heruntergestuft")


</dt> <dd></dd> <dt>



 ("Unbekannt")


</dt> <dd></dd> <dt>



 ("Pred Fail")


</dt> <dd></dd> <dt>



 ("Wird gestartet")


</dt> <dd></dd> <dt>



 ("Wird beendet")


</dt> <dd></dd> <dt>



 ("Dienst")


</dt> <dd></dd> </dl>

</dd> <dt>

**UseMultimon**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob mehrere Monitore für den Desktop aktiviert sind.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Sie müssen Mitglied der Gruppe Administratoren sein, um Eigenschaften mithilfe dieser Klasse festlegen zu können.

Wenn **RequireServerAuth** auf TRUE festgelegt **ist,** sollten Sie Folgendes berücksichtigen:

-   Wenn das RemoteApp-Programm für die Intranetnutzung verwendet wird und auf allen Clientcomputern entweder Windows Server 2008 oder Windows Vista ausgeführt wird, müssen Sie den RD-Sitzungshost-Server nicht für die Verwendung eines SSL-Zertifikats konfigurieren. In diesem Fall wird Authentifizierung auf Netzwerkebene verwendet.
-   Sie müssen den FQDN des Servers oder der Farm für den Wert der **FarmName-Eigenschaft** angeben.

Um eine Verbindung mit dem Namespace "CIMV2 \\ TerminalServices" herzustellen, muss die Authentifizierungsebene den Paketschutz enthalten. Bei C/C++-Aufrufen ist dies eine Authentifizierungsebene von **RPC \_ C \_ AUTHN \_ LEVEL \_ PKT \_ PRIVACY,** die mithilfe der [**COM-Funktion CoSetProxyBlanket festgelegt**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) werden kann. Für Visual Basic- und Skriptaufrufe ist dies eine Authentifizierungsebene von **WbemAuthenticationLevelPktPrivacy** oder "pktPrivacy" mit dem Wert 6. Das folgende Visual Basic Scripting Edition (VBScript) zeigt, wie Sie eine Verbindung mit einem Remotecomputer mit Paketschutz herstellen.


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



Managed Object Format -Dateien (MOF) enthalten die Definitionen für Windows WMI-Klassen (Management Instrumentation). Sie werden auf dem Computer installiert, wenn Sie die zugeordnete Rolle hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\ \\ CiMv2-Stammterminaldienste<br/>                                                |
| MOF<br/>                      | <dl> <dt>Tsallow.mof</dt> </dl>  |
| DLL<br/>                      | <dl> <dt>TsPubWmi.dll</dt> </dl> |



 

