---
title: MicrosoftDNS_Server-Klasse
description: Die MicrosoftDNS \_ Server-Klasse beschreibt einen DNS-Server. Jede Instanz dieser Klasse kann einer Instanz von MicrosoftDNS \_ Cache, einer Instanz von MicrosoftDNS \_ RootHints und mehreren Instanzen der MicrosoftDNS-Zone zugeordnet \_ werden.
ms.assetid: 768f5f96-d7a5-472f-afe6-63aa9c0e5258
keywords:
- dns der MicrosoftDNS_Server-Klasse
- MicrosoftDNS_Server Dns-Klasse beschrieben
topic_type:
- apiref
api_name:
- MicrosoftDNS_Server
- MicrosoftDNS_Server.StartService
- MicrosoftDNS_Server.StopService
- MicrosoftDNS_Server.StartScavenging
- MicrosoftDNS_Server.GetDistinguishedName
- MicrosoftDNS_Server.Name
- MicrosoftDNS_Server.Version
- MicrosoftDNS_Server.LogLevel
- MicrosoftDNS_Server.LogFilePath
- MicrosoftDNS_Server.LogFileMaxSize
- MicrosoftDNS_Server.LogIPFilterList
- MicrosoftDNS_Server.EventLogLevel
- MicrosoftDNS_Server.RpcProtocol
- MicrosoftDNS_Server.NameCheckFlag
- MicrosoftDNS_Server.AddressAnswerLimit
- MicrosoftDNS_Server.RecursionRetry
- MicrosoftDNS_Server.RecursionTimeout
- MicrosoftDNS_Server.DsPollingInterval
- MicrosoftDNS_Server.DsTombstoneInterval
- MicrosoftDNS_Server.MaxCacheTTL
- MicrosoftDNS_Server.MaxNegativeCacheTTL
- MicrosoftDNS_Server.SendPort
- MicrosoftDNS_Server.XfrConnectTimeout
- MicrosoftDNS_Server.BootMethod
- MicrosoftDNS_Server.AllowUpdate
- MicrosoftDNS_Server.UpdateOptions
- MicrosoftDNS_Server.DsAvailable
- MicrosoftDNS_Server.DisableAutoReverseZones
- MicrosoftDNS_Server.AutoCacheUpdate
- MicrosoftDNS_Server.NoRecursion
- MicrosoftDNS_Server.RoundRobin
- MicrosoftDNS_Server.LocalNetPriority
- MicrosoftDNS_Server.StrictFileParsing
- MicrosoftDNS_Server.LooseWildcarding
- MicrosoftDNS_Server.BindSecondaries
- MicrosoftDNS_Server.WriteAuthorityNS
- MicrosoftDNS_Server.ForwardDelegations
- MicrosoftDNS_Server.SecureResponses
- MicrosoftDNS_Server.DisjointNets
- MicrosoftDNS_Server.AutoConfigFileZones
- MicrosoftDNS_Server.ScavengingInterval
- MicrosoftDNS_Server.DefaultRefreshInterval
- MicrosoftDNS_Server.DefaultNoRefreshInterval
- MicrosoftDNS_Server.DefaultAgingState
- MicrosoftDNS_Server.EDnsCacheTimeout
- MicrosoftDNS_Server.EnableEDnsProbes
- MicrosoftDNS_Server.EnableDnsSec
- MicrosoftDNS_Server.ServerAddresses
- MicrosoftDNS_Server.ListenAddresses
- MicrosoftDNS_Server.Forwarders
- MicrosoftDNS_Server.ForwardingTimeout
- MicrosoftDNS_Server.IsSlave
- MicrosoftDNS_Server.EnableDirectoryPartitions
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c4a42432a11b5cde0df657ba2a9725a68d76a055fce3787bce56c10dfd227ff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119539270"
---
# <a name="microsoftdns_server-class"></a>\_MicrosoftDNS-Serverklasse

