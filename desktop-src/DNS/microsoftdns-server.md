---
title: MicrosoftDNS_Server-Klasse
description: Die MicrosoftDNS- \_ Serverklasse beschreibt einen DNS-Server. Jede Instanz dieser Klasse kann mit einer Instanz des MicrosoftDNS \_ -Caches, einer Instanz von MicrosoftDNS \_ -roothints und mehreren Instanzen der MicrosoftDNS-Zone verknüpft werden \_ .
ms.assetid: 768f5f96-d7a5-472f-afe6-63aa9c0e5258
keywords:
- DNS-MicrosoftDNS_Server Klasse
- DNS-MicrosoftDNS_Server Klasse, beschrieben
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
ms.openlocfilehash: 854a90f5b0fa4d331bd0478d104e50dd70b0cd65
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949487"
---
# <a name="microsoftdns_server-class"></a>MicrosoftDNS- \_ Server Klasse

Die **MicrosoftDNS- \_ Server** Klasse beschreibt einen DNS-Server. Jede Instanz dieser Klasse kann mit einer Instanz des [**MicrosoftDNS- \_ Caches**](microsoftdns-cache.md), einer Instanz von [**MicrosoftDNS- \_ roothints**](microsoftdns-roothints.md)und mehreren Instanzen der [**MicrosoftDNS- \_ Zone**](microsoftdns-zone.md)verknüpft werden.

Die folgende Syntax wird durch den MOF-Code vereinfacht.

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

Die **MicrosoftDNS- \_ Server** Klasse verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **MicrosoftDNS- \_ Server** Klasse verfügt über diese Methoden.



| Methode                   | BESCHREIBUNG                                                                      |
|:-------------------------|:---------------------------------------------------------------------------------|
| **Getchilshedname** | Ruft den DNS-Distinguished Name für die Zone ab.<br/>                        |
| **Startscavenging**      | Startet das Bereinigung veralteter Datensätze in den Zonen, die für das Löschen von Daten stehen.<br/> |
| **Start Service**         | Hiermit wird der DNS-Server gestartet.<br/>                                                |
| **Stop Service**          | Beendet den DNS-Server.<br/>                                                 |



 

### <a name="properties"></a>Eigenschaften

Die **MicrosoftDNS- \_ Server** Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Addressbeantworungslimit**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Maximale Anzahl von Host Datensätzen, die als Reaktion auf eine Adress Anforderung zurückgegeben werden. Werte zwischen 5 und 28 sind gültig.

</dd> <dt>

**AllowUpdate**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob der DNS-Server dynamische Update Anforderungen akzeptiert. Gültige Werte sind wie in der folgenden Tabelle dargestellt.



| Wert                                                                                                | Bedeutung                                                                                               |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | Keine Einschränkungen.<br/>                                                                           |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | Lässt keine dynamische Aktualisierung von SOA-Datensätzen zu.<br/>                                             |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Lässt keine dynamischen Updates von NS-Datensätzen am Zonen Stamm zu.<br/>                             |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | Lässt keine dynamischen Updates von NS-Einträgen zu, die sich nicht im Zonen Stamm befinden (Delegierung von NS-Einträgen).<br/> |



 

Addieren Sie diese Werte, um den Einstellungs Wert zu bestimmen.

</dd> <dt>

**Autocacheupdate**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob der DNS-Server versucht, seine Cache Einträge mithilfe von Daten von Stamm Servern zu aktualisieren. Wenn ein DNS-Server gestartet wird, benötigt er eine Liste der "Hinweise" des Stamm Servers und eine Einträge für die Server, die in der Vergangenheit als Cachedatei bezeichnet wurden. Microsoft DNS-Server verfügen über eine Funktion, mit der Sie versuchen können, eine neue Cachedatei auf der Grundlage der Antworten von Stamm Servern zurückzuschreiben.

</dd> <dt>

