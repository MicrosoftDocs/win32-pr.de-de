---
title: MicrosoftDNS_Zone-Klasse
description: Die MicrosoftDNS \_ Zone-Klasse beschreibt eine DNS-Zone. Jede Instanz der \_ MicrosoftDNS-Zonenklasse muss genau einem DNS-Server zugewiesen werden. Zonen können mehreren Instanzen der \_ MicrosoftDNS-Domänen- oder \_ MicrosoftDNS-Ressourcenrecord-Klassen zugeordnet werden.
ms.assetid: 9c59fa61-cca5-4718-ad40-8d2c6ed5fc2d
keywords:
- MicrosoftDNS_Zone-Klasse DNS
- MicrosoftDNS_Zone DNS-Klasse beschrieben
topic_type:
- apiref
api_name:
- MicrosoftDNS_Zone
- MicrosoftDNS_Zone.PauseZone
- MicrosoftDNS_Zone.ResumeZone
- MicrosoftDNS_Zone.ReloadZone
- MicrosoftDNS_Zone.ForceRefresh
- MicrosoftDNS_Zone.UpdateFromDS
- MicrosoftDNS_Zone.WriteBackZone
- MicrosoftDNS_Zone.AgeAllRecords
- MicrosoftDNS_Zone.CreateZone
- MicrosoftDNS_Zone.ChangeZoneType
- MicrosoftDNS_Zone.ResetSecondaries
- MicrosoftDNS_Zone.GetDistinguishedName
- MicrosoftDNS_Zone.ZoneType
- MicrosoftDNS_Zone.DsIntegrated
- MicrosoftDNS_Zone.AllowUpdate
- MicrosoftDNS_Zone.DataFile
- MicrosoftDNS_Zone.DisableWINSRecordReplication
- MicrosoftDNS_Zone.Notify
- MicrosoftDNS_Zone.SecureSecondaries
- MicrosoftDNS_Zone.Paused
- MicrosoftDNS_Zone.Shutdown
- MicrosoftDNS_Zone.Reverse
- MicrosoftDNS_Zone.AutoCreated
- MicrosoftDNS_Zone.UseWins
- MicrosoftDNS_Zone.UseNBStat
- MicrosoftDNS_Zone.Aging
- MicrosoftDNS_Zone.RefreshInterval
- MicrosoftDNS_Zone.NoRefreshInterval
- MicrosoftDNS_Zone.AvailForScavengeTime
- MicrosoftDNS_Zone.MasterServers
- MicrosoftDNS_Zone.LocalMasterServers
- MicrosoftDNS_Zone.ScavengeServers
- MicrosoftDNS_Zone.SecondaryServers
- MicrosoftDNS_Zone.NotifyServers
- MicrosoftDNS_Zone.ForwarderTimeout
- MicrosoftDNS_Zone.ForwarderSlave
- MicrosoftDNS_Zone.LastSuccessfulSoaCheck
- MicrosoftDNS_Zone.LastSuccessfulXfr
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a37b8c99fcd0fb70206758dd67dab8cfffe145ea2ef1aa75186b1268a7ff3b63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957179"
---
# <a name="microsoftdns_zone-class"></a>MicrosoftDNS \_ Zone-Klasse

> [!NOTE]
> Dieser Artikel enthält Verweise auf den Begriff Slave, einen Begriff, den Microsoft nicht mehr verwendet. Sobald der Begriff aus der Software entfernt wird, wird er auch aus diesem Artikel entfernt.

> [!NOTE]
> Dieser Artikel enthält Verweise auf den Begriff Masterserver, einen Begriff, den Microsoft nicht mehr verwendet. Sobald der Begriff aus der Software entfernt wird, wird er auch aus diesem Artikel entfernt.

Die **\_ MicrosoftDNS-Zone-Klasse** beschreibt eine DNS-Zone. Jede Instanz der **MicrosoftDNS-Zonenklasse \_** muss genau einem DNS-Server zugewiesen werden. Zonen können mehreren Instanzen der [**MicrosoftDNS-Domänen- \_**](microsoftdns-domain.md) oder [**MicrosoftDNS-Ressourcenrecord-Klassen \_**](microsoftdns-resourcerecord.md) zugeordnet werden.

