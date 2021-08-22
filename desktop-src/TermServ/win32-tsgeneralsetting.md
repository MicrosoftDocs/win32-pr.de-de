---
title: Win32_TSGeneralSetting-Klasse
description: Stellt allgemeine Einstellungen des Terminals dar, z. B. die Verschlüsselungsebene und das Transportprotokoll.
ms.assetid: a31d68c0-e446-4d78-85e0-5173e7870255
ms.tgt_platform: multiple
keywords:
- Win32_TSGeneralSetting der Remotedesktopdienste
- Win32_TSGeneralSetting klasse Remotedesktopdienste , beschrieben
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
ms.openlocfilehash: de2cc2e7ede46b503e0d33f65c5735d5e0cc653a75184384be2d706bfc8ac9cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999810"
---
# <a name="win32_tsgeneralsetting-class"></a>Win32 \_ TSGeneralSetting-Klasse

Die **WMI-Klasse Win32 \_ TSGeneralSetting** stellt allgemeine Einstellungen des Terminals dar, z. B. die Verschlüsselungsebene und das Transportprotokoll.

Die folgende Syntax wird von MOF-Code vereinfacht und enthält alle definierten und geerbten Eigenschaften in alphabetischer Reihenfolge. Referenzinformationen zu Methoden finden Sie in der Tabelle der Methoden weiter unten in diesem Thema.

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

Die **Win32 \_ TSGeneralSetting-Klasse** verfügt über die folgenden Membertypen:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **Win32 \_ TSGeneralSetting-Klasse** verfügt über diese Methoden.



| Methode                                                                                        | Beschreibung                                                                                                                                                             |
|:----------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SetEncryptionLevel**](win32-tsgeneralsetting-setencryptionlevel.md)                       | Legt die Verschlüsselungsstufe fest.<br/>                                                                                                                                   |
| [**SetSecurityLayer**](win32-tsgeneralsetting-setsecuritylayer.md)                           | Legt die Sicherheitsschicht auf eine der Folgenden fest: "RDP-Sicherheitsschicht" (0), "Aushandlung" (1) oder "SSL" (2).<br/>                                                                   |
| [**SetUserAuthenticationRequired**](setuserauthenticationrequired-win32-tsgeneralsetting.md) | Aktiviert oder deaktiviert die Anforderung, dass Benutzer zur Verbindungszeit durch Festlegen des Werts der **UserAuthenticationRequired-Eigenschaft authentifiziert werden** müssen.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ TSGeneralSetting-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

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

**CertificateName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Anzeigename für den Namen des persönlichen Zertifikats des lokalen Computers.

</dd> <dt>

**Zertifikate**
</dt> <dd> <dl> <dt>

Datentyp: **uint8 array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Enthält einen serialisierten Zertifikatspeicher, der alle  Zertifikate aus dem Speicher Mein Benutzerkonto auf dem Computer enthält, die gültige Serverzertifikate für die Verwendung mit Secure Sockets Layer (SSL) sind.

</dd> <dt>

**Comment**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Beschreibender Name der Kombination aus Sitzungsebene und Transportprotokoll.

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

**MinEncryptionLevel**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Niedrig** ("Nur vom Client an den Server gesendete Daten werden durch Verschlüsselung basierend auf der Standardschlüsselstärke des Servers geschützt. Vom Server an den Client gesendete Daten sind nicht geschützt."), **Mittel** ("Alle zwischen Server und Client gesendeten Daten werden basierend auf der Standardschlüsselstärke des Servers durch Verschlüsselung geschützt."), **Hoch** ("Alle zwischen Server und Client gesendeten Daten werden basierend auf der maximalen Schlüsselstärke des Servers durch Verschlüsselung geschützt.")
</dt> </dl>

Die Mindestverschlüsselungsstufe.

<dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>**Niedrig** (1)


</dt> <dd>

Niedrige Verschlüsselungsebene. Nur daten, die vom Client an den Server gesendet werden, werden mit 56-Bit-Verschlüsselung verschlüsselt. Beachten Sie, dass vom Server an den Client gesendete Daten nicht verschlüsselt sind.

</dd> <dt>

<span id="Medium___Client_Compatible"></span><span id="medium___client_compatible"></span><span id="MEDIUM___CLIENT_COMPATIBLE"></span>

<span id="Medium___Client_Compatible"></span><span id="medium___client_compatible"></span><span id="MEDIUM___CLIENT_COMPATIBLE"></span>**Mittel/Clientkompatibel** (2)


</dt> <dd>

Clientkompatible Verschlüsselungsebene. Alle vom Client an den Server und vom Server an den Client gesendeten Daten werden mit der maximalen Schlüsselstärke verschlüsselt, die vom Client unterstützt wird.

</dd> <dt>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>**Hoch** (3)


</dt> <dd>