**Autoconfigfilezones**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, welche standardmäßigen primären Zonen, die für den Namen des DNS-Servers autorisierend sind, aktualisiert werden müssen, wenn der Namen Server geändert wird. Gültige Werte sind:



| Wert                                                                                                | Bedeutung                                                    |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | Keine.<br/>                                           |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | Nur Server, die dynamische Updates zulassen.<br/>        |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Nur Server, die keine dynamischen Updates zulassen.<br/> |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | Alle Server.<br/>                                    |



 

Der Standardwert ist 1.

* * Windows Server 2003: * *

Die Zahl 3 stellt alle Server dar.

</dd> <dt>

**Bindsecon-Datenbanken**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Bestimmt das AXFR-Nachrichtenformat beim Senden an sekundäre DNS-Server-Objekte, die nicht von Microsoft verwendet werden. Wenn diese Einstellung auf "true" festgelegt ist, sendet der DNS-Server Übertragungen an sekundäre DNS-Server-Replikate im nicht komprimierten Format. Bei "false" werden alle Übertragungen im schnellen Format gesendet.

</dd> <dt>

**Bootmethod**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Initialisierungs Methode für den DNS-Server. Gültige Werte werden in der folgenden Tabelle angezeigt.



| Wert                                                                                                | Bedeutung                                      |
|------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | Nicht initialisiert.<br/>                    |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | Starten von einer Datei aus.<br/>                   |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Starten von der Registrierung aus.<br/>               |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | Starten von Verzeichnis und Registrierung.<br/> |



 

</dd> <dt>

**DefaultAgingState**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Der Standardwert für **ScavengingInterval** ist für alle Active Directory integrierten Zonen festgelegt, die auf diesem DNS-Server erstellt wurden. Der Standardwert ist 0 (null), was bedeutet, dass das Bereinigung deaktiviert ist

</dd> <dt>

**DefaultNoRefreshInterval**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Kein Aktualisierungs Intervall (in Stunden) für alle Active Directory integrierten Zonen, die auf diesem DNS-Server erstellt wurden. Der Standardwert ist 168 Stunden (sieben Tage).

</dd> <dt>

**DefaultRefreshInterval**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Aktualisierungs Intervall (in Stunden), das für alle Active Directory integrierten Zonen festgelegt wird, die auf diesem DNS-Server erstellt wurden. Der Standardwert ist 168 Stunden (sieben Tage).

</dd> <dt>

**Disableautoreverversionen**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob der DNS-Server automatisch standardmäßige Reverse-Lookupzonen erstellt.

</dd> <dt>

**Disjoinnetze**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob die Standard Port Bindung für einen Socket, der zum Senden von Abfragen an DNS-Remote Server verwendet wird, überschrieben werden kann.

</dd> <dt>

**Dsavailable**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob auf dem DNS-Server ein verfügbarer DS vorhanden ist.

</dd> <dt>

**Dspollinginterval**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Intervall (in Sekunden) zum Abfragen der in DS integrierten Zonen.

</dd> <dt>

**Dstombstoneinterval**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Lebensdauer von Datensätzen mit tombstoning in den in einem Verzeichnisdienst integrierten Zonen, ausgedrückt in Sekunden.

</dd> <dt>

**EDNSCacheTimeout**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Lebensdauer (in Sekunden) der zwischengespeicherten Informationen, die die von anderen DNS-Servern unterstützte EDNS-Version beschreiben.

</dd> <dt>

**Enabledirectoriypartitions**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob die Unterstützung für Anwendungsverzeichnis Partitionen auf dem DNS-Server aktiviert ist.

* * Windows Server 2003: * *

Diese Methode heißt enabledirectorypartitionsupport.

</dd> <dt>

**EnableDnsSec**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob der DNS-Server DNSSEC-spezifische RRS, Key, SIG und NXT in einer Antwort enthält, die in der folgenden Tabelle aufgeführt sind:



