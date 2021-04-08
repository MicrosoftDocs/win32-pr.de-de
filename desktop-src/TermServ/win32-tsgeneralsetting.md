---
title: Win32_TSGeneralSetting-Klasse
description: Stellt allgemeine Einstellungen des Terminals dar, z. b. die Verschlüsselungs Stufe und das Transportprotokoll.
ms.assetid: a31d68c0-e446-4d78-85e0-5173e7870255
ms.tgt_platform: multiple
keywords:
- Win32_TSGeneralSetting-Klasse Remotedesktopdienste
- Win32_TSGeneralSetting Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_TSGeneralSetting
- Win32_TSGeneralSetting.Caption
- Win32_TSGeneralSetting.Description
- Win32_TSGeneralSetting.InstallDate
- Win32_TSGeneralSetting.Name
- Win32_TSGeneralSetting.Status
- Win32_TSGeneralSetting.TerminalName
- Win32_TSGeneralSetting.CertificateName
- Win32_TSGeneralSetting.Certificates
- Win32_TSGeneralSetting.Comment
- Win32_TSGeneralSetting.MinEncryptionLevel
- Win32_TSGeneralSetting.PolicySourceMinEncryptionLevel
- Win32_TSGeneralSetting.PolicySourceSecurityLayer
- Win32_TSGeneralSetting.PolicySourceUserAuthenticationRequired
- Win32_TSGeneralSetting.SecurityLayer
- Win32_TSGeneralSetting.SSLCertificateSHA1Hash
- Win32_TSGeneralSetting.SSLCertificateSHA1HashType
- Win32_TSGeneralSetting.TerminalProtocol
- Win32_TSGeneralSetting.Transport
- Win32_TSGeneralSetting.UserAuthenticationRequired
- Win32_TSGeneralSetting.WindowsAuthentication
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 172f18bbddd364d74dfcfb00e7e665628267af36
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741776"
---
# <a name="win32_tsgeneralsetting-class"></a>Win32-Klasse "t \_ General setting"

Die **Win32 \_ tgeneralsetting** -WMI-Klasse stellt allgemeine Einstellungen des Terminals dar, z. b. die Verschlüsselungs Stufe und das Transportprotokoll.

Die folgende Syntax wird aus dem MOF-Code vereinfacht und umfasst alle definierten und geerbten Eigenschaften in alphabetischer Reihenfolge. Referenzinformationen zu-Methoden finden Sie in der Tabelle mit den Methoden weiter unten in diesem Thema.

## <a name="syntax"></a>Syntax

``` syntax
[dynamic, provider("Win32_WIN32_TSGENERALSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_TSGeneralSetting : Win32_TerminalSetting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
  string   CertificateName;
  uint8    Certificates[];
  string   Comment;
  uint32   MinEncryptionLevel;
  uint32   PolicySourceMinEncryptionLevel;
  uint32   PolicySourceSecurityLayer;
  uint32   PolicySourceUserAuthenticationRequired;
  uint32   SecurityLayer;
  string   SSLCertificateSHA1Hash;
  uint32   SSLCertificateSHA1HashType;
  string   TerminalProtocol;
  string   Transport;
  uint32   UserAuthenticationRequired;
  uint32   WindowsAuthentication;
};
```

## <a name="members"></a>Member

Die Win32-Klasse " **\_ zgeneralsetting** " verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die Win32-Klasse " **\_ zgeneralsetting** " verfügt über diese Methoden.



| Methode                                                                                        | BESCHREIBUNG                                                                                                                                                             |
|:----------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Setencryptionlevel**](win32-tsgeneralsetting-setencryptionlevel.md)                       | Legt die Verschlüsselungs Stufe fest.<br/>                                                                                                                                   |
| [**Setsecuritylayer**](win32-tsgeneralsetting-setsecuritylayer.md)                           | Legt die Sicherheitsstufe auf "RDP Security Layer" (0), "aushandeln" (1) oder "SSL" (2) fest.<br/>                                                                   |
| [**Setuserauthenticationrequired**](setuserauthenticationrequired-win32-tsgeneralsetting.md) | Aktiviert oder deaktiviert die Anforderung, dass Benutzer zur Verbindungszeit authentifiziert werden müssen, indem der Wert der **UserAuthenticationRequired** -Eigenschaft festgelegt wird.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die Win32-Klasse "t- **\_ generalsetting** " verfügt über diese Eigenschaften.