Die folgende Syntax wird durch einen MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
class MicrosoftDNS_Zone : MicrosoftDNS_Domain
{
  uint32  ZoneType;
  boolean DsIntegrated;
  uint32  AllowUpdate;
  string  DataFile;
  boolean DisableWINSRecordReplication;
  uint32  Notify;
  uint32  SecureSecondaries;
  boolean Paused;
  boolean Shutdown;
  boolean Reverse;
  boolean AutoCreated;
  boolean UseWins;
  boolean UseNBStat;
  boolean Aging;
  uint32  RefreshInterval;
  uint32  NoRefreshInterval;
  uint32  AvailForScavengeTime;
  string  MasterServers[];
  string  LocalMasterServers[];
  string  ScavengeServers[];
  string  SecondaryServers[];
  string  NotifyServers[];
  uint32  ForwarderTimeout;
  boolean ForwarderSlave;
  uint32  LastSuccessfulSoaCheck;
  uint32  LastSuccessfulXfr;
};
```

## <a name="members"></a>Member

Die **MicrosoftDNS \_ Zone-Klasse** verfügt über folgende Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **MicrosoftDNS \_ Zone-Klasse** verfügt über diese Methoden.



| Methode                   | BESCHREIBUNG                                                                                                                                                                                                |
|:-------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **AgeAllRecords**        | Aktiviert das Altern für einige oder alle Nicht-NS- und Nicht-SOA-Datensätze.<br/>                                                                                                                                       |
| **ChangeZoneType**       | Ändert Zonentypen. <br/> Qualifizierer: Implementiert<br/>                                                                                                                                         |
| **CreateZone**           | Erstellt eine neue Zone. <br/> Qualifizierer: Keine.<br/>                                                                                                                                               |
| **ForceRefresh**         | Erzwingt ein Update der sekundären Vom Master-DNS-Server. <br/> Qualifizierer: Implementiert<br/>                                                                                               |
| **GetDistinguishedName** | Ruft den DS-Distinguished Name für die Zone ab. <br/> Qualifizierer: Implementiert<br/>                                                                                                                 |
| **PauseZone**            | Hält die Zone an. <br/> Qualifizierer: Implementiert<br/>                                                                                                                                            |
| **ReloadZone**           | Lädt die Zone erneut. <br/> Qualifizierer: Implementiert<br/>                                                                                                                                           |
| **ResetSecondaries**     | Setzt das sekundäre IP-Adressarray zurück. <br/> Qualifizierer: Implementiert<br/>                                                                                                                      |
| **ResumeZone**           | Setzt die Zone fort. <br/> Qualifizierer: Implementiert<br/>                                                                                                                                           |
| **UpdateFromDS**         | Erzwingt eine Aktualisierung der Zone vom Verzeichnisdienst (Directory Service, DS). Damit diese Methode gültig ist, muss ZoneType 0 sein, die Zone muss tatsächlich im DS gespeichert werden. <br/> Qualifizierer: Implementiert<br/> |
| **WriteBackZone**        | Speichert Zonendaten in der Zonendatei. <br/> Qualifizierer: Implementiert, statisch<br/>                                                                                                                   |



 

### <a name="properties"></a>Eigenschaften

Die **MicrosoftDNS \_ Zone-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Alterung**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt das Altern und Löschverhalten der Zone an. 0 (null) gibt an, dass die Kapselung deaktiviert ist. Wenn die Kapselung deaktiviert ist, werden die Zeitstempel von Datensätzen in der Zone nicht aktualisiert, und die Datensätze werden nicht gespeichert. Wenn diese Einstellung auf 1 festgelegt ist, werden Datensätze gespeichert, und ihre Zeitstempel werden aktualisiert, wenn der Server die dynamische Updateanforderung für die Datensätze empfängt. Für in Active Directory integrierte Zonen wird dieser Wert auf die *DefaultAgingState-Eigenschaft* des DNS-Servers festgelegt, auf dem die Zone erstellt wird. Für primäre Standardzonen ist der Standardwert 0 (null).

</dd> <dt>

**AllowUpdate**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die Zone dynamische Updateanforderungen akzeptiert.

</dd> <dt>

**AutoCreated**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die Zone automatisch generiert wird.

</dd> <dt>

**AvailForScavengeTime**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt den Zeitpunkt an, zu dem der Server versuchen kann, die Zone zu speichern. Selbst wenn die Zone so konfiguriert ist, dass die Kapselung aktiviert ist, versucht der DNS-Server erst nach diesem Moment, diese Zone zu speichern. Dieser Wert wird auf die aktuelle Zeit plus das Aktualisierungsintervall der Zone festgelegt, wenn die Zone geladen wird. Dieser Parameter wird lokal gespeichert und nicht in andere Kopien der Zone repliziert.

</dd> <dt>

**Datafile**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt den Namen der Zonendatei an.

</dd> <dt>

**DisableWINSRecordReplication**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob der WINS-Eintrag repliziert wird. Wenn diese Einstellung auf TRUE festgelegt ist, ist die WINS-Datensatzreplikation deaktiviert.

</dd> <dt>

**DsIntegrated**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die Zone in DS integriert ist.

</dd> <dt>

**ForwarderSlave**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob das DNS beim Auflösen der Namen für die angegebene Forwardzone eine Rekursion verwendet. Gilt nur für Zonen mit bedingter Weiterleitung.

</dd> <dt>

**ForwarderTimeout**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt die Zeit in Sekunden an, die ein DNS-Server, der eine Abfrage für den Namen unter der Forwardzone weiterleitet, auf die Auflösung von der Weiterleitung wartet, bevor versucht wird, die Abfrage selbst aufzulösen. Dieser Parameter gilt nur für Forward-Zonen.

</dd> <dt>

**LastSuccessfulSoaCheck**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Anzahl der Sekunden seit Dem 1. Januar 1970 GMT seit der letzten Überprüfung der SOA-Seriennummer für die Zone.

</dd> <dt>

**LastSuccessfulXfr**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Anzahl der Sekunden seit Dem 1. Januar 1970 GMT seit der letzten Übertragung der Zone von einem Masterserver.

</dd> <dt>

**LocalMasterServers**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Lokale IP-Adressen der DNS-Masterserver für diese Zone. Wenn diese Einstellung festgelegt ist, überfahren diese Masterserver die in Active Directory gefundenen MasterServer.

</dd> <dt>

**MasterServer**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

IP-Adressen der MASTER-DNS-Server für diese Zone.

</dd> <dt>

**NoRefreshInterval**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt das Zeitintervall zwischen der letzten Aktualisierung des Zeitstempels eines Datensatzes und dem frühesten Zeitpunkt an, zu dem der Zeitstempel aktualisiert werden kann.

</dd> <dt>

**Benachrichtigen**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die Masterzone die zweiten Datenbanken über Änderungen in ihrer RRs-Datenbank benachrichtigt. Legen Sie auf 1 fest, um die zweiten Binärdateien zu benachrichtigen.

</dd> <dt>

**NotifyServers**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Array von Zeichenfolgen, die IP-Adressen von DNS-Servern aufzählen, um über Änderungen in dieser Zone benachrichtigt zu werden.

</dd> <dt>

**Angehalten**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die Zone angehalten wird.

</dd> <dt>

**RefreshInterval**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt das Aktualisierungsintervall an, in dem die Datensätze mit einem Zeitstempel ungleich 0 (null) aktualisiert werden sollen, damit sie in der Zone verbleiben. Datensätze, die nach Ablauf des Aktualisierungsintervalls nicht aktualisiert wurden, können durch die nächste Kapselung entfernt werden, die von einem Server ausgeführt wird. Dieser Wert darf nie kleiner als der längste Aktualisierungszeitraum der in der Zone registrierten Datensätze sein. Werte, die zu klein sind, können dazu führen, dass gültige DNS-Einträge entfernt werden. -Werte, die zu groß sind, verlängern die Lebensdauer veralteter Datensätze. Dieser Wert wird auf die *DefaultRefreshInterval-Eigenschaft* des DNS-Servers festgelegt, auf dem die Zone erstellt wird.

</dd> <dt>

**Rückwärts**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die Zone umgekehrt (TRUE) oder vorwärts (FALSE) ist.

</dd> <dt>

**ScavengeServers**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Array von Zeichenfolgen, das die Liste der IP-Adressen von DNS-Servern auflistet, die die Kapselung veralteter Datensätze dieser Zone ausführen dürfen. Wenn die Liste nicht angegeben ist, kann jeder primäre DNS-Server, der für die Zone autoritativ ist, die Zone speichern, wenn andere Voraussetzungen erfüllt sind.

</dd> <dt>

**SecondaryServers**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Array von Zeichenfolgen, die IP-Adressen von DNS-Servern aufzählen, die diese Zone über die Zonenreplikation empfangen dürfen.

</dd> <dt>

**SecureSecondaries**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die Zonenübertragung nur für bestimmte secondaries zulässig ist. Designierte secondaries sind DNS-Server, deren IP-Adressen unter SecondariesIPAddressesArrayaufgeführt sind.

</dd> <dt>

**Herunterfahren**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die Kopie der Zone abgelaufen ist. True gibt an, dass die Zone abgelaufen ist oder heruntergefahren wird.

</dd> <dt>

**UseNBStat**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Dieser boolesche Wert gibt an, ob die Zone den reversen NBStat-Lookup verwendet.

</dd> <dt>

**UseWins**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die Zone WINS-Suche verwendet.

</dd> <dt>

**ZoneType**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt den Typ der Zone an. Gültige Werte sind:

-   DS integriert
-   Primär
-   Secondary

**Windows Server 2003: **

Zusätzliche Werte:

-   Cache
-   Stub
-   Weiterleitung

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

[**MicrosoftDNS-Domäne \_**](microsoftdns-domain.md)
</dt> <dt>

[**AgeAllRecords-Methode der \_ MicrosoftDNS-Zonenklasse**](microsoftdns-zone-ageallrecords.md)
</dt> <dt>

[**ChangeZoneType-Methode der \_ MicrosoftDNS-Zonenklasse**](microsoftdns-zone-changezonetype.md)
</dt> <dt>

[**CreateZone-Methode der \_ MicrosoftDNS-Zonenklasse**](microsoftdns-zone-createzone.md)
</dt> <dt>

[**ForceRefresh-Methode der \_ MicrosoftDNS-Zonenklasse**](microsoftdns-zone-forcerefresh.md)
</dt> <dt>

[**GetDistinguishedName-Methode der \_ MicrosoftDNS-Zonenklasse**](microsoftdns-zone-getdistinguishedname.md)
</dt> <dt>

[**PauseZone-Methode der \_ MicrosoftDNS-Zonenklasse**](microsoftdns-zone-pausezone.md)
</dt> <dt>

[**ReloadZone-Methode der \_ MicrosoftDNS-Zonenklasse**](microsoftdns-zone-reloadzone.md)
</dt> <dt>

[**ResetSecondaries-Methode der \_ MicrosoftDNS-Zonenklasse**](microsoftdns-zone-resetsecondaries.md)
</dt> <dt>

[**ResumeZone-Methode der \_ MicrosoftDNS-Zonenklasse**](microsoftdns-zone-resumezone.md)
</dt> <dt>

[**UpdateFromDS-Methode der \_ MicrosoftDNS-Zonenklasse**](microsoftdns-zone-updatefromds.md)
</dt> <dt>

[**WriteBackZone-Methode der \_ MicrosoftDNS-Zonenklasse**](microsoftdns-zone-writebackzone.md)
</dt> </dl>

 

 





