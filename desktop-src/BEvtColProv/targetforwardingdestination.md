---
description: Die bekannten Ziele, die die gesammelten Daten enthalten. Nur verfügbar, wenn der Collector mit aktiviertem Status Protokoll ausgeführt wird.
ms.assetid: ab0d2949-9808-49c3-8a0c-f2ce9c300a2a
ms.tgt_platform: multiple
title: Targetforwardingdestination-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TargetForwardingDestination
- TargetForwardingDestination.TargetEndpoint
- TargetForwardingDestination.TargetMac
- TargetForwardingDestination.TargetGuid
- TargetForwardingDestination.CollectorEndpoint
- TargetForwardingDestination.Computer
- TargetForwardingDestination.ForwarderType
- TargetForwardingDestination.Destination
- TargetForwardingDestination.DestinationPattern
- TargetForwardingDestination.Error
- TargetForwardingDestination.ConnectedSince
- TargetForwardingDestination.DisconnectedSince
- TargetForwardingDestination.WmiDateTime
api_type:
- DllExport
api_location:
- BEvtCol.exe
ms.openlocfilehash: 735b6179fe9d72b5faf0cad976410aeace427f63
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104482795"
---
# <a name="targetforwardingdestination-class"></a>Targetforwardingdestination-Klasse

Die bekannten Ziele, die die gesammelten Daten enthalten. Nur verfügbar, wenn der Collector mit aktiviertem Status Protokoll ausgeführt wird.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Provider("BootEventCollectorWmiProvider"), Dynamic, AMENDMENT]
class TargetForwardingDestination
{
  string   TargetEndpoint;
  string   TargetMac;
  string   TargetGuid;
  string   CollectorEndpoint;
  string   Computer;
  string   ForwarderType;
  string   Destination;
  string   DestinationPattern;
  string   Error;
  DATETIME ConnectedSince;
  DATETIME DisconnectedSince;
  DATETIME WmiDateTime;
};
```

## <a name="members"></a>Member

Die Klasse " **targetforwardingdestination** " verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **targetforwardingdestination** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Collector Endpoint**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **korrigiert**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Der Host: Port Informationen des Endpunkts auf der Collector-Seite.

</dd> <dt>

**Computer**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **korrigiert**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Der Name des Ziel Computers, der vom Collector entsprechend seiner Konfiguration festgelegt wurde.

</dd> <dt>

**Connectedsince**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **korrigiert**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Der Zeitstempel, zu dem die Verbindung hergestellt wurde.

</dd> <dt>

**Ziel**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Schlüssel**](/windows/desktop/WmiSdk/key-qualifier), [**korrigiert**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Das Ziel der Daten. Die Bedeutung hängt vom Weiterleitungs Typen ab. Kann ein Dateiname oder ein anderer Identifizierungs-ID sein.

</dd> <dt>

**Destinationpattern**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **korrigiert**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Muster, das verwendet wird, um das Ziel der Daten zu generieren. Die Bedeutung hängt von der Weiterleitungs Art und der Konfiguration ab. Für ein festes Ziel wäre das gleiche wie das Ziel selbst. Für das Ziel mit der Drehung der Dateien würde die Muster Zeichen enthalten, die durch den eigentlichen Index im Ziel ersetzt werden.

</dd> <dt>

**Disconnectedsince**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **korrigiert**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Zeitstempel für den Zeitpunkt, zu dem die Verbindung gelöscht wurde.

</dd> <dt>

**Fehler**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **korrigiert**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Fehlermeldung, wenn ein Fehler aufgetreten ist. Andernfalls ist es leer.

</dd> <dt>

**Weiterforwardertyp**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Schlüssel**](/windows/desktop/WmiSdk/key-qualifier), [**korrigiert**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Der Typ der Weiterleitung (z. b. "ETL").

</dd> <dt>

**Targetendpoint**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **korrigiert**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Die Endpunkt Informationen des Ziel Computers in einem von menschenlesbaren Format. Diese Eigenschaft ist als *Host*:*Port* Zeichenfolge formatiert. Beispiel: "127.0.0.1:50000".

</dd> <dt>

**Targetguid**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **korrigiert**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Die SMBIOS-GUID des Ziel Computers (sofern bekannt).

</dd> <dt>

**Targetmac**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **korrigiert**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Die Mac-Adresse des Ziel Computers (sofern bekannt).

</dd> <dt>

**Wmidatetime**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **korrigiert**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Zeitstempel für den Zeitpunkt, zu dem diese Zustandsänderung aufgezeichnet wurde.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                                       |
| Namespace<br/>                | Stammverzeichnis von \\ Microsoft \\ Windows \\ booteventcollector<br/>                                              |
| MOF<br/>                      | <dl> <dt>Booteventcollector WMI. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>BEvtCol.exe</dt> </dl>               |



 

