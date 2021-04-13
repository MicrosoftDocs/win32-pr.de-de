---
description: Das Win32- \_ networkprotocol-&\# 8194; Die WMI-Klasse stellt ein Protokoll und seine Netzwerk Eigenschaften auf einem Win32-Computersystem dar.
ms.assetid: c864a694-d507-4629-91c5-bd26ccf397f7
ms.tgt_platform: multiple
title: Win32_NetworkProtocol-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkProtocol
- Win32_NetworkProtocol.Caption
- Win32_NetworkProtocol.Description
- Win32_NetworkProtocol.InstallDate
- Win32_NetworkProtocol.Status
- Win32_NetworkProtocol.ConnectionlessService
- Win32_NetworkProtocol.GuaranteesDelivery
- Win32_NetworkProtocol.GuaranteesSequencing
- Win32_NetworkProtocol.MaximumAddressSize
- Win32_NetworkProtocol.MaximumMessageSize
- Win32_NetworkProtocol.MessageOriented
- Win32_NetworkProtocol.MinimumAddressSize
- Win32_NetworkProtocol.Name
- Win32_NetworkProtocol.PseudoStreamOriented
- Win32_NetworkProtocol.SupportsBroadcasting
- Win32_NetworkProtocol.SupportsConnectData
- Win32_NetworkProtocol.SupportsDisconnectData
- Win32_NetworkProtocol.SupportsEncryption
- Win32_NetworkProtocol.SupportsExpeditedData
- Win32_NetworkProtocol.SupportsFragmentation
- Win32_NetworkProtocol.SupportsGracefulClosing
- Win32_NetworkProtocol.SupportsGuaranteedBandwidth
- Win32_NetworkProtocol.SupportsMulticasting
- Win32_NetworkProtocol.SupportsQualityofService
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 33817fa4aa55747ecf9d4e89f5dcf406160c0c67
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483790"
---
# <a name="win32_networkprotocol-class"></a>Win32- \_ networkprotocol-Klasse