| Wert                                                                                                | Bedeutung                                                                                                                                        |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | In der Antwort sind keine DNSSEC-Einträge enthalten, es sei denn, die Abfrage hat einen Ressourcen Eintrags Satz des DNSSEC-Daten Satz Typs angefordert.<br/>          |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | DNSSEC-Datensätze sind in der Antwort gemäß RFC 2535 enthalten.<br/>                                                                  |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | DNSSEC-Datensätze sind nur in einer Antwort enthalten, wenn die ursprüngliche Client Abfrage den Opt-Ressourcen Daten Satz gemäß RFC 2671 enthielt.<br/> |



 

Wenn eine Abfrage einen Ressourcen Eintrags Satz des DNSSEC-Typs anfordert, antwortet der DNS-Server immer mit solchen Datensätzen, falls verfügbar.

</dd> <dt>

**EnableEDnsProbes**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt das Verhalten des DNS-Servers an. TRUE gibt an, dass der DNS-Server nach RFC 2671 immer mit opt-Ressourcen Einträgen antwortet, es sei denn, der Remote Server hat angegeben, dass EDNS in einem früheren Exchange nicht unterstützt werden. FALSE gibt an, dass der DNS-Server nur dann auf Abfragen mit OPTS antwortet, wenn opts in der ursprünglichen Abfrage gesendet werden.

</dd> <dt>

**EventLogLevel**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, welche Ereignisse der DNS-Server im Ereignisanzeige System Protokoll aufzeichnet. Die folgenden Werte werden verwendet.



| Wert                                                                                                | Bedeutung                                  |
|------------------------------------------------------------------------------------------------------|------------------------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | Keine.<br/>                         |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | Nur Fehler protokollieren.<br/>              |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Protokolliert nur Warnungen und Fehler.<br/> |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | Alle Ereignisse protokollieren.<br/>               |



 

</dd> <dt>

**Weiterleitungen**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob Abfragen an Delegierte Subzonen weitergeleitet werden.

</dd> <dt>

**Weiterleitungen**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Listet die IP-Adressen der Weiterleitungen auf, an die der DNS-Server Abfragen weiterleitet.

</dd> <dt>

**"Forwardingtimeout"**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Die Zeit (in Sekunden), die ein DNS-Server, der eine Abfrage weiterleitet, auf Auflösung von der Weiterleitung wartet [*, bevor versucht*](f-gly.md) wird, die Abfrage selbst aufzulösen.

Dieser Wert ist bedeutungslos, wenn der Weiterleitungsserver nicht für die Verwendung der Rekursion festgelegt ist. Um dies zu ermitteln, überprüfen Sie die Eigenschaft ' isslave ' Boolean.

</dd> <dt>

**Isslave**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

**True** , wenn der DNS-Server keine Rekursion verwendet, wenn die Namensauflösung durch Weiterleitungen fehlschlägt.

</dd> <dt>

**Listenadressen**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Listet die IP-Adressen auf, auf denen der DNS-Server Abfragen empfangen kann.

</dd> <dt>

**Localnetpriority**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob der DNS-Server bei der Rückgabe von Datensätzen Priorität für die lokale Netzwerkadresse erhält.

</dd> <dt>

**LogFileMaxSize**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Größe des DNS-Server-Debugprotokolls in Bytes.

</dd> <dt>

**LogFilePath**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Dateiname und Pfad für das DNS-Server-Debugprotokoll. Der Standardwert ist% System32% \\ DNS \\ DNS. log. Relative Pfade sind relativ zu% systemroot% \\ system32. Absolute Pfade können verwendet werden, UNC-Pfade werden jedoch nicht unterstützt.

</dd> <dt>

**Logipfilterlist**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Liste der IP-Adressen, die zum Filtern von in das Debugprotokoll geschriebenen DNS-Ereignissen verwendet werden.

</dd> <dt>

**LogLevel**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, welche Richtlinien im Ereignisanzeige System Protokoll aktiviert werden.

Sollte auf Grundlage des folgenden Algorithmus auf bestimmte Werte festgelegt werden: für jede Richtlinie (die im Ereignisanzeige System Protokoll aktiviert werden soll) wird ein bestimmter Wert zugewiesen.