<dl> <dt>

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

**CertificateName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Anzeige Name für den Antragsteller Namen des persönlichen Zertifikats für den lokalen Computer.

</dd> <dt>

**Zertifikate**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Enthält einen serialisierten Zertifikat Speicher, der alle Zertifikate aus dem **eigenen Benutzerkonten** Speicher auf dem Computer enthält, bei denen es sich um gültige Server Zertifikate für die Verwendung mit SSL (Secure Sockets Layer) handelt.

</dd> <dt>

**Kommentar**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Beschreibender Name der Kombination aus Sitzungsschicht und Transportprotokoll.

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

**Minverschlüsselungslevel**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **niedrig** ("nur Daten, die vom Client an den Server gesendet werden, werden durch Verschlüsselung basierend auf der Standardschlüssel Stärke des Servers geschützt. Die vom Server an den Client gesendeten Daten sind nicht geschützt. "), **Mittel** (" alle Daten, die zwischen dem Server und dem Client gesendet werden, werden durch Verschlüsselung basierend auf der Standardschlüssel Stärke des Servers geschützt. "), **hoch** (" alle Daten, die zwischen Server und Client gesendet werden, werden durch die Verschlüsselungs basierte maximale Schlüssel Stärke von onServer geschützt. ")
</dt> </dl>

Die minimale Verschlüsselungs Stufe.

<dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>**Niedrig** (1)


</dt> <dd>

Niedriger Verschlüsselungs Grad. Nur vom Client an den Server gesendete Daten werden mithilfe der 56-Bit-Verschlüsselung verschlüsselt. Beachten Sie, dass die vom Server an den Client gesendeten Daten nicht verschlüsselt sind.

</dd> <dt>

<span id="Medium___Client_Compatible"></span><span id="medium___client_compatible"></span><span id="MEDIUM___CLIENT_COMPATIBLE"></span>

<span id="Medium___Client_Compatible"></span><span id="medium___client_compatible"></span><span id="MEDIUM___CLIENT_COMPATIBLE"></span>**Mittel/Client kompatibel** (2)


</dt> <dd>

Client kompatibler Verschlüsselungs Grad. Alle Daten, die vom Client an den Server und vom Server an den Client gesendet werden, werden mit der maximalen Schlüssel Stärke verschlüsselt, die vom Client unterstützt wird.

</dd> <dt>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>**Hoch** (3)


</dt> <dd>

Hohes Maß an Verschlüsselung. Alle Daten, die vom Client an den Server und vom Server an den Client gesendet werden, werden mit starker 128-Bit-Verschlüsselung verschlüsselt. Clients, die diese Verschlüsselungs Stufe nicht unterstützen, können keine Verbindung herstellen.

</dd> <dt>

<span id="FIPS_Compliant"></span><span id="fips_compliant"></span><span id="FIPS_COMPLIANT"></span>

<span id="FIPS_Compliant"></span><span id="fips_compliant"></span><span id="FIPS_COMPLIANT"></span>**Kompatibel** mit der Konformität (4)


</dt> <dd>

Mit Aktivier barer Verschlüsselung. Alle Daten, die vom Client an den Server und vom Server an den Client gesendet werden, werden verschlüsselt und mit den Federal Information Processing Standard (FI)-Verschlüsselungsalgorithmen mithilfe der Kryptografiemodule von Microsoft entschlüsselt. Der Standardwert für "Sicherheitsanforderungen für kryptografische Module" ist "Standard". In den Informationen zu den in der US-Regierung verwendeten Hardware-und Softwaremodulen werden die behördlichen Anforderungen für Hardware-und Software Kryptografiemodule beschrieben. 2001 140-2 1994 140-1

</dd> </dl>

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

**Policysourceminverschlüsselunglevel**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die **minverschlüsseltionlevel** -Eigenschaft vom Server, von der Gruppenrichtlinie oder standardmäßig konfiguriert wird.

<dt>

