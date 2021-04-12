---
title: Win32_TSSessionDirectory-Klasse
description: Definiert die Konfigurationseinstellungen für den Remotedesktopverbindung Broker (RD-Verbindungsbroker) für die Win32- \_ Klasse "tssessiondirectorysetting".
ms.assetid: ef9042c2-4a35-49e9-b195-fb37c0919068
ms.tgt_platform: multiple
keywords:
- Win32_TSSessionDirectory-Klasse Remotedesktopdienste
- Win32_TSSessionDirectory Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory
- Win32_TSSessionDirectory.Caption
- Win32_TSSessionDirectory.Description
- Win32_TSSessionDirectory.InstallDate
- Win32_TSSessionDirectory.Name
- Win32_TSSessionDirectory.Status
- Win32_TSSessionDirectory.SessionDirectoryLocation
- Win32_TSSessionDirectory.PolicySourceSessionDirectoryLocation
- Win32_TSSessionDirectory.SessionDirectoryActive
- Win32_TSSessionDirectory.PolicySourceSessionDirectoryActive
- Win32_TSSessionDirectory.SessionDirectoryExposeServerIP
- Win32_TSSessionDirectory.PolicySourceSessionDirectoryExposeServerIP
- Win32_TSSessionDirectory.SessionDirectoryClusterName
- Win32_TSSessionDirectory.PolicySourceLoadBalancing
- Win32_TSSessionDirectory.GetLoadBalancingState
- Win32_TSSessionDirectory.GetServerWeight
- Win32_TSSessionDirectory.PolicySourceSessionDirectoryClusterName
- Win32_TSSessionDirectory.SessionDirectoryIPAddress
- Win32_TSSessionDirectory.GetTSRedirectorMode
- Win32_TSSessionDirectory.PolicySourceTSRedirectorMode
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb50ed77b99f415ae551dfcf69655af5c1d77501
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949730"
---
# <a name="win32_tssessiondirectory-class"></a>Win32- \_ Klasse "tssessiondirectory"

Definiert die Konfigurationseinstellungen für den Remotedesktopverbindung Broker (RD-Verbindungsbroker) für die Win32-Klasse " [**\_ tssessiondirectorysetting**](win32-tssessiondirectorysetting.md) ".

> [!Note]  
> In Windows Server 2008 R2 wurde der Name des Terminal Dienste-Sitzungs Brokers (TS-Sitzungs Broker) in "RD-Verbindungsbroker" geändert. Diese Eigenschaften gelten für alle unterstützten Betriebssysteme, sofern nicht anders angegeben.

 

Die folgende Syntax wird aus dem MOF-Code vereinfacht und umfasst alle definierten und geerbten Eigenschaften in alphabetischer Reihenfolge. Referenzinformationen zu Methoden finden Sie in der Tabelle mit den Methoden weiter unten in diesem Thema.

## <a name="syntax"></a>Syntax

``` syntax
[dynamic, provider("Win32_WIN32_TSSESSIONDIRECTORY_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer"), AMENDMENT]
class Win32_TSSessionDirectory : CIM_Setting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   SessionDirectoryLocation;
  uint32   PolicySourceSessionDirectoryLocation;
  uint32   SessionDirectoryActive;
  uint32   PolicySourceSessionDirectoryActive;
  uint32   SessionDirectoryExposeServerIP;
  uint32   PolicySourceSessionDirectoryExposeServerIP;
  string   SessionDirectoryClusterName;
  uint32   PolicySourceLoadBalancing;
  uint32   GetLoadBalancingState;
  uint32   GetServerWeight;
  uint32   PolicySourceSessionDirectoryClusterName;
  string   SessionDirectoryIPAddress;
  uint32   GetTSRedirectorMode;
  uint32   PolicySourceTSRedirectorMode;
};
```

## <a name="members"></a>Member

Die Win32-Klasse " **\_ tssessiondirectory** " verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die Win32-Klasse " **\_ tssessiondirectory** " verfügt über diese Methoden.



