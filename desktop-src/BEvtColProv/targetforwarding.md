---
description: Ruft Weiterleitungs Daten von einem Bereitstellungs Zielcomputer ab.
ms.assetid: e9ed210d-09ad-4689-b6a0-f84c5cce86f5
ms.tgt_platform: multiple
title: Targetforwarding-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TargetForwarding
- TargetForwarding.TargetEndpoint
- TargetForwarding.TargetMac
- TargetForwarding.TargetGuid
- TargetForwarding.CollectorEndpoint
- TargetForwarding.Computer
- TargetForwarding.ForwarderType
- TargetForwarding.Destination
- TargetForwarding.DestinationPattern
- TargetForwarding.Error
- TargetForwarding.ConnectedSince
api_type:
- DllExport
api_location:
- BEvtCol.exe
ms.openlocfilehash: aba0a40ccd5611cecfe7450e518620d4d41ec1e0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104522907"
---
# <a name="targetforwarding-class"></a>Targetforwarding-Klasse

Ruft Weiterleitungs Daten von einem Bereitstellungs Zielcomputer ab.

> [!Note]  
> Auf einem Bereitstellungs Zielcomputer können mehrere Weiterleitungen konfiguriert sein.

 

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Provider("BootEventCollectorWmiProvider"), Dynamic, AMENDMENT]
class TargetForwarding
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
};
```

## <a name="members"></a>Member

Die **targetforwarding** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **targetforwarding** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Collector Endpoint**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **korrigiert**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Die Endpunkt Informationen des Collector-Servers. Diese Eigenschaft ist als *Host*:*Port* Zeichenfolge formatiert.

</dd> <dt>

**Computer**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **korrigiert**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Der Computername des Ziel Computers.

</dd> <dt>

**Connectedsince**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **korrigiert**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Der Zeitstempel, der angibt, wann die Verbindung für die Weiterleitungs Daten hergestellt wurde.

</dd> <dt>

**Ziel**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **korrigiert**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Das Ziel der Weiterleitungs Daten, z. b. ein Dateiname.

</dd> <dt>

**Destinationpattern**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **korrigiert**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Das Format, das verwendet wird, um das Ziel der Weiterleitungs Daten zu generieren.

</dd> <dt>

**Fehler**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **korrigiert**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Eine Fehlermeldung, in der ein aufgetretene Fehler beschrieben wird. Diese Eigenschaft ist leer, wenn kein Fehler aufgetreten ist.

</dd> <dt>

**Weiterforwardertyp**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **korrigiert**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Der Dateityp, der die Weiterleitungs Daten enthält, z. b. ETL.

</dd> <dt>

**Targetendpoint**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Schlüssel**](/windows/desktop/WmiSdk/key-qualifier), [**korrigiert**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Die Endpunkt Informationen des Ziel Computers in einem von menschenlesbaren Format. Diese Eigenschaft ist als *Host*:*Port* Zeichenfolge formatiert. Beispiel: "127.0.0.1:50000".

</dd> <dt>

**Targetguid**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Schlüssel**](/windows/desktop/WmiSdk/key-qualifier), [**korrigiert**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Die SMBIOS- **GUID** des Ziel Computers.

</dd> <dt>

**Targetmac**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Schlüssel**](/windows/desktop/WmiSdk/key-qualifier), [**korrigiert**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Die Mac-Adresse des Ziel Computers.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                                       |
| Namespace<br/>                | Stammverzeichnis von \\ Microsoft \\ Windows \\ booteventcollector<br/>                                              |
| MOF<br/>                      | <dl> <dt>Booteventcollector WMI. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>BEvtCol.exe</dt> </dl>               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[WMI-Anbieter für Start Ereignis Sammler](boot-event-collector-wmi-provider-portal.md)
</dt> </dl>

 

