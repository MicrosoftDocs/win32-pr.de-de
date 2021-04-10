---
title: MicrosoftDNS_Zone-Klasse
description: Die MicrosoftDNS- \_ Zonen Klasse beschreibt eine DNS-Zone. Jede Instanz der MicrosoftDNS- \_ Zonen Klasse muss genau einem DNS-Server zugewiesen werden. Zonen können mehreren Instanzen der MicrosoftDNS- \_ Domäne oder der MicrosoftDNS- \_ resourcerecord-Klassen zugeordnet werden.
ms.assetid: 9c59fa61-cca5-4718-ad40-8d2c6ed5fc2d
keywords:
- DNS-MicrosoftDNS_Zone Klasse
- DNS-MicrosoftDNS_Zone Klasse, beschrieben
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
ms.openlocfilehash: b15119c7a5cdc1dba2998e17b5c69a4d0e15c6ca
ms.sourcegitcommit: 03fb201e1ea36e353c335ff063ed993fb5993e61
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104041106"
---
# <a name="microsoftdns_zone-class"></a>MicrosoftDNS- \_ Zonen Klasse

> [!NOTE]
> Dieser Artikel enthält Verweise auf den Begriff Slave, einen Begriff, den Microsoft nicht mehr verwendet. Sobald der Begriff aus der Software entfernt wird, wird er auch aus diesem Artikel entfernt.

> [!NOTE]
> Dieser Artikel enthält Verweise auf den Begriff Master Server, einen Begriff, den Microsoft nicht mehr verwendet. Sobald der Begriff aus der Software entfernt wird, wird er auch aus diesem Artikel entfernt.

Die **MicrosoftDNS- \_ Zonen** Klasse beschreibt eine DNS-Zone. Jede Instanz der **MicrosoftDNS- \_ Zonen** Klasse muss genau einem DNS-Server zugewiesen werden. Zonen können mehreren Instanzen der [**MicrosoftDNS- \_ Domäne**](microsoftdns-domain.md) oder der [**MicrosoftDNS- \_ resourcerecord**](microsoftdns-resourcerecord.md) -Klassen zugeordnet werden.

Die folgende Syntax wird durch den MOF-Code vereinfacht.

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

Die **MicrosoftDNS- \_ Zonen** Klasse verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **MicrosoftDNS- \_ Zonen** Klasse verfügt über diese Methoden.



| Methode                   | BESCHREIBUNG                                                                                                                                                                                                |
|:-------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **AgeAllRecords**        | Ermöglicht die Alterung für einige oder alle nicht-NS-und nicht-SOA-Datensätze.<br/>                                                                                                                                       |
| **Changezonetype**       | Ändert Zonen Typen. <br/> Qualifizierer: Implementiert<br/>                                                                                                                                         |
| **"Kreatezone"**           | Erstellt eine neue Zone. <br/> Qualifizierer: keine.<br/>                                                                                                                                               |
| **ForceRefresh**         | Erzwingt ein Update der sekundären Datenbank vom DNS-Master Server. <br/> Qualifizierer: Implementiert<br/>                                                                                               |
| **Getchilshedname** | Ruft den Distinguished Name DS für die Zone ab. <br/> Qualifizierer: Implementiert<br/>                                                                                                                 |
| **Pausegzone**            | Hält die Zone an. <br/> Qualifizierer: Implementiert<br/>                                                                                                                                            |
| **Reloadzone**           | Lädt die Zone erneut. <br/> Qualifizierer: Implementiert<br/>                                                                                                                                           |
| **Resetsecon-Replikate**     | Setzt das Array der sekundären IP-Adresse zurück. <br/> Qualifizierer: Implementiert<br/>                                                                                                                      |
| **Resumezone**           | Nimmt die Zone wieder auf. <br/> Qualifizierer: Implementiert<br/>                                                                                                                                           |
| **Updatefromds**         | Erzwingt ein Update der Zone aus dem Verzeichnisdienst (DS). Damit diese Methode gültig ist, muss zonetype gleich 0 sein. die Zone muss tatsächlich in DS gespeichert werden. <br/> Qualifizierer: Implementiert<br/> |
| **"Write Backzone"**        | Speichert Zonendaten in der zugehörigen Zonendatei. <br/> Qualifizierer: implementiert, statisch<br/>                                                                                                                   |



 