| Methode                                                                                                  | BESCHREIBUNG                                                                                                  |
|:--------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------|
| [**"Buildeuserdisktemplate"**](createuserdisktemplate-win32-tssessiondirectory.md)                       | Erstellt eine Vorlage für Benutzer Datenträger.<br/>                                                                     |
| [**Disableuservhd**](disableuservhd-win32-tssessiondirectory.md)                                       | Deaktiviert eine Benutzerprofil-VHD.<br/>                                                                      |
| [**Enableuservhd**](enableuservhd-win32-tssessiondirectory.md)                                         | Aktiviert eine Benutzerprofil-VHD auf einem RDSH-Server.<br/>                                                     |
| [**Getcurrentredirectableadressen**](getcurrentredirectableaddresses-win32-tssessiondirectory.md)     | Ruft die derzeit konfigurierte Liste der für den DNS berechtigten Adressen und den Umleitungstyp ab.<br/>        |
| [**Getredirectableadressen**](getredirectableaddresses-win32-tssessiondirectory.md)                   | Ruft die gesamte Liste der für den DNS berechtigten Adressen ab.<br/>                                                |
| [**Pingsessiondirectory**](pingsessiondirectory-win32-tssessiondirectory.md)                           | Überprüft, ob der RD-Verbindungsbroker Server verfügbar ist.<br/>                                      |
| [**Setcurrentredirectableadressen**](setcurrentredirectableaddresses-win32-tssessiondirectory.md)     | Legt die konfigurierte Liste der für den DNS berechtigten Adressen und den Umleitungstyp fest.<br/>                     |
| [**Setloadbalancingstate**](setloadbalancingstate-win32-tssessiondirectory.md)                         | Legt den Wert fest, mit dem angegeben wird, ob der Server an RD-Verbindungsbroker Lastenausgleich beteiligt ist.<br/> |
| [**Setserverweight**](setserverweight-win32-tssessiondirectory.md)                                     | Legt den Server Gewichtungswert für RD-Verbindungsbroker Lastenausgleich fest.<br/>                             |
| [**"-Essiondirector"**](win32-tssessiondirectory-setsessiondirectoryactive.md)                 | Deaktiviert und aktiviert die RD-Verbindungsbroker.<br/>                                                    |
| [**"Server-Sitzungs Verzeichnis-IP"**](win32-tssessiondirectory-setsessiondirectoryexposeserverip.md) | Legt die **sessiondirectoriyexposeserverip-** Eigenschaft fest.<br/>                                             |
| [**"Gensessiondirectoriyproperty"**](win32-tssessiondirectory-setsessiondirectoryproperty.md)             | Legt die **sessiondirector yLocation** -Eigenschaft oder die **sessiondirectoriyclustername** -Eigenschaft fest.<br/>   |
| [**Settsredirector Mode**](settsredirectormode-win32-tssessiondirectory.md)                             | Diese Methode ist nicht verfügbar.<br/>                                                                     |



 

### <a name="properties"></a>Eigenschaften

Die Win32-Klasse " **\_ tssessiondirectory** " verfügt über diese Eigenschaften.

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

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Beschreibung des Objekts.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**Getloadbalancingstate**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob der Server für die Teilnahme an RD-Verbindungsbroker Lastenausgleich konfiguriert ist.

<dt>

0
</dt> <dd>

Der Server ist nicht für die Teilnahme an RD-Verbindungsbroker Lastenausgleich konfiguriert.

</dd> <dt>

1
</dt> <dd>

Der Server ist so konfiguriert, dass er an RD-Verbindungsbroker Lastenausgleich beteiligt ist.

</dd> </dl>

</dd> <dt>

**Getserverweight**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft den Wert für den Server Gewichtungswert ab, der in RD-Verbindungsbroker Lastenausgleich verwendet wird.

</dd> <dt>

**Gettsredirector Mode**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob der Server so konfiguriert ist, dass er als Remotedesktopdienste Redirector fungiert.

<dt>

0
</dt> <dd>

Der Server ist so konfiguriert, dass er als Remotedesktopdienste Redirector fungiert.

</dd> <dt>

1
</dt> <dd>

Der Server ist nicht so konfiguriert, dass er als Remotedesktopdienste Redirector fungiert.

</dd> </dl>

**Windows Server 2008:** Diese Eigenschaft ist nicht verfügbar.

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

**Policysourceloadbalancing**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die **getloadbalancingstate** -Eigenschaft vom Server oder von der Gruppenrichtlinie konfiguriert wird.

<dt>

0 (0x0)
</dt> <dd>

Server

</dd> <dt>

1 (0x1)
</dt> <dd>

Gruppenrichtlinie

</dd> </dl>

</dd> <dt>

**Policysourcesessiondirectorialactive**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die **sessiondirectoryactive** -Eigenschaft vom Server oder von der Gruppenrichtlinie konfiguriert wird.

<dt>