| Wert                                                                                                                  | Bedeutung                                             |
|------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl>                   | Such.<br/>                                   |
| <span id="16"></span><dl> <dt>**Uhr**</dt> </dl>                 | Informiert.<br/>                                  |
| <span id="32"></span><dl> <dt>**32**</dt> </dl>                 | Alisierungs.<br/>                                  |
| <span id="254"></span><dl> <dt>**254**</dt> </dl>               | Nicht abgefragt Transaktionen.<br/>                   |
| <span id="256"></span><dl> <dt>**256**</dt> </dl>               | Fragen.<br/>                               |
| <span id="512"></span><dl> <dt>**512**</dt> </dl>               | Beantwortet.<br/>                                 |
| <span id="4096"></span><dl> <dt>**4096**</dt> </dl>             | Send.<br/>                                    |
| <span id="8192"></span><dl> <dt>**8192**</dt> </dl>             | Medizinisch.<br/>                                 |
| <span id="16384"></span><dl> <dt>**16384**</dt> </dl>           | UDP.<br/>                                     |
| <span id="32768"></span><dl> <dt>**32768**</dt> </dl>           | TCP.<br/>                                     |
| <span id="65535"></span><dl> <dt>**65535**</dt> </dl>           | Alle Pakete.<br/>                             |
| <span id="65536"></span><dl> <dt>**65536**</dt> </dl>           | NT-Verzeichnisdienst-Schreib Transaktion.<br/>  |
| <span id="131072"></span><dl> <dt>**131072**</dt> </dl>         | NT-Verzeichnisdienst-Aktualisierungs Transaktion.<br/> |
| <span id="16777216"></span><dl> <dt>**16777216**</dt> </dl>     | Vollständige Pakete.<br/>                            |
| <span id="2147483648"></span><dl> <dt>**2147483648**</dt> </dl> | Schreiben Sie.<br/>                           |



 

Die Summe der Werte, die allen zu aktivierenden Richtlinien entsprechen, wird in dieser Eigenschaft angegeben.

</dd> <dt>

**Looseemwildcarding**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob der DNS-Server lose Platzhalter Vorgänge ausführt. Wenn nicht definiert oder 0 (null), folgt der Server dem in der DNS-RFC angegebenen Platzhalter Verhalten. In diesem Fall wird empfohlen, MX-Einträge für alle Hosts aufzunehmen, die keine e-Mail empfangen können. Wenn der Wert ungleich NULL ist, wird vom Server der nächste Platzhalter Knoten gesucht. in diesem Fall sollte ein Administrator MX-Einträge am Zonen Stamm und in einem Platzhalter Knoten (" \* ") direkt unterhalb des Zonen Stamms ablegen. Administratoren sollten außerdem selbst verweisende MX-Einträge auf Hosts platzieren, die ihre eigene e-Mail erhalten.

</dd> <dt>

**Maxcachettl**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Maximale Zeit in Sekunden, während der der Datensatz einer rekursiven Namensabfrage im DNS-Server Cache verbleiben kann. Der DNS-Server löscht Datensätze aus dem Cache, wenn der Wert dieses Eintrags abläuft, auch wenn der Wert des TTL-Felds im Datensatz größer ist.

Der Standardwert dieser Eigenschaft ist 86.400 Sekunden (1 Tag).

</dd> <dt>

**Maxnegativecachettl**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Die maximale Zeit in Sekunden, die ein Namensfehler Ergebnis einer rekursiven Abfrage im DNS-Server Cache verbleiben kann. DNS löscht Datensätze aus dem Cache, wenn dieser Timer abläuft, auch wenn das TTL-Feld größer ist. Der Standardwert ist 86.400 (ein Tag).

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der voll qualifizierte Domänen Name (FQDN) oder die IP-Adresse des DNS-Servers.

</dd> <dt>

