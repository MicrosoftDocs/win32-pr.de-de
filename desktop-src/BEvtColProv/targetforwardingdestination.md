---
description: Die bekannten Ziele, die die gesammelten Daten enthalten. Nur verfügbar, wenn der Collector mit aktivierten Statusprotokollen ausgeführt wird.
ms.assetid: ab0d2949-9808-49c3-8a0c-f2ce9c300a2a
ms.tgt_platform: multiple
title: TargetForwardingDestination-Klasse
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
ms.openlocfilehash: 58492b8b334085a6dd03c397558c4f10bc1fa4aff441f5b7bbfc7ba7cf37b0bc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119589000"
---
# <a name="targetforwardingdestination-class"></a>TargetForwardingDestination-Klasse

Die bekannten Ziele, die die gesammelten Daten enthalten. Nur verfügbar, wenn der Collector mit aktivierten Statusprotokollen ausgeführt wird.

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

Die **TargetForwardingDestination-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **TargetForwardingDestination-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**CollectorEndpoint**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Behoben**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Die Host:Port-Informationen des Endpunkts auf der Collectorseite.

</dd> <dt>

**Computer**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Behoben**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Der Name des Zielcomputers, der vom Collector gemäß seiner Konfiguration bestimmt wird.

</dd> <dt>

**ConnectedSince**
</dt> <dd> <dl> <dt>

Datentyp: **DATETIME**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Behoben**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Zeitstempel des Zeitpunkts, zu dem die Verbindung hergestellt wurde.

</dd> <dt>

**Ziel**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Ziel der Daten. Die Bedeutung hängt vom Forwardertyp ab. Kann ein Dateiname oder eine andere Identifikation sein.

</dd> <dt>

**DestinationPattern**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Behoben**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Muster, das zum Generieren des Ziels der Daten verwendet wird. Die Bedeutung hängt vom Typ und der Konfiguration der Forwarder ab. Für ein festes Ziel wäre dasselbe wie das Ziel selbst. Für das Ziel mit Der Drehung der Dateien enthält die Musterzeichen, die durch den tatsächlichen Index im Ziel ersetzt werden.

</dd> <dt>

**DisconnectedSince**
</dt> <dd> <dl> <dt>

Datentyp: **DATETIME**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Behoben**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Zeitstempel des Zeitpunkts, zu dem die Verbindung gelöscht wurde.

</dd> <dt>

**Fehler**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Behoben**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Fehlermeldung, wenn ein Fehler aufgetreten ist. Andernfalls ist leer.

</dd> <dt>

**ForwarderType**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Typ der Weitergeleiteten (z. B. "etl").

</dd> <dt>

**TargetEndpoint**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Behoben**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Die Endpunktinformationen des Zielcomputers im lesbaren Format. Diese Eigenschaft wird als Hostformatiert:*Portzeichenfolge.* Beispiel: "127.0.0.1:50000".

</dd> <dt>

**TargetGuid**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Behoben**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Die SMBIOS-GUID des Zielcomputers (sofern bekannt).

</dd> <dt>

**TargetMac**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Behoben**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Die MAC-Adresse des Zielcomputers (sofern bekannt).

</dd> <dt>

**WmiDateTime**
</dt> <dd> <dl> <dt>

Datentyp: **DATETIME**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Behoben**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Zeitstempel des Zeitpunkts, zu dem diese Zustandsänderung aufgezeichnet wurde.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                                       |
| Namespace<br/>                | Root \\ Microsoft \\ Windows \\ BootEventCollector<br/>                                              |
| MOF<br/>                      | <dl> <dt>BootEventCollectorWMI.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>BEvtCol.exe</dt> </dl>               |



 