Hohes Maß an Verschlüsselung. Alle vom Client an den Server und vom Server an den Client gesendeten Daten werden mit starker 128-Bit-Verschlüsselung verschlüsselt. Clients, die diese Verschlüsselungsstufe nicht unterstützen, können keine Verbindung herstellen.

</dd> <dt>

<span id="FIPS_Compliant"></span><span id="fips_compliant"></span><span id="FIPS_COMPLIANT"></span>

<span id="FIPS_Compliant"></span><span id="fips_compliant"></span><span id="FIPS_COMPLIANT"></span>**FIPS-kompatibel** (4)


</dt> <dd>

FIPS-konforme Verschlüsselung. Alle daten, die vom Client zum Server und vom Server zum Client gesendet werden, werden mithilfe der verschlüsselungsalgorithmen der Federal Information Processing Standard (FIPS) mithilfe der Microsoft-Kryptografiemodule verschlüsselt und entschlüsselt. FIPS ist ein Standard mit dem Titel "Sicherheitsanforderungen für Kryptografiemodule". FIPS 140-1 (1994) und FIPS 140-2 (2001) beschreiben die anforderungen der Regierung für hardware- und software kryptografische Module, die innerhalb der US-Regierung verwendet werden.

</dd> </dl>

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

**PolicySourceMinEncryptionLevel**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, **ob die MinEncryptionLevel-Eigenschaft** vom Server, von der Gruppenrichtlinie oder standardmäßig konfiguriert wird.

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

**PolicySourceSecurityLayer**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, **ob die SecurityLayer-Eigenschaft** vom Server, von der Gruppenrichtlinie oder standardmäßig konfiguriert wird.

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

**PolicySourceUserAuthenticationRequired**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die **UserAuthenticationRequired-Eigenschaft** vom Server, von der Gruppenrichtlinie oder standardmäßig konfiguriert wird.

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

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **RDPSecurityLayer** ("RDP-Sicherheitsschicht: Kommunikation zwischen dem Server und dem Client verwendet native RDP-Verschlüsselung."), **Negotiate** ("Die sicherste Ebene, die vom Client unterstützt wird, wird verwendet. Wenn dies unterstützt wird, wird TLS 1.0 verwendet."), **SSL** ("SSL (TLS 1.0) wird für die Serverauthentifizierung sowie für die Verschlüsselung aller Daten verwendet, die zwischen dem Server und dem Client übertragen werden. Für diese Einstellung muss der Server über ein SSL-kompatibles Zertifikat verfügen."), **NEWTBD** ("A NEW SECURITY LAYER in LONGHORN").
</dt> </dl>

Gibt die Sicherheitsschicht an, die zwischen Client und Server verwendet wird.

<dt>

<span id="RDP_Security_Layer"></span><span id="rdp_security_layer"></span><span id="RDP_SECURITY_LAYER"></span>

<span id="RDP_Security_Layer"></span><span id="rdp_security_layer"></span><span id="RDP_SECURITY_LAYER"></span>**RDP-Sicherheitsschicht** (1)


</dt> <dd>

Für die Kommunikation zwischen dem Server und dem Client wird native RDP-Verschlüsselung verwendet.

</dd> <dt>

<span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>

<span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>**Aushandeln** (2)


</dt> <dd>

Die sicherste Ebene, die vom Client unterstützt wird, wird verwendet. Falls unterstützt, wird SSL (TLS 1.0) verwendet.

</dd> <dt>

<span id="SSL"></span><span id="ssl"></span>

<span id="SSL"></span><span id="ssl"></span>**SSL** (3)


</dt> <dd>

SSL (TLS 1.0) wird für die Serverauthentifizierung und die Verschlüsselung aller zwischen dem Server und dem Client übertragenen Daten verwendet. Für diese Einstellung muss der Server über ein SSL-kompatibles Zertifikat verfügen. Diese Einstellung ist nicht kompatibel mit dem **MinEncryptionLevel-Wert** 1.

</dd> <dt>

<span id="NEWTBD"></span><span id="newtbd"></span>

<span id="NEWTBD"></span><span id="newtbd"></span>**NEWTBD** (4)


</dt> <dd>

Eine neue Sicherheitsebene.

</dd> </dl>

</dd> <dt>

**SSLCertificateSHA1Hash**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt den SHA1-Hash im Hexadezimalformat des SSL-Zertifikats an, das der Zielserver verwenden soll.

Den Fingerabdruck eines Zertifikats finden Sie über das MMC-Snap-In Zertifikate auf der Registerkarte Details der Eigenschaftenseite des Zertifikats.

</dd> <dt>

**SSLCertificateSHA1HashType**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt den Zustand der **SSLCertificateSHA1Hash-Eigenschaft** an.

<dt>

0 (0x0)
</dt> <dd>

Ungültig

</dd> <dt>

1 (0x1)
</dt> <dd>