**Namecheckflag**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt den Satz berechtigter Zeichen an, die in DNS-Namen verwendet werden sollen. Die folgenden Werte werden verwendet.



| Wert                                                                                                | Bedeutung                      |
|------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | Strict RFC (ANSI)<br/> |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | Nicht-RFC (ANSI)<br/>    |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | Multibyte (UTF8)<br/>  |



 

* * Windows Server 2003: * *

Der Wert "2" gibt "Any" an.

</dd> <dt>

**NoRecursion**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob der DNS-Server rekursive Suche ausführt. TRUE gibt an, dass rekursive Suchen nicht ausgeführt werden.

</dd> <dt>

**Rekursionretry**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Verstrichene Sekunden vor Wiederholungsversuch für eine rekursive Suche. Wenn die Eigenschaft nicht definiert oder NULL ist, werden nach drei Sekunden Wiederholungs Versuche durchgeführt. Benutzer werden davon abgeraten, diese Eigenschaft zu ändern. Es gibt bestimmte Situationen, in denen die Eigenschaft geändert werden soll. ein Beispiel hierfür ist, wenn der DNS-Server über eine langsame Verbindung mit Remote Servern kontaktiert und der DNS-Server wiederholt wird, bevor die Antwort vom Remote-DNS empfangen wird. In diesem Fall wäre es sinnvoll, den Timeout zu erhöhen, wenn die beobachtete Antwortzeit des Remote-DNS etwas länger ist.

</dd> <dt>

**Recursiontimeout**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Verstrichene Sekunden, bevor der DNS-Server eine rekursive Abfrage ermöglicht. Wenn die Eigenschaft nicht definiert oder NULL ist, gibt der DNS-Server nach 15 Sekunden einen Wert aus. Im Allgemeinen ist das 15-Sekunden-Timeout ausreichend, damit alle ausstehenden Antworten an den DNS-Server zurückgegeben werden können.

Benutzer werden davon abgeraten, diese Eigenschaft zu ändern. Ein Szenario, in dem die Eigenschaft geändert werden sollte, ist, wenn der DNS-Server über eine langsame Verbindung mit Remote Servern kontaktiert wird und der DNS-Server beobachtet wird, dass Abfragen (mit Server \_ Fehlern) abgelehnt werden, bevor Antworten empfangen werden.

Clientresolver wiederholen auch Abfragen, daher ist eine sorgfältige Untersuchung erforderlich, um zu bestimmen, ob Remote Antworten tatsächlich der Abfrage zugeordnet sind, für die ein Timeout aufgetreten ist. In diesem Fall wäre es sinnvoll, den Timeout Wert so zu erhöhen, dass er etwas länger als die beobachtete Antwortzeit des Remote-DNS ist.

</dd> <dt>

**Roundrobin**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob der DNS-Server mehrere A-Einträge aufrundet.

</dd> <dt>

**RpcProtocol**
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

RPC-Protokoll oder-Protokolle, über die administrative RPC ausgeführt werden. Der folgende Algorithmus wird verwendet, um einen bestimmten Wert zuzuweisen:



| Wert                                                                                                | Bedeutung                |
|------------------------------------------------------------------------------------------------------|------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | Keine<br/>        |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | TCP<br/>         |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Named Pipes<br/> |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | LPC<br/>         |



 

Die Summe der Werte gibt die verwendeten Protokolle an.

</dd> <dt>

**ScavengingInterval**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Intervall (in Stunden) zwischen zwei aufeinander folgenden Bereinigung-Vorgängen, die vom DNS-Server ausgeführt werden. NULL gibt an, dass das Bereinigung deaktiviert ist. Der Standardwert ist 168 Stunden (sieben Tage).

</dd> <dt>

**Secureresponses**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob der DNS-Server exklusiv Datensätze in derselben Unterstruktur speichert wie der Server, von dem Sie bereitgestellt wurden.

</dd> <dt>

**SendPort**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Port, an den der DNS-Server UDP-Abfragen an andere Server sendet. Standardmäßig sendet der DNS-Server Abfragen an einen Socket, der an den DNS-Port gebunden ist.

