---
title: Win32_TSDeploymentSettings-Klasse
description: Definiert die Standardeinstellungen, die der RemoteApp-Manager verwendet, wenn Remotedesktopprotokoll (RDP)-Dateien erstellt werden.
ms.assetid: b3eeef86-e6cb-40ea-99f8-200c5993f31e
ms.tgt_platform: multiple
keywords:
- Win32_TSDeploymentSettings-Klasse Remotedesktopdienste
- Win32_TSDeploymentSettings Klasse Remotedesktopdienste, beschrieben
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
ms.openlocfilehash: 0f254363968099ab73c5f3f14f1f15ab8554f62a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476392"
---
# <a name="win32_tsdeploymentsettings-class"></a>Win32-Klasse "t \_ deploymentsettings"

Definiert die Standardeinstellungen, die der RemoteApp-Manager verwendet, wenn Remotedesktopprotokoll (RDP)-Dateien erstellt werden. Diese Einstellungen wirken sich nicht auf veröffentlichte Anwendungen oder Desktops aus.

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

Die Win32-Klasse " **\_ zdeploymentsettings** " verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die Win32-Klasse "t- **\_ deploymentsettings** " verfügt über diese Eigenschaften.

<dl> <dt>

**Allowfonsitzmoothing**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob die Schriftart Glättung zulässig ist.

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Kurze Beschreibung (einzeilige Zeichenfolge) des-Objekts.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**Certificateexpireson**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Das Datum, an dem das Zertifikat abläuft. Dieser Wert wird als 64-Bit- [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) -Format gespeichert.

</dd> <dt>

**CertificateHash**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8** Array
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Der Fingerabdruck des Zertifikats, das zum Signieren von RDP-Dateien verwendet wird.

</dd> <dt>

**Certifi-eissuedby**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, von wem das Zertifikat ausgestellt wird.

</dd> <dt>

**Certifi-eissuedto**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, für wen das Zertifikat ausgestellt wird.

</dd> <dt>

**Colorbittiefe**
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Die farbbit Tiefe der Anzeige. Mögliche Werte sind 4, 8, 15, 16, 24 und 32.

</dd> <dt>

**Customrdpsettings**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Der Inhalt der RDP-Datei, die den benutzerdefinierten RDP-Einstellungen in RemoteApp-Manager entspricht.

</dd> <dt>

**Bereitstellerentrdpsettings**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Der Inhalt der RDP-Datei, die den Bereitstellungs Einstellungen in RemoteApp-Manager entspricht. Wenn dieser Wert festgelegt ist, ersetzen die RDP-Bereitstellungs Einstellungen die Standardeinstellungen in dieser Klasse. Wenn Sie z. b. die **gatewayauthmode** -Eigenschaft in dieser Klasse festlegen und die **bereitstellerentrdpsettings** -Eigenschaft festlegen, wird die **gatewayauthmode** -Eigenschaft dieser Klasse ignoriert, und der **gatewayauthmode** -Wert aus der bereitstellerentrdpsettings wird verwendet. 

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Beschreibung des Objekts.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**Farmname**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Der Name des RD-Sitzungshost Servers oder der voll qualifizierte Domänen Name (Fully Qualified Domain Name, FQDN) der RD-Sitzungshost Serverfarm.

</dd> <dt>

**Gatewayauthmode**
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Die RD-Gateway Authentifizierungsmethode. Die folgenden Werte sind möglich.

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

Ermöglicht es Benutzern, während der Verbindung auszuwählen.

</dd> </dl>

</dd> <dt>

**Gatewayname**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Der Name des zu verwendenden RD-Gateway Servers.

</dd> <dt>

**Gatewayusage**
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob ein RD-Gateway Server verwendet werden soll, um eine Verbindung mit dem Ziel RD-Sitzungshost Server über eine Firewall herzustellen. Die folgenden Werte sind möglich.

<dt>

0
</dt> <dd>

Verwenden Sie keinen RD-Gateway Server.

</dd> <dt>

1
</dt> <dd>

Verwenden Sie einen RD-Gateway Server. Umgehen Sie den RD-Gateway Server für lokale Adressen.

</dd> <dt>

2
</dt> <dd>

Verwenden Sie einen RD-Gateway Server.