### <a name="properties"></a>Eigenschaften

Die **MicrosoftDNS- \_ Zonen** Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Zunehmendem**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt das Verhalten für die Alterung und das Verhalten der Zone an. NULL gibt an, dass das Bereinigung deaktiviert ist. Wenn das Bereinigung deaktiviert ist, werden die Zeitstempel der Datensätze in der Zone nicht aktualisiert, und die Datensätze unterliegen nicht dem scräging. Wenn diese Einstellung auf 1 festgelegt ist, werden die Datensätze gelöscht, und ihre Zeitstempel werden aktualisiert, wenn der Server die Anforderung für das dynamische Update für die Datensätze empfängt. Für Active Directory integrierte Zonen wird dieser Wert auf die *DefaultAgingState* -Eigenschaft des DNS-Servers festgelegt, auf dem die Zone erstellt wird. Für Standard primäre Zonen ist der Standardwert 0 (null).

</dd> <dt>

**AllowUpdate**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die Zone dynamische Update Anforderungen akzeptiert.

</dd> <dt>

**Automatisch**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die Zone automatisch erstellt wird.

</dd> <dt>

**Availforscavengetime**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt die Zeit an, zu der der Server versuchen kann, die Zone zu löschen. Auch wenn die Zone so konfiguriert ist, dass die Weiterbildung aktiviert ist, versucht der DNS-Server erst nach diesem Moment, diese Zone zu löschen. Dieser Wert wird auf die aktuelle Uhrzeit zuzüglich des Aktualisierungs Intervalls der Zone festgelegt, wenn die Zone geladen wird. Dieser Parameter wird lokal gespeichert und nicht in andere Kopien der Zone repliziert.

</dd> <dt>

**Datendatei**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt den Namen der Zonendatei an.

</dd> <dt>

**Disablewinsrecordreplizierung**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob der WINS-Datensatz repliziert wird. Wenn true festgelegt ist, ist die WINS-Daten Satz Replikation deaktiviert.

</dd> <dt>

**Dsintegriert**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die Zone DS-integriert ist.

</dd> <dt>

**Forwarderslave**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob das DNS Rekursion verwendet, wenn die Namen für die angegebene vorwärts Zone aufgelöst werden. Gilt nur für bedingte Weiterleitungs Zonen.

</dd> <dt>

**Weiterforwardertimeout**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt die Zeit in Sekunden an, die ein DNS-Server, der eine Abfrage für den Namen in der Forward-Zone weiterleitet, auf eine Auflösung von der Weiterleitung wartet, bevor versucht wird, die Abfrage selbst aufzulösen. Dieser Parameter gilt nur für die vorwärts Zonen.

</dd> <dt>

**Lasterfolgreichen fulsoacheck**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Anzahl der Sekunden seit dem 1. Januar 1970 GMT, seit die SOA-Seriennummer für die Zone zuletzt aktiviert wurde.

</dd> <dt>

**Lasterfolgreiches XFR**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Anzahl der Sekunden seit dem 1. Januar 1970 GMT, seit die Zone zuletzt von einem Master Server übertragen wurde.

</dd> <dt>

**Localmasterservers**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Lokale IP-Adressen der Master-DNS-Server für diese Zone. Wenn festgelegt, werden diese Master Server in Active Directory überlaufen.

</dd> <dt>

**Master Server**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

IP-Adressen der Master-DNS-Server für diese Zone.

</dd> <dt>

**NoRefreshInterval**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt das Zeitintervall zwischen der letzten Aktualisierung des Zeitstempels eines Datensatzes und dem frühesten Zeitpunkt an, zu dem der Zeitstempel aktualisiert werden kann.

</dd> <dt>

**Benachrichtigen**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die Master Zone die sekundären Replikate über Änderungen in der RRS-Datenbank benachrichtigt. Legen Sie auf 1 fest, um sekundäre Datenbanken zu Benachrichtigen

</dd> <dt>

**Notifyservers**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Array von Zeichen folgen, das IP-Adressen von DNS-Servern auflistet, die über Änderungen in dieser Zone benachrichtigt werden sollen.

</dd> <dt>

**Angehalten**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die Zone angehalten wurde.

</dd> <dt>