0 (0x0)
</dt> <dd>

Server

</dd> <dt>

1 (0x1)
</dt> <dd>

Gruppenrichtlinie

</dd> <dt>

2 (0x2)
</dt> <dd>

Standard

</dd> </dl>

</dd> <dt>

**Policysourcesecuritylayer**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die **securitylayer** -Eigenschaft vom Server, von der Gruppenrichtlinie oder standardmäßig konfiguriert wird.

<dt>

0 (0x0)
</dt> <dd>

Server

</dd> <dt>

1 (0x1)
</dt> <dd>

Gruppenrichtlinie

</dd> <dt>

2 (0x2)
</dt> <dd>

Standard

</dd> </dl>

</dd> <dt>

**Policysourceuserauthenticationrequired**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die **UserAuthenticationRequired** -Eigenschaft vom Server, von der Gruppenrichtlinie oder standardmäßig konfiguriert wird.

<dt>

0 (0x0)
</dt> <dd>

Server

</dd> <dt>

1 (0x1)
</dt> <dd>

Gruppenrichtlinie

</dd> <dt>

2 (0x2)
</dt> <dd>

Standard

</dd> </dl>

</dd> <dt>

**SecurityLayer**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **rdpsecuritylayer** ("RDP-Sicherheitsebene: Kommunikation zwischen dem Server und der Client verwendet die Native RDP-Verschlüsselung"), **Aushandlungs** ("die sicherste Ebene, die vom Client unterstützt wird, wird verwendet. Wenn unterstützt, wird TLS 1,0 verwendet. "), **SSL** (" SSL (TLS 1,0) "wird für die Server Authentifizierung verwendet, und alle Daten, die zwischen dem Server und dem Client übertragen werden, werden verschlüsselt. Diese Einstellung erfordert, dass der Server über ein SSL-kompatibles Zertifikat verfügt. "), **newtbd** (" eine neue Sicherheitsebene in Longhorn ")
</dt> </dl>

Gibt die Sicherheitsebene an, die zwischen dem Client und dem Server verwendet wird.

<dt>

<span id="RDP_Security_Layer"></span><span id="rdp_security_layer"></span><span id="RDP_SECURITY_LAYER"></span>

<span id="RDP_Security_Layer"></span><span id="rdp_security_layer"></span><span id="RDP_SECURITY_LAYER"></span>**RDP-Sicherheitsebene** (1)


</dt> <dd>

Bei der Kommunikation zwischen dem Server und dem Client wird die Native RDP-Verschlüsselung verwendet.

</dd> <dt>

<span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>

<span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>**Aushandeln** (2)


</dt> <dd>

Die sicherste Ebene, die vom Client unterstützt wird, wird verwendet. Wenn unterstützt, wird SSL (TLS 1,0) verwendet.

</dd> <dt>

<span id="SSL"></span><span id="ssl"></span>

<span id="SSL"></span><span id="ssl"></span>**SSL** (3)


</dt> <dd>

SSL (TLS 1,0) wird für die Server Authentifizierung und für die Verschlüsselung aller Daten verwendet, die zwischen dem Server und dem Client übertragen werden. Diese Einstellung erfordert, dass der Server über ein SSL-kompatibles Zertifikat verfügt. Diese Einstellung ist nicht kompatibel mit dem **minverschlüsseltionlevel** -Wert 1.

</dd> <dt>

<span id="NEWTBD"></span><span id="newtbd"></span>

<span id="NEWTBD"></span><span id="newtbd"></span>**Newtbd** (4)


</dt> <dd>

Eine neue Sicherheitsebene.

</dd> </dl>

</dd> <dt>

**SSLCertificateSHA1Hash**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt den SHA1-Hash im Hexadezimal Format des SSL-Zertifikats an, das vom Zielserver verwendet werden soll.

Sie finden den Fingerabdruck eines Zertifikats mithilfe des MMC-Snap-Ins "Zertifikate" auf der Registerkarte "Details" auf der Seite "Zertifikat Eigenschaften".

</dd> <dt>

**SSLCertificateSHA1HashType**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt den Status der **SSLCertificateSHA1Hash** -Eigenschaft an.

<dt>

0 (0x0)
</dt> <dd>

Ungültig

</dd> <dt>

1 (0x1)
</dt> <dd>

Standardmäßig selbst signiert

</dd> <dt>

2 (0x2)
</dt> <dd>

Standard Gruppenrichtlinie erzwungen

</dd> <dt>

3 (0x3)
</dt> <dd>

Benutzerdefiniert

</dd> </dl>

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

**Terminal Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name des Terminals.

Diese Eigenschaft wird von [**Win32 \_ TerminalSetting**](win32-terminalsetting.md)geerbt.

</dd> <dt>

**TerminalProtocol**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name des Sitzungsschicht Protokolls. Beispiel: Microsoft RDP 5,0.

</dd> <dt>

**Transport**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Transporttyp, der in der Verbindung verwendet wird. beispielsweise TCP, NetBIOS oder IPX/SPX.

</dd> <dt>

**UserAuthenticationRequired**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt den Typ der Benutzerauthentifizierung an, die für Remote Verbindungen verwendet wird. Wenn der Wert auf 1 festgelegt ist, bedeutet dies, dass **UserAuthenticationRequired** zur Verbindungszeit eine Benutzerauthentifizierung erfordert, um den Server Schutz vor Netzwerk Angriffen zu erhöhen. Nur [Remotedesktopprotokoll](remote-desktop-protocol.md) (RDP)-Clients, die RDP-Version 6,0 oder höher unterstützen, können eine Verbindung herstellen. Um Unterbrechungen für Remote Benutzer zu vermeiden, wird empfohlen, RDP-Clients bereitzustellen, die die entsprechende Protokollversion unterstützen, bevor Sie die-Eigenschaft aktivieren.

Verwenden Sie die [**setuserauthenticationrequired**](setuserauthenticationrequired-win32-tsgeneralsetting.md) -Methode, um diese Eigenschaft zu aktivieren oder zu deaktivieren.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

Die Benutzerauthentifizierung bei Verbindung ist deaktiviert.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (1)


</dt> <dd>

Die Benutzerauthentifizierung bei Verbindung ist aktiviert.

</dd> </dl>

</dd> <dt>

**WindowsAuthentication**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob die Verbindung standardmäßig auf den standardmäßigen Windows-Authentifizierungsprozess oder auf ein anderes auf dem System installiertes Authentifizierungs Paket festgelegt ist.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

Der standardmäßige Windows-Authentifizierungsprozess wird nicht standardmäßig verwendet.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (1)


</dt> <dd>

Standardmäßig wird der Windows-Authentifizierungsprozess standardmäßig verwendet.

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Beachten Sie, dass Windows-Stationen, die nicht der Konsolen Sitzung zugeordnet sind, nicht auf die Methoden und Eigenschaften dieser Klasse zugreifen können. Wenn ein Versuch unternommen wird, indem "Console" als Wert der Terminalname-Eigenschaft angegeben wird, wird **WBEM \_ E \_ \_** von Methoden dieses Objekts zurückgegeben. Dieser Fehlercode wird auch zurückgegeben, wenn eine Fenster Station versucht, Methoden dieses Objekts zum Hinzufügen oder Ändern der Sicherheitseigenschaften der Konten "LocalSystem", "LocalService" oder "Network Service" aufzurufen.

Zum Herstellen einer Verbindung mit dem \\ root \\ CIMV2 \\ TerminalServices-Namespace muss die Authentifizierungs Ebene den Datenschutz für das Paket enthalten. Bei C/C++-aufrufen handelt es sich hierbei um eine Authentifizierungs Ebene der **RPC- \_ c- \_ authn- \_ Ebene \_ Pkt \_ Privacy**. Bei Visual Basic-und Skript aufrufen handelt es sich hierbei um eine Authentifizierungs Ebene von **wbemauthenticationlevelpzprivacy** oder "PKTPRIVACY" mit einem Wert von 6. Im folgenden Visual Basic Scripting Edition (VBScript)-Beispiel wird gezeigt, wie eine Verbindung mit einem Remote Computer mit Paket Datenschutz hergestellt wird.


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>Tscsgwmi. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ TerminalSetting**](win32-terminalsetting.md)
</dt> </dl>

 