</dd> <dt>

3
</dt> <dd>

RD-Gateway Servereinstellungen automatisch erkennen.

</dd> </dl>

</dd> <dt>

**Gatewayusecachedkreds**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Verwenden Sie nach Möglichkeit die gleichen Benutzer Anmelde Informationen für den RD-Gateway Server und den RD-Sitzungshost Server.

</dd> <dt>

**Hascertificate**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob ein Zertifikat zum Signieren der RDP-Dateien verwendet werden soll.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 ")
</dt> </dl>

Das Datum, an dem das Objekt installiert wurde. Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name des Objekts.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**Port**
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Der zu verwendende RDP-Port.

</dd> <dt>

**Redirectionoptions**
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt die Optionen für die Geräte-und Ressourcen Umleitung für RemoteApp-Verbindungen an. Flags für **redirectionoptions** können kombiniert werden. Die folgenden Werte sind möglich.

<dt>

0
</dt> <dd>

Keine Geräte-oder Ressourcen Umleitung.

</dd> <dt>

1
</dt> <dd>

Umleiten von Laufwerken

</dd> <dt>

2
</dt> <dd>

Umleiten von Druckern

</dd> <dt>

4
</dt> <dd>

Umleiten der Zwischenablage.

</dd> <dt>

8
</dt> <dd>

Umleitung Plug & Play Geräten unterstützt.

</dd> <dt>

16
</dt> <dd>

Umleiten von Smartcards.

</dd> <dt>

32
</dt> <dd>

Umleiten von Audiodaten

</dd> <dt>

64
</dt> <dd>

Serielle Ports umleiten.

</dd> </dl>

</dd> <dt>

**Requirements serverauth**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob die Server Authentifizierung erforderlich ist.

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)
</dt> </dl>

Aktueller Status des Objekts. Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden. Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail" (ein Element, z. b. ein Smart-aktiviertes Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber in naher Zukunft einen Fehler vorherzusagen). Nicht betriebsbereite Status umfassen: "Error", "Starting", "Stop" und "Service". Der letztgenannte "Dienst" kann während der Spiegelung eines Datenträgers, dem erneuten Laden einer Benutzer Berechtigungs Liste oder anderer administrativer Aufgaben angewendet werden. Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

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

**Usemultimon**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob mehrere Monitore für den Desktop aktiviert sind.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Sie müssen Mitglied der Gruppe "Administratoren" sein, um Eigenschaften mithilfe dieser Klasse festzulegen.

Wenn "Requirements **serverauth** " auf " **true**" festgelegt ist, sollten Sie Folgendes beachten:

-   Wenn das RemoteApp-Programm für die Intranetverwendung vorgesehen ist und auf allen Client Computern entweder Windows Server 2008 oder Windows Vista ausgeführt wird, müssen Sie den RD-Sitzungshost Server nicht für die Verwendung eines SSL-Zertifikats konfigurieren. In diesem Fall wird Authentifizierung auf Netzwerkebene verwendet.
-   Sie müssen den voll qualifizierten Namen des Servers oder der Farm für den Wert der **Farmname** -Eigenschaft angeben.

Zum Herstellen einer Verbindung mit dem \\ Namespace "CIMV2 TerminalServices" muss die Authentifizierungs Ebene den Datenschutz für das Paket enthalten. Bei C/C++-aufrufen handelt es sich hierbei um eine Authentifizierungs Ebene für den **\_ \_ \_ \_ Pkt- \_ Datenschutz auf RPC-C-Ebene**, die mithilfe der com-Funktion [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) festgelegt werden kann. Bei Visual Basic-und Skript aufrufen handelt es sich hierbei um eine Authentifizierungs Ebene von **wbemauthenticationlevelpzprivacy** oder "PKTPRIVACY" mit einem Wert von 6. Im folgenden Visual Basic Scripting Edition (VBScript)-Beispiel wird gezeigt, wie eine Verbindung mit einem Remote Computer mit Paket Datenschutz hergestellt wird.


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen. Sie werden auf dem Computer installiert, wenn Sie die zugehörige Rolle hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>Tsallow. MOF</dt> </dl>  |
| DLL<br/>                      | <dl> <dt>TsPubWmi.dll</dt> </dl> |



 