Die **Win32 \_ Network Protocol** [WMI-Klasse](../wmisdk/retrieving-a-class.md) stellt ein Protokoll und seine Netzwerk Eigenschaften auf einem Win32-Computersystem dar.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4D8-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_NetworkProtocol : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  boolean  ConnectionlessService;
  boolean  GuaranteesDelivery;
  boolean  GuaranteesSequencing;
  uint32   MaximumAddressSize;
  uint32   MaximumMessageSize;
  boolean  MessageOriented;
  uint32   MinimumAddressSize;
  string   Name;
  boolean  PseudoStreamOriented;
  boolean  SupportsBroadcasting;
  boolean  SupportsConnectData;
  boolean  SupportsDisconnectData;
  boolean  SupportsEncryption;
  boolean  SupportsExpeditedData;
  boolean  SupportsFragmentation;
  boolean  SupportsGracefulClosing;
  boolean  SupportsGuaranteedBandwidth;
  boolean  SupportsMulticasting;
  boolean  SupportsQualityofService;
};
```

## <a name="members"></a>Member

Die **Win32- \_ networkprotocol** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32- \_ networkprotocol** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Caption")
</dt> </dl>

Eine kurze Textbeschreibung des-Objekts.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**ConnectionlessService**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32- \_ API \| Windows Sockets Structures \| Protokoll \_ Info \| dwserviceflags \| XP1 \_ Connectionless")
</dt> </dl>

Das Protokoll unterstützt den Verbindungs losen Dienst. Ein verbindungsloses-Dienst (Datagramm) beschreibt ein Kommunikationsprotokoll oder einen Transport, in dem Datenpakete unabhängig voneinander weitergeleitet werden und den verschiedenen Routen folgen können und in einer anderen Reihenfolge als der Sendevorgang eintreffen. Umgekehrt bietet ein Verbindungs orientierter Dienst eine virtuelle Verbindung, über die Datenpakete in derselben Reihenfolge empfangen werden, in der Sie übertragen wurden. Wenn die Verbindung zwischen Computern fehlschlägt, wird die Anwendung benachrichtigt.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Description")
</dt> </dl>

Eine Textbeschreibung des-Objekts.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**Zustellungs Bereitstellung**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32- \_ API \| Windows Sockets Structures \| Protokoll \_ Info \| dwserviceflags \| XP \_ garantierte \_ Übermittlung")
</dt> </dl>

Das Protokoll unterstützt die Übermittlung von Datenpaketen. Wenn dieses Flag **false** ist, ist es unsicher, dass alle gesendeten Daten das beabsichtigte Ziel erreichen.

</dd> <dt>

**Die Sequenzierung**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32- \_ API \| Windows Sockets Structures \| Protokoll \_ Info \| dwserviceflags \| XP \_ garantierte \_ Reihenfolge")
</dt> </dl>

Mit dem Protokoll wird sichergestellt, dass die Daten in der Reihenfolge eintreffen, in der Sie gesendet wurden. Beachten Sie, dass dieses Merkmal nicht sicherstellt, dass die Daten nur in seiner Reihenfolge bereitgestellt werden.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](../wmisdk/standard-qualifiers.md) (" Install Date ")
</dt> </dl>

Gibt an, wann das Objekt installiert wurde. Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**MaximumAddressSize**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32- \_ API \| Windows Sockets Structures \| Protokoll \_ Info \| imaxsockaddr"), [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Zeichen")
</dt> </dl>

Maximale Länge einer vom Protokoll unterstützten Socketadresse. Socketadressen können Elemente sein, z. b. eine URL ( `www.microsoft.com` ) oder eine IP-Adresse ( `130.215.24.1` ).

</dd> <dt>

**Maximummessagesize**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32- \_ API \| Windows Sockets Structures \| Protokoll \_ Info \| dwmessagesize"), [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Zeichen")
</dt> </dl>

Maximale Nachrichtengröße, die vom Protokoll unterstützt wird. Dies ist die maximale Größe einer Nachricht, die vom Host gesendet oder empfangen werden kann. Bei Protokollen, die Nachrichtenrahmen nicht unterstützen, kann die tatsächliche maximale Größe einer Nachricht, die an eine bestimmte Adresse gesendet werden kann, kleiner als dieser Wert sein.

</dd> <dt>

**Messageoriented**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32- \_ API \| Windows Sockets Structures \| Protokoll \_ Info \| dwserviceflags \| XP \_ Nachrichten \_ orientiert")
</dt> </dl>

Protokoll ist Nachrichten orientiert. Ein Nachrichten orientiertes Protokoll verwendet Datenpakete zum Übertragen von Informationen. Im Gegensatz dazu übertragen Streamorientierte Protokolle Daten als kontinuierlichen Stream von Bytes.

</dd> <dt>

**MinimumAddressSize**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32- \_ API \| Windows Sockets Structures \| Protokoll \_ Info \| iminsockaddr"), [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Zeichen")
</dt> </dl>

Die minimale Länge einer Socketadresse, die vom Protokoll unterstützt wird.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("Name"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32- \_ API \| Windows Sockets Structures \| Protokoll \_ Info \| lpprotocol")
</dt> </dl>

Der Name des Protokolls.

Beispiel: "TCP/IP"

</dd> <dt>

**PseudoStreamOriented**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32- \_ API \| Windows Sockets Structures \| Protokoll \_ Info \| dwserviceflags \| XP \_ Pseudo Daten \_ Strom")
</dt> </dl>

Das Protokoll ist ein Nachrichten orientiertes Protokoll, das Datenpakete variabler Länge oder Stream-Daten für alle Empfangs Vorgänge empfangen kann. Diese optionale Funktion ist hilfreich, wenn eine Anwendung nicht in der Lage sein soll, Nachrichten in das Protokoll zu unterteilen, und Streamorientierte Merkmale erfordert. **True** gibt an, dass das Protokoll Pseudo Datenstrom orientiert ist.

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Status")
</dt> </dl>

Eine Zeichenfolge, die den aktuellen Status des Objekts angibt. Der Betriebsstatus und der nicht betriebliche Status können definiert werden. Der Betriebsstatus kann "OK", "heruntergestuft" und "pred Fail" enthalten. "Pred Fail" gibt an, dass ein Element ordnungsgemäß funktioniert, aber einen Fehler vorhersagt (z. b. ein intelligent-fähiges Festplattenlaufwerk).

Der nicht betriebliche Status kann "Error", "Starting", "Stop" und "Service" enthalten. "Service" kann während der Datenträger Spiegelung angewendet werden, indem eine Benutzer Berechtigungs Liste oder eine andere administrative Arbeit neu geladen wird. Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

Folgende Werte sind gültig:

<dt>

<span id="OK"></span><span id="ok"></span>

**OK** ("OK")


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

**Fehler** ("Fehler")


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

Herunter **gestuft ("** heruntergestuft")


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** ("unbekannt")


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Pred-** Fehler ("pred Fail")


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

Wird **gestartet** ("wird gestartet")


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

Wird **beendet ("wird angehalten** ")


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

**Dienst** ("Dienst")


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

**Betont** ("gestresst")


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

**Nicht wiederherstellen** ("nicht wiederherstellen")


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**Kein Kontakt** ("kein Kontakt")


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

**Verlorene** Kommunikations ("verlorene Kommunikations-")


</dt> <dd></dd> </dl>

</dd> <dt>

**SupportsBroadcasting**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32- \_ API \| Windows Sockets Structures \| Protokoll \_ Info \| dwserviceflags \| XP \_ unterstützt \_ Broadcast")
</dt> </dl>

Das Protokoll unterstützt einen Mechanismus zum Senden von Nachrichten über das Netzwerk.

</dd> <dt>

**SupportsConnectData**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32- \_ API \| Windows Sockets Structures \| Protokoll \_ Info \| dwserviceflags \| XP \_ Connect \_ Data")
</dt> </dl>

Mit dem Protokoll können Daten über das Netzwerk verbunden werden.

</dd> <dt>

**SupportsDisconnectData**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32- \_ API \| Windows Sockets Structures \| Protokoll \_ Info \| dwserviceflags \| XP \_ Disconnect \_ Data")
</dt> </dl>

Mit dem Protokoll können Daten über das Netzwerk getrennt werden.

</dd> <dt>

**SupportsEncryption**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32- \_ API \| Windows Sockets Structures \| Protokoll \_ Info \| dwserviceflags \| XP \_ verschlüsselt")
</dt> </dl>

Das Protokoll unterstützt die Datenverschlüsselung.

</dd> <dt>

**Supportsexpediteddata**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32- \_ API \| Windows Sockets Structures \| Protokoll \_ Info \| dwserviceflags \| XP \_ beschleunigte \_ Daten")
</dt> </dl>

Das Protokoll unterstützt beschleunigte Daten (auch als dringende Daten bezeichnet) im gesamten Netzwerk. Beschleunigte Daten können die Fluss Steuerung umgehen und Vorrang vor normalen Datenpaketen erhalten.

</dd> <dt>

**Supportsfragmentierung**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32- \_ API \| Windows Sockets Structures \| Protokoll \_ Info \| dwserviceflags \| XP \_ Fragmentierung")
</dt> </dl>

Das Protokoll unterstützt das Übertragen von Daten in Fragmenten. Das physische Netzwerk für die maximale Übertragungseinheit (MTU) ist in den Anwendungen ausgeblendet. Jeder Medientyp hat eine maximale Frame Größe, die nicht überschritten werden kann. Die Verbindungs Ebene ermittelt die MTU und meldet Sie den verwendeten Protokollen.

</dd> <dt>

**SupportsGracefulClosing**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32- \_ API \| Windows Sockets Structures \| Protokoll \_ Info \| dwserviceflags XP ordnungsgemäß \| \_ \_ Schließen")
</dt> </dl>

Das Protokoll unterstützt zweiphasenclose-Vorgänge, auch bekannt als "ordnungsgemäße Schließ Vorgänge". Andernfalls unterstützt das Protokoll nur Abbruch Vorgänge.

</dd> <dt>

**Supportszuder Bandbreite**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32- \_ API \| Windows Sockets Structures \| Protokoll \_ Info \| dwserviceflags \| XP \_ Bandbreiten \_ Zuordnung")
</dt> </dl>

Das Protokoll verfügt über einen Mechanismus zum Einrichten und Verwalten einer Bandbreite.

</dd> <dt>

**SupportsMulticasting**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32- \_ API \| Windows Sockets Structures \| Protokoll \_ Info \| dwserviceflags \| XP \_ unterstützt \_ Multicast")
</dt> </dl>

Das Protokoll unterstützt Multicasting.

</dd> <dt>

**SupportsQualityofService**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32- \_ API \| Windows Sockets-Strukturen \| wsaprotocol \_ Info \| dwServiceFlags1 \| XP1 \_ QoS \_ unterstützt")
</dt> </dl>

Das Protokoll unterstützt Quality of Service (QoS)-Unterstützung durch den zugrunde liegenden, geschichteten Dienstanbieter oder Transportunternehmen. QoS ist eine Sammlung von-Komponenten, die eine Differenzierung und bevorzugte Behandlung für Teilmengen von Daten ermöglichen, die über das Netzwerk übertragen werden. QoS bedeutet, dass Teilmengen von Daten bei der Durchquerung eines Netzwerks eine höhere Priorität oder einen garantierten Dienst erhalten.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **Win32- \_ networkprotocol** -Klasse wird von [**CIM \_ LogicalElement**](cim-logicalelement.md)abgeleitet.

## <a name="examples"></a>Beispiele

Im folgenden VBScript-Codebeispiel wird veranschaulicht, wie eine Liste der laufenden Dienste aus Instanzen von **Win32 \_ Network Protocol** abgerufen wird.


```VB
Set ProtocolSet = GetObject("winmgmts:").ExecQuery("select * from Win32_NetworkProtocol")

for each Protocol in ProtocolSet
 WScript.Echo Protocol.Name
next
```



Im folgenden perl-Codebeispiel wird veranschaulicht, wie eine Liste der laufenden Dienste aus Instanzen von **Win32 \_ Network Protocol** abgerufen wird.


```
use strict;
use Win32::OLE;

my ( $ProtocolSet, $Protocol );

eval { $ProtocolSet = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2")->
 ExecQuery("SELECT * FROM Win32_NetworkProtocol"); };
unless($@)
{
 print "\n";
 foreach $Protocol (in $ProtocolSet) 
 {
  print $Protocol->{Name}, "\n";
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Cimwin32. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM \_ LogicalElement**](cim-logicalelement.md)
</dt> <dt>

[Betriebssystemklassen](./operating-system-classes.md)
</dt> </dl>

 

 