Standardmäßig selbstsignierend

</dd> <dt>

2 (0x2)
</dt> <dd>

Erzwungene Standardgruppenrichtlinie

</dd> <dt>

3 (0x3)
</dt> <dd>

Benutzerdefiniert

</dd> </dl>

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)
</dt> </dl>

Aktueller Status des Objekts. Es können verschiedene Betriebs- und Nichtoperationsstatus definiert werden. Betriebsstatus: "OK", "Heruntergestuft" und "Pred Fail" (ein Element, z. B. ein SMART-fähiges Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, sagt aber einen Fehler in naher Zukunft vorher). Nichtoperationale Status: "Error", "Starting", "Stopping" und "Service". Letzteres, "Dienst", kann während des Spiegelungsresilverings eines Datenträgers, beim erneuten Laden einer Benutzerberechtigungsliste oder bei anderen Verwaltungsaufgaben angewendet werden. Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.

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

**TerminalName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name des Terminals.

Diese Eigenschaft wird von [**Win32 \_ TerminalSetting**](win32-terminalsetting.md)geerbt.

</dd> <dt>

**TerminalProtocol**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name des Sitzungsebenenprotokolls. Beispiel: Microsoft RDP 5.0.

</dd> <dt>

**Transport**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der in der Verbindung verwendete Transporttyp. Beispielsweise TCP, NetBIOS oder IPX/SPX.

</dd> <dt>

**UserAuthenticationRequired**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt den Typ der Benutzerauthentifizierung an, der für Remoteverbindungen verwendet wird. Wenn diese Option auf 1 festgelegt ist, bedeutet dies, dass **UserAuthenticationRequired** zur Verbindungszeit eine Benutzerauthentifizierung erfordert, um den Serverschutz vor Netzwerkangriffen zu erhöhen. Nur [Remotedesktopprotokoll-Clients](remote-desktop-protocol.md) (RDP), die RDP Version 6.0 oder höher unterstützen, können eine Verbindung herstellen. Um Unterbrechungen für Remotebenutzer zu vermeiden, wird empfohlen, dass Sie RDP-Clients bereitstellen, die die entsprechende Protokollversion unterstützen, bevor Sie die -Eigenschaft aktivieren.

Verwenden Sie die [**SetUserAuthenticationRequired-Methode,**](setuserauthenticationrequired-win32-tsgeneralsetting.md) um diese Eigenschaft zu aktivieren oder zu deaktivieren.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**FALSE** (0)


</dt> <dd>

Die Benutzerauthentifizierung bei der Verbindung ist deaktiviert.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**TRUE** (1)


</dt> <dd>

Die Benutzerauthentifizierung bei der Verbindung ist aktiviert.

</dd> </dl>

</dd> <dt>

**WindowsAuthentication**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob die Verbindung standardmäßig auf den Standard-Windows Authentifizierungsprozess oder auf ein anderes Authentifizierungspaket festgelegt ist, das auf dem System installiert wurde.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**FALSE** (0)


</dt> <dd>

Standardmäßig wird nicht der Standard-Windows-Authentifizierungsprozess verwendet.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**TRUE** (1)


</dt> <dd>

Der Standardwert ist der Standardmäßige Windows Authentifizierungsprozess.

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Hinweise

Beachten Sie, dass Fensterstationen, die nicht der Konsolensitzung zugeordnet sind, nicht auf die Methoden und Eigenschaften dieser Klasse zugreifen können. Wenn versucht wird, dies zu tun, indem "Console" als Wert der TerminalName-Eigenschaft angegeben wird, geben Methoden dieses Objekts **WBEM \_ E NOT SUPPORTED \_ \_ zurück.** Dieser Fehlercode wird auch zurückgegeben, wenn eine Fensterstation versucht, Methoden dieses Objekts zum Hinzufügen oder Ändern der Sicherheitseigenschaften der Konten LocalSystem, LocalService oder NetworkService aufzurufen.

Um eine Verbindung mit dem \\ \\ CIMV2 \\ TerminalServices-Stammnamespace herzustellen, muss die Authentifizierungsebene Paketdatenschutz enthalten. Bei C/C++-Aufrufen ist dies eine Authentifizierungsebene von **RPC \_ C \_ AUTHN \_ LEVEL \_ PKT \_ PRIVACY**. Bei Visual Basic- und Skriptaufrufen ist dies die Authentifizierungsebene **WbemAuthenticationLevelPktPrivacy** oder "pktPrivacy" mit dem Wert 6. Das folgende Beispiel Visual Basic Scripting Edition (VBScript) zeigt, wie Sie eine Verbindung mit einem Remotecomputer mit Paketschutz herstellen.


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



Managed Object Format -Dateien (MOF) enthalten die Definitionen für Windows Management Instrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ TerminalSetting**](win32-terminalsetting.md)
</dt> </dl>

 