**RefreshInterval**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt das Aktualisierungs Intervall an, in dem die Datensätze mit einem Zeitstempel ungleich NULL aktualisiert werden, damit Sie in der Zone verbleiben. Datensätze, die nach Ablauf des Aktualisierungs Intervalls nicht aktualisiert wurden, können durch das nächste von einem Server ausgeführte Bereinigung entfernt werden. Dieser Wert sollte nie kleiner als der längste Aktualisierungs Zeitraum der in der Zone registrierten Datensätze sein. Werte, die zu klein sind, können dazu führen, dass gültige DNS-Einträge entfernt werden. Werte, die zu groß sind, verlängern die Lebensdauer veralteter Datensätze. Dieser Wert wird auf die *DefaultRefreshInterval* -Eigenschaft des DNS-Servers festgelegt, auf dem die Zone erstellt wird.

</dd> <dt>

**Umgekehr**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die Zone umgekehrt (true) oder vorwärts (false) ist.

</dd> <dt>

**Scavengeservers**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Array von Zeichen folgen, das die Liste der IP-Adressen von DNS-Servern auflistet, die für die Ausführung veralteter Datensätze dieser Zone berechtigt sind. Wenn die Liste nicht angegeben wird, darf jeder primäre DNS-Server, der für die Zone autorisierend ist, die Zone durchlaufen, wenn andere Voraussetzungen erfüllt sind.

</dd> <dt>

**Secondaryservers**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Array von Zeichen folgen, das IP-Adressen von DNS-Servern auflistet, die diese Zone durch Zonen Replikation empfangen dürfen.

</dd> <dt>

**Securesecon-Replikate**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die Zonen Übertragung nur für bestimmte sekundäre Replikate zulässig ist. Die vorgesehenen sekundären Replikate sind DNS-Server, deren IP-Adressen in secondariesipaddressesarray aufgeführt sind.

</dd> <dt>

**Herunterfahren**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die Kopie der Zone abgelaufen ist. TRUE gibt an, dass die Zone abgelaufen ist oder heruntergefahren wird.

</dd> <dt>

**Usenbstat**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Dieser boolesche Wert gibt an, ob die Zone NBSTAT Reverse Lookup verwendet.

</dd> <dt>

**Usewins**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die Zone WINS-Suche verwendet.

</dd> <dt>

**Zonetype**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt den Typ der Zone an. Gültige Werte sind:

-   DS integriert
-   Primär
-   Secondary

* * Windows Server 2003: * *

Weitere Werte:

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
| MOF<br/>                      | <dl> <dt>Dnsprov. MOF</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MicrosoftDNS- \_ Domäne**](microsoftdns-domain.md)
</dt> <dt>

[**AgeAllRecords-Methode der MicrosoftDNS- \_ Zonen Klasse**](microsoftdns-zone-ageallrecords.md)
</dt> <dt>

[**Changezonetype-Methode der MicrosoftDNS- \_ Zonen Klasse**](microsoftdns-zone-changezonetype.md)
</dt> <dt>

[**Die Methode "kreatezone" der MicrosoftDNS- \_ Zonen Klasse**](microsoftdns-zone-createzone.md)
</dt> <dt>

[**ForceRefresh-Methode der MicrosoftDNS- \_ Zonen Klasse**](microsoftdns-zone-forcerefresh.md)
</dt> <dt>

[**Geterkennbar shedname-Methode der MicrosoftDNS- \_ Zonen Klasse**](microsoftdns-zone-getdistinguishedname.md)
</dt> <dt>

[**Pauzzone-Methode der MicrosoftDNS- \_ Zonen Klasse**](microsoftdns-zone-pausezone.md)
</dt> <dt>

[**Reloadzone-Methode der MicrosoftDNS- \_ Zonen Klasse**](microsoftdns-zone-reloadzone.md)
</dt> <dt>

[**Resetsecon-Replikats-Methode der MicrosoftDNS- \_ Zonen Klasse**](microsoftdns-zone-resetsecondaries.md)
</dt> <dt>

[**Resumezone-Methode der MicrosoftDNS- \_ Zonen Klasse**](microsoftdns-zone-resumezone.md)
</dt> <dt>

[**Updatefromds-Methode der MicrosoftDNS- \_ Zonen Klasse**](microsoftdns-zone-updatefromds.md)
</dt> <dt>

[**"Write Backzone"-Methode der MicrosoftDNS- \_ Zonen Klasse**](microsoftdns-zone-writebackzone.md)
</dt> </dl>

 

 