0 (0x0)
</dt> <dd>

Server

</dd> <dt>

1 (0x1)
</dt> <dd>

Gruppenrichtlinie

</dd> </dl>

</dd> <dt>

**Policysourcesessiondirectoriyclustername**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die **SessionDirectoryClusterName** -Eigenschaft vom Server oder von der Gruppenrichtlinie konfiguriert wird.

<dt>

0 (0x0)
</dt> <dd>

Server

</dd> <dt>

1 (0x1)
</dt> <dd>

Gruppenrichtlinie

</dd> </dl>

</dd> <dt>

**Policysourcesessiondirectoriyexposeserverip**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die **SessionDirectoryExposeServerIP-** Eigenschaft vom Server oder von der Gruppenrichtlinie konfiguriert wird.

<dt>

0 (0x0)
</dt> <dd>

Server

</dd> <dt>

1 (0x1)
</dt> <dd>

Gruppenrichtlinie

</dd> </dl>

</dd> <dt>

**Policysourcesessiondirectoriylocation**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die **SessionDirectoryLocation** -Eigenschaft vom Server oder von der Gruppenrichtlinie konfiguriert wird.

<dt>

0 (0x0)
</dt> <dd>

Server

</dd> <dt>

1 (0x1)
</dt> <dd>

Gruppenrichtlinie

</dd> </dl>

</dd> <dt>

**Policysourcetsredirector Mode**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Diese Eigenschaft ist nicht verfügbar.

**Windows Server 2008 R2:** Gibt an, ob die **gettsredirectormode** -Eigenschaft vom Server oder von der Gruppenrichtlinie konfiguriert wird.

<dt>

0 (0x0)
</dt> <dd>

Server

</dd> <dt>

1 (0x1)
</dt> <dd>

Gruppenrichtlinie

</dd> </dl>

</dd> <dt>

**Sessiondirectorialactive**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Gibt an, ob Remotedesktopdienste an der RD-Verbindungsbroker teilnimmt.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

Remotedesktopdienste Teilnahme am RD-Verbindungsbroker ist deaktiviert.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (1)


</dt> <dd>

Remotedesktopdienste Teilnahme am RD-Verbindungsbroker aktiviert ist.

</dd> </dl>

</dd> <dt>

**Sessiondirectoriyclustername**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die virtuelle IP-Adresse des Clusters, zu dem der RD-Sitzungshost-Server gehört.

</dd> <dt>

**Sessiondirectoriyexposeserverip**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob das Abrufen der IP-Adresse des RD-Verbindungsbroker zulässig ist.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

Der Abruf wurde verweigert.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (1)


</dt> <dd>

Der Abruf ist zulässig.

</dd> </dl>

</dd> <dt>

**Sessiondirector yipaddress**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Die IP-Adresse des vom Sitzungs Verzeichnis verwendeten LAN-Adapters.

</dd> <dt>

**Sessiondirectoriylocation**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Netzwerk-DNS-Name oder die IP-Adresse des Servers, auf dem der RD-Verbindungsbroker-Dienst ausgeführt wird.

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

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Zum Herstellen einer Verbindung mit dem \\ \\ root \\ CIMV2 \\ TerminalServices-Namespace muss die Authentifizierungs Ebene den Datenschutz für das Paket enthalten. Bei C/C++-aufrufen handelt es sich hierbei um eine Authentifizierungs Ebene der **RPC- \_ c- \_ authn- \_ Ebene \_ Pkt \_ Privacy**. Bei Visual Basic-und Skript aufrufen handelt es sich hierbei um eine Authentifizierungs Ebene von **wbemauthenticationlevelpzprivacy** oder "PKTPRIVACY" mit einem Wert von sechs.

Im folgenden Visual Basic Scripting Edition (VBScript)-Beispiel wird gezeigt, wie eine Verbindung mit einem Remote Computer mit Paket Datenschutz hergestellt wird.


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



In Windows Server 2008 wurde der Name des Terminaldienste-Sitzungs Verzeichnis Features in Terminaldienste-Sitzungs Broker geändert.

In Windows Server 2008 R2 wurde der Name des Terminal Dienste-Sitzungs Broker Features in Remotedesktopverbindung Broker geändert.

Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>Tscsgwmi. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM- \_ Einstellung**](cim-setting.md)
</dt> <dt>

[**Win32- \_ tssessiondirectorysetting**](win32-tssessiondirectorysetting.md)
</dt> </dl>

 