In bestimmten Situationen ist dies nicht die beste Konfiguration. Ein offensichtlicher Fall ist, wenn ein Administrator den DNS-Port mit einer Firewall blockiert, um den externen Zugriff auf den DNS-Server zu verhindern, der Server jedoch weiterhin in der Lage sein soll, eine Verbindung mit den Internet-DNS-Servern aufzunehmen, um die Namensauflösung für interne Clients Ein weiterer Fall ist, wenn der DNS-Server nicht zusammenhängende Netze unterstützt (die Eigenschaft **disjointnets** , die auf true festgelegt ist, identifiziert dieses Szenario). In diesen Fällen weist das Festlegen der **sendonnondnsport** -Eigenschaft auf einen Wert ungleich NULL den DNS-Server an, an einen beliebigen Port für das Senden an Remote-DNS-Server zu binden.

Wenn der **sendonnondnsport** -Wert größer als 1024 ist, bindet der DNS-Server explizit an den angegebenen Portwert. Diese Konfigurationsoption ist nützlich, wenn ein Administrator den DNS-abfrageport zu firewallzwecken korrigieren muss.

* * Windows Server 2003: * *

Das Festlegen der sendport-Eigenschaft auf einen Wert ungleich 0 (null) bewirkt, dass der DNS-Server an einen beliebigen Port zum Senden an Remote-DNS-Server gebunden wird.

</dd> <dt>

**Serveradressen**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Listet die IP-Adressen für den DNS-Server auf.

</dd> <dt>

**Strictfile-paramesing**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob [*Zonendateien*](z-gly.md) vom DNS-Server strikt analysiert werden. Wenn Sie nicht definiert oder NULL ist, protokolliert der Server ungültige Daten in der Zonendatei und ignoriert diese, und die Daten werden weiterhin geladen. Wenn der Wert ungleich NULL ist, protokolliert der Server Fehler bei Zonendateien und schlägt fehl.

</dd> <dt>

**Update Options**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Schränkt den Typ der Datensätze ein, die auf dem Server dynamisch aktualisiert werden können, und wird zusätzlich zu den **AllowUpdate** -Einstellungen auf Server-und Zonen Objekten verwendet.

* * Windows Server 2003: * *

0: keine Einschränkungen.

1: dynamische Updates von SOA-Datensätzen nicht zulassen.

2: lassen Sie keine dynamischen Updates von NS-Datensätzen am Zonen Stamm zu.

4: lassen Sie keine dynamischen Updates von NS-Einträgen zu, die sich nicht im Zonen Stamm befinden (Delegierung NS-Einträge).

Addieren Sie diese Werte, um den Einstellungs Wert zu bestimmen.

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Version des DNS-Servers.

</dd> <dt>

**Schreib Autorität**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob der DNS-Server bei erfolgreicher Antwort NS-und SOA-Einträge in den Autorisierungs Abschnitt schreibt.

</dd> <dt>

**Xfrconnecttimeout**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Die Zeit in Sekunden, während der der DNS-Server auf eine erfolgreiche TCP-Verbindung mit einem Remote Server wartet, wenn eine Zonen Übertragung versucht wird.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| Namespace<br/>                | \\MicrosoftDNS-Stamm<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov. MOF</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Start Service-Methode der MicrosoftDNS- \_ Server Klasse**](microsoftdns-server-startservice.md)
</dt> <dt>

[**Stop Service-Methode der MicrosoftDNS- \_ Server Klasse**](microsoftdns-server-stopservice.md)
</dt> <dt>

[**Startscavenging-Methode der MicrosoftDNS- \_ Server Klasse**](microsoftdns-server-startscavenging.md)
</dt> <dt>

[**Geterkennbar shedname-Methode der MicrosoftDNS- \_ Server Klasse**](microsoftdns-server-getdistinguishedname.md)
</dt> </dl>

 

 