Die **MicrosoftDNS \_ Server-Klasse** beschreibt einen DNS-Server. Jede Instanz dieser Klasse kann einer Instanz von [**MicrosoftDNS \_ Cache,**](microsoftdns-cache.md)einer Instanz von [**MicrosoftDNS \_ RootHints**](microsoftdns-roothints.md)und mehreren Instanzen der [**MicrosoftDNS-Zone \_**](microsoftdns-zone.md)zugeordnet werden.

Die folgende Syntax wird durch einen MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
class MicrosoftDNS_Server : CIM_Service
{
  string  Name;
  uint32  Version;
  uint32  LogLevel;
  string  LogFilePath;
  uint32  LogFileMaxSize;
  string  LogIPFilterList[];
  uint32  EventLogLevel;
  sint32  RpcProtocol;
  uint32  NameCheckFlag;
  uint32  AddressAnswerLimit;
  uint32  RecursionRetry;
  uint32  RecursionTimeout;
  uint32  DsPollingInterval;
  uint32  DsTombstoneInterval;
  uint32  MaxCacheTTL;
  uint32  MaxNegativeCacheTTL;
  uint32  SendPort;
  uint32  XfrConnectTimeout;
  uint32  BootMethod;
  uint32  AllowUpdate;
  uint32  UpdateOptions;
  boolean DsAvailable;
  boolean DisableAutoReverseZones;
  boolean AutoCacheUpdate;
  boolean NoRecursion;
  boolean RoundRobin;
  boolean LocalNetPriority;
  boolean StrictFileParsing;
  boolean LooseWildcarding;
  boolean BindSecondaries;
  boolean WriteAuthorityNS;
  uint32  ForwardDelegations;
  boolean SecureResponses;
  boolean DisjointNets;
  uint32  AutoConfigFileZones;
  uint32  ScavengingInterval;
  uint32  DefaultRefreshInterval;
  uint32  DefaultNoRefreshInterval;
  boolean DefaultAgingState;
  uint32  EDnsCacheTimeout;
  boolean EnableEDnsProbes;
  uint32  EnableDnsSec;
  string  ServerAddresses[];
  string  ListenAddresses[];
  string  Forwarders[];
  uint32  ForwardingTimeout;
  boolean IsSlave;
  boolean EnableDirectoryPartitions;
};
```

## <a name="members"></a>Member

Die **MicrosoftDNS \_ Server-Klasse** verfügt über folgende Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **MicrosoftDNS \_ Server-Klasse** verfügt über diese Methoden.



| Methode                   | Beschreibung                                                                      |
|:-------------------------|:---------------------------------------------------------------------------------|
| **GetDistinguishedName** | Ruft den DNS-Distinguished Name für die Zone ab.<br/>                        |
| **StartScavenging**      | Beginnt mit dem Aufräumen veralteter Datensätze in den Zonen, die der Kapselung unterliegen.<br/> |
| **Startservice**         | Startet den DNS-Server.<br/>                                                |
| **StopService**          | Beendet den DNS-Server.<br/>                                                 |



 

### <a name="properties"></a>Eigenschaften

Die **\_ MicrosoftDNS-Serverklasse** verfügt über diese Eigenschaften.

<dl> <dt>

**AddressAnswerLimit**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Maximale Anzahl von Hostdatensätzen, die als Antwort auf eine Adressanforderung zurückgegeben werden. Werte zwischen 5 und 28 sind gültig.

</dd> <dt>

**AllowUpdate**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob der DNS-Server dynamische Updateanforderungen akzeptiert. Gültige Werte sind wie in der folgenden Tabelle dargestellt.



| Wert                                                                                                | Bedeutung                                                                                               |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | Keine Einschränkungen.<br/>                                                                           |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | Dynamische Updates von SOA-Datensätzen sind nicht zulässig.<br/>                                             |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Dynamische Updates von NS-Einträgen im Zonenstamm sind nicht zulässig.<br/>                             |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | Dynamische Updates von NS-Einträgen, die sich nicht im Zonenstamm befinden (Delegierungs-NS-Einträge), sind nicht zulässig.<br/> |



 

Addieren Sie diese Werte, um den Einstellungswert zu bestimmen.

</dd> <dt>

**AutoCacheUpdate**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob der DNS-Server versucht, seine Cacheeinträge mithilfe von Daten von Stammservern zu aktualisieren. Wenn ein DNS-Server gestartet wird, benötigt er eine Liste der Stammserverhinweise NS- und A-Einträge für die Server, die in der Vergangenheit als Cachedatei bezeichnet wurden. Microsoft DNS-Server verfügen über ein Feature, mit dem sie versuchen können, basierend auf den Antworten von Stammservern eine neue Cachedatei zurückzuschreiben.

</dd> <dt>

**AutoConfigFileZones**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, welche primären Standardzonen, die für den Namen des DNS-Servers autoritativ sind, aktualisiert werden müssen, wenn sich der Namenserver ändert. Gültige Werte sind:



| Wert                                                                                                | Bedeutung                                                    |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | Keine.<br/>                                           |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | Nur Server, die dynamische Updates zulassen.<br/>        |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Nur Server, die keine dynamischen Updates zulassen.<br/> |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | Alle Server.<br/>                                    |



 

Der Standardwert ist 1.

**Windows Server 2003: **

Die Zahl 3 steht für Alle Server.

</dd> <dt>

**BindSecondaries**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Bestimmt das AXFR-Nachrichtenformat beim Senden an Nicht-Microsoft DNS Server-Secondaries. Wenn diese Einstellung auf TRUE festgelegt ist, sendet der DNS-Server Übertragungen an Nicht-Microsoft DNS Server-Secondaries im nicht komprimierten Format. False gibt an, dass alle Übertragungen im schnellen Format gesendet werden.

</dd> <dt>

**BootMethod**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Initialisierungsmethode für den DNS-Server. Gültige Werte werden in der folgenden Tabelle angezeigt.



| Wert                                                                                                | Bedeutung                                      |
|------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | Nicht initialisiert.<br/>                    |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | Starten sie aus der Datei.<br/>                   |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Starten sie aus der Registrierung.<br/>               |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | Starten Sie über das Verzeichnis und die Registrierung.<br/> |



 

</dd> <dt>

**DefaultAgingState**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Der **ScavengingInterval-Standardwert** wird für alle active Directory-integrierten Zonen festgelegt, die auf diesem DNS-Server erstellt wurden. Der Standardwert ist 0 (null), was angibt, dass die Kapselung deaktiviert ist.

</dd> <dt>

**DefaultNoRefreshInterval**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Das Aktualisierungsintervall in Stunden wird für alle active Directory-integrierten Zonen festgelegt, die auf diesem DNS-Server erstellt wurden. Der Standardwert ist 168 Stunden (sieben Tage).

</dd> <dt>

**DefaultRefreshInterval**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Aktualisierungsintervall in Stunden für alle active Directory-integrierten Zonen festgelegt, die auf diesem DNS-Server erstellt wurden. Der Standardwert ist 168 Stunden (sieben Tage).

</dd> <dt>

**DisableAutoReverseZones**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob der DNS-Server automatisch Standardmäßige Reverse-Look up-Zonen erstellt.

</dd> <dt>

**DisjointNets**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob die Standardportbindung für einen Socket, der zum Senden von Abfragen an DNS-Remoteserver verwendet wird, überschrieben werden kann.

</dd> <dt>

**DsAvailable**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob ein DS auf dem DNS-Server verfügbar ist.

</dd> <dt>

**DsPollingInterval**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Intervall in Sekunden zum Abfragen der in DS integrierten Zonen.

</dd> <dt>

**DsTombstoneInterval**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Lebensdauer von tombstoned-Datensätzen in verzeichnisdienstintegrierten Zonen, ausgedrückt in Sekunden.

</dd> <dt>

**EDnsCacheTimeout**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Lebensdauer der zwischengespeicherten Informationen in Sekunden, die die von anderen DNS-Servern unterstützte EDNS-Version beschreiben.

</dd> <dt>

**EnableDirectoryPartitions**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob die Unterstützung für Anwendungsverzeichnispartitionen auf dem DNS-Server aktiviert ist.

**Windows Server 2003: **

Diese Methode heißt EnableDirectoryPartitionSupport.

</dd> <dt>

**EnableDnsSec**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob der DNS-Server DNSSEC-spezifische RRs, KEY, SIG und NXT in einer Antwort gemäß der folgenden Tabelle enthält:



| Wert                                                                                                | Bedeutung                                                                                                                                        |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | In der Antwort sind keine DNSSEC-Einträge enthalten, es sei denn, die Abfrage hat einen Ressourceneintragssatz des DNSSEC-Eintragstyps angefordert.<br/>          |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | DNSSEC-Einträge sind gemäß RFC 2535 in der Antwort enthalten.<br/>                                                                  |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | DNSSEC-Einträge sind nur dann in einer Antwort enthalten, wenn die ursprüngliche Clientabfrage den OPT-Ressourceneintrag gemäß RFC 2671 enthielt.<br/> |



 

Wenn eine Abfrage einen Ressourceneintragssatz vom Typ DNSSEC anfordert, antwortet der DNS-Server immer mit solchen Einträgen, sofern verfügbar.

</dd> <dt>

**EnableEDnsProbes**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt das Verhalten des DNS-Servers an. Bei TRUE antwortet der DNS-Server immer mit OPT-Ressourceneinträgen gemäß RFC 2671, es sei denn, der Remoteserver hat angegeben, dass er EDNS in einem früheren Austausch nicht unterstützt. False gibt an, dass der DNS-Server nur dann auf Abfragen mit OPTs antwortet, wenn OPTs in der ursprünglichen Abfrage gesendet werden.

</dd> <dt>

**EventLogLevel**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, welche Ereignisse der DNS-Server im Ereignisanzeige Systemprotokoll aufzeichnet. Die folgenden Werte werden verwendet.



| Wert                                                                                                | Bedeutung                                  |
|------------------------------------------------------------------------------------------------------|------------------------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | Keine.<br/>                         |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | Protokollieren Sie nur Fehler.<br/>              |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Protokollieren Sie nur Warnungen und Fehler.<br/> |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | Protokollieren Sie alle Ereignisse.<br/>               |



 

</dd> <dt>

**ForwardDelegations**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob Abfragen an delegierte Unterzonen weitergeleitet werden.

</dd> <dt>

**Weiterleitungen**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Listet die IP-Adressen der Weiterleitungen auf, an die der DNS-Server Abfragen weiterleitet.

</dd> <dt>

**ForwardingTimeout**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Die Zeit in Sekunden, in der ein DNS-Server, der eine Abfrage weiterleiten kann, auf die Auflösung der [*Weiterleitung*](f-gly.md) wartet, bevor versucht wird, die Abfrage selbst aufzulösen.

Dieser Wert ist bedeutungslos, wenn der Weiterleitungsserver nicht für die Verwendung der Rekursion festgelegt ist. Überprüfen Sie die boolesche IsSlave-Eigenschaft, um dies zu ermitteln.

</dd> <dt>

**IsSlave**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

**TRUE,** wenn der DNS-Server keine Rekursion verwendet, wenn die Namensauflösung über Weiterleitungen fehlschlägt.

</dd> <dt>

**ListenAddresses**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Listet die IP-Adressen auf, für die der DNS-Server Abfragen empfangen kann.

</dd> <dt>

**LocalNetPriority**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob der DNS-Server der lokalen Netzwerkadresse prioritätiert, wenn A-Einträge zurückgegeben werden.

</dd> <dt>

**LogFileMaxSize**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Größe des DNS-Serverdebuggingprotokolls in Bytes.

</dd> <dt>

**Logfilepath**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Dateiname und Pfad für das DNS-Serverdebuggingprotokoll. Der Standardwert ist %system32% \\ dns \\ dns.log. Relative Pfade sind relativ zu %Systemroot% \\ System32. Absolute Pfade können verwendet werden, ABER UNC-Pfade werden nicht unterstützt.

</dd> <dt>

**LogIPFilterList**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Liste der IP-Adressen, die zum Filtern von DNS-Ereignissen verwendet werden, die in das Debugprotokoll geschrieben wurden.

</dd> <dt>

**LogLevel**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, welche Richtlinien im Ereignisanzeige Systemprotokoll aktiviert werden.

Sollte basierend auf dem folgenden Algorithmus auf bestimmte Werte festgelegt werden: Jeder Richtlinie (die im Ereignisanzeige Systemprotokoll aktiviert werden soll) wird ein bestimmter Wert zugewiesen.



| Wert                                                                                                                  | Bedeutung                                             |
|------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl>                   | Abfrage.<br/>                                   |
| <span id="16"></span><dl> <dt>**16**</dt> </dl>                 | Benachrichtigen.<br/>                                  |
| <span id="32"></span><dl> <dt>**32**</dt> </dl>                 | aktualisieren.<br/>                                  |
| <span id="254"></span><dl> <dt>**254**</dt> </dl>               | Nichtabfragetransaktionen.<br/>                   |
| <span id="256"></span><dl> <dt>**256**</dt> </dl>               | Fragen.<br/>                               |
| <span id="512"></span><dl> <dt>**512**</dt> </dl>               | Antworten.<br/>                                 |
| <span id="4096"></span><dl> <dt>**4096**</dt> </dl>             | Send.<br/>                                    |
| <span id="8192"></span><dl> <dt>**8192**</dt> </dl>             | Erhalten.<br/>                                 |
| <span id="16384"></span><dl> <dt>**16384**</dt> </dl>           | Udp.<br/>                                     |
| <span id="32768"></span><dl> <dt>**32768**</dt> </dl>           | TCP.<br/>                                     |
| <span id="65535"></span><dl> <dt>**65535**</dt> </dl>           | Alle Pakete.<br/>                             |
| <span id="65536"></span><dl> <dt>**65536**</dt> </dl>           | NT Directory Service-Schreibtransaktion.<br/>  |
| <span id="131072"></span><dl> <dt>**131072**</dt> </dl>         | NT Directory Service-Updatetransaktion.<br/> |
| <span id="16777216"></span><dl> <dt>**16777216**</dt> </dl>     | Vollständige Pakete.<br/>                            |
| <span id="2147483648"></span><dl> <dt>**2147483648**</dt> </dl> | Schreiben sie durch.<br/>                           |



 

Die Summe der Werte, die allen zu aktivierenden Richtlinien entsprechen, wird in dieser Eigenschaft angegeben.

</dd> <dt>

**LooseWildcarding**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob der DNS-Server lose Platzhalter ausführt. Wenn nicht definiert oder 0 (null), folgt der Server dem in der DNS RFC angegebenen Platzhalterverhalten. In diesem Fall wird einem Administrator empfohlen, MX-Einträge für alle Hosts einzuschließen, die keine E-Mails empfangen können. Wenn der Wert ungleich 0 (null) ist, sucht der Server den nächstgelegenen Platzhalterknoten. In diesem Fall sollte ein Administrator MX-Einträge im Zonenstamm und in einem Platzhalterknoten \* ("") direkt unterhalb des Zonenstamms speichern. Außerdem sollten Administratoren selbstverweisende MX-Einträge auf Hosts setzen, die ihre eigenen E-Mails empfangen.

</dd> <dt>

**MaxCacheTTL**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Die maximale Zeit (in Sekunden) kann der Datensatz einer rekursiven Namensabfrage im DNS-Servercache verbleiben. Der DNS-Server löscht Datensätze aus dem Cache, wenn der Wert dieses Eintrags abläuft, auch wenn der Wert des TTL-Felds im Datensatz größer ist.

Der Standardwert dieser Eigenschaft ist 86.400 Sekunden (1 Tag).

</dd> <dt>

**MaxNegativeCacheTTL**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Die maximale Zeit in Sekunden, die ein Namensfehler aufgrund einer rekursiven Abfrage verursacht, kann im DNS-Servercache verbleiben. DNS löscht Datensätze aus dem Cache, wenn dieser Timer abläuft, auch wenn das TTL-Feld größer ist. Der Standardwert ist 86.400 (ein Tag).

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Vollqualifizierte Domänennamen (Fully Qualified Domain Name, FQDN) oder IP-Adresse des DNS-Servers.

</dd> <dt>

**NameCheckFlag**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt den Satz berechtigter Zeichen an, die in DNS-Namen verwendet werden sollen. Die folgenden Werte werden verwendet.



| Wert                                                                                                | Bedeutung                      |
|------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | Strict RFC (ANSI)<br/> |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | Nicht-RFC (ANSI)<br/>    |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | Multibyte (UTF8)<br/>  |



 

**Windows Server 2003: **

Der Wert "2" gibt "Any" an.

</dd> <dt>

**NoRecursion**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob der DNS-Server rekursive Suchläufe ausführt. TRUE gibt an, dass rekursive Suchläufe nicht ausgeführt werden.

</dd> <dt>

**RekursionRetry**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Verstrichene Sekunden, bevor eine rekursive Suche wiederholt wird. Wenn die Eigenschaft nicht definiert oder 0 (null) ist, werden nach drei Sekunden Erneutentitäten vorgenommen. Benutzer werden davon abgeraten, diese Eigenschaft zu ändern. Es gibt bestimmte Situationen, in denen die Eigenschaft geändert werden soll. Ein Beispiel ist, wenn der DNS-Server Remoteserver über eine langsame Verbindung kontaktiert und der DNS-Server einen Wiederholungsversuch vor dem Empfang der Antwort vom Remote-DNS vorn durchfing. In diesem Fall wäre es sinnvoll, das Time out auf einen etwas längeren Zeitraum als die beobachtete Antwortzeit vom Remote-DNS aus zu erhöhen.

</dd> <dt>

**RecursionTimeout**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Verstrichene Sekunden, bevor der DNS-Server eine rekursive Abfrage aufgibt. Wenn die Eigenschaft nicht definiert oder 0 (null) ist, gibt der DNS-Server nach 15 Sekunden auf. Im Allgemeinen reicht das 15-Sekunden-Time out aus, damit alle ausstehenden Antworten wieder an den DNS-Server gesendet werden können.

Benutzer werden davon abgeraten, diese Eigenschaft zu ändern. Ein Szenario, in dem die -Eigenschaft geändert werden sollte, ist, wenn der DNS-Server Remoteserver über eine langsame Verbindung kontaktiert und der DNS-Server beobachtet wird, dass Abfragen (mit SERVERFEHLER) abgelehnt werden, bevor Antworten empfangen \_ werden.

Client-Resolver wiederholen auch Abfragen, daher ist eine sorgfältige Untersuchung erforderlich, um zu ermitteln, ob Remoteantworten tatsächlich mit der Abfrage verknüpft sind, bei der ein Time out auft ist. In diesem Fall wäre es sinnvoll, den Time out-Wert so zu erhöhen, dass er etwas länger als die beobachtete Antwortzeit vom Remote-DNS ist.

</dd> <dt>

**RoundRobin**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob der DNS-Server mehrere A-Einträge roundrobiniert.

</dd> <dt>

**RpcProtocol**
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

RPC-Protokoll oder -Protokolle, über die der administrative RPC ausgeführt wird. Der folgende Algorithmus wird verwendet, um einen bestimmten Wert zu zuweisen:



| Wert                                                                                                | Bedeutung                |
|------------------------------------------------------------------------------------------------------|------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | Keine<br/>        |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | TCP<br/>         |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Named Pipes<br/> |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | Lpc<br/>         |



 

Die Summe der Werte gibt die verwendeten Protokolle an.

</dd> <dt>

**ScavengingInterval**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Intervall in Stunden zwischen zwei aufeinanderfolgenden Besendungsvorgängen, die vom DNS-Server ausgeführt werden. 0 (null) gibt an, dass die Besenkung deaktiviert ist. Der Standardwert ist 168 Stunden (sieben Tage).

</dd> <dt>

**SecureResponses**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob der DNS-Server ausschließlich Einträge mit Namen in derselben Unterstruktur speichert wie der Server, der sie bereitgestellt hat.

</dd> <dt>

**SendPort**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Port, an dem der DNS-Server UDP-Abfragen an andere Server sendet. Standardmäßig sendet der DNS-Server Abfragen an einen Socket, der an den DNS-Port gebunden ist.

In bestimmten Situationen ist dies nicht die beste Konfiguration. Ein offensichtlicher Fall ist, wenn ein Administrator den DNS-Port mit einer Firewall blockiert, um externen Zugriff auf den DNS-Server zu verhindern, aber dennoch möchte, dass der Server Internet-DNS-Server kontaktieren kann, um eine Namensauflösung für interne Clients zu ermöglichen. Ein weiterer Fall ist, wenn der DNS-Server disjoint-Nets unterstützt (die Eigenschaft **DisjointNets,** die auf TRUE festgelegt ist, identifiziert dieses Szenario). In diesen Fällen wird der DNS-Server durch Festlegen der **SendOnNonDnsPort-Eigenschaft** auf einen Wert ungleich 0 (null) an einen beliebigen Port zum Senden an DNS-Remoteserver gebunden.

Wenn der **SendOnNonDnsPort-Wert** größer als 1024 ist, wird der DNS-Server explizit an den angegebenen Portwert gebunden. Diese Konfigurationsoption ist nützlich, wenn ein Administrator den DNS-Abfrageport für Firewallzwecke korrigieren muss.

**Windows Server 2003: **

Das Festlegen der SendPort-Eigenschaft auf einen Wert von nicht 0 (null) bewirkt, dass der DNS-Server eine Bindung an einen beliebigen Port zum Senden an DNS-Remoteserver erstellt.

</dd> <dt>

**ServerAddresses**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Listet die IP-Adressen für den DNS-Server auf.

</dd> <dt>

**StrictFileParsing**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob der DNS-Server [*Zonendateien streng*](z-gly.md) analysiert. Wenn nicht definiert oder 0 (null) ist, protokolliert und ignoriert der Server fehlerhafte Daten in der Zonendatei und wird weiterhin geladen. Wenn nicht 0 (null) ist, protokolliert der Server Zonendateifehler und kann nicht ausgeführt werden.

</dd> <dt>

**UpdateOptions**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Schränkt den Typ der Datensätze ein, die auf dem Server dynamisch aktualisiert werden können und zusätzlich zu den **AllowUpdate-Einstellungen** für Server- und Zonenobjekte verwendet werden.

**Windows Server 2003: **

0: Keine Einschränkungen.

1: Dynamische Updates von SOA-Datensätzen nicht zulassen.

2: Dynamische Updates von NS-Einträgen im Zonenstamm nicht zulassen.

4: Dynamische Updates von NS-Einträgen, die sich nicht im Zonenstamm befinden, nicht zulassen (Delegierung von NS-Einträgen).

Summiert diese Werte, um den Einstellungswert zu bestimmen.

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Version des DNS-Servers.

</dd> <dt>

**WriteAuthorityNS**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob der DNS-Server bei erfolgreicher Antwort NS- und SOA-Einträge in den Autoritätsabschnitt schreibt.

</dd> <dt>

**XfrConnectTimeout**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Die Zeit in Sekunden, die der DNS-Server beim Versuch einer Zonenübertragung auf eine erfolgreiche TCP-Verbindung mit einem Remoteserver wartet.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| Namespace<br/>                | \\MicrosoftDNS-Stamm<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov.mof</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**StartService-Methode der \_ MicrosoftDNS-Serverklasse**](microsoftdns-server-startservice.md)
</dt> <dt>

[**StopService-Methode der \_ MicrosoftDNS-Serverklasse**](microsoftdns-server-stopservice.md)
</dt> <dt>

[**StartScavenging-Methode der \_ MicrosoftDNS-Serverklasse**](microsoftdns-server-startscavenging.md)
</dt> <dt>

[**GetDistinguishedName-Methode der \_ MicrosoftDNS-Serverklasse**](microsoftdns-server-getdistinguishedname.md)
</dt> </dl>

 

 





