---
description: Ruft Weiterleitungsdaten von einem Zielcomputer ab.
ms.assetid: e9ed210d-09ad-4689-b6a0-f84c5cce86f5
ms.tgt_platform: multiple
title: TargetForwarding-Klasse
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
ms.openlocfilehash: a6025089d069504889d7b97d87a73b167746c3e594013acf58f0ed615162f787
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119529690"
---
# <a name="targetforwarding-class"></a>TargetForwarding-Klasse

Ruft Weiterleitungsdaten von einem Zielcomputer ab.

> [!Note]  
> Auf einem Zielcomputer sind möglicherweise mehrere Weiterleitungen konfiguriert.

 

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

Die **TargetForwarding-Klasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **TargetForwarding-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**CollectorEndpoint**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Behoben**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Die Endpunktinformationen des Collectorservers. Diese Eigenschaft ist als *Host* formatiert:*Portzeichenfolge.*

</dd> <dt>

**Computer**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Behoben**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Der Computername des Zielcomputers.

</dd> <dt>

**ConnectedSince**
</dt> <dd> <dl> <dt>

Datentyp: **DATETIME**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Behoben**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Der Zeitstempel, der angibt, wann die Verbindung für die Weiterleitungsdaten hergestellt wurde.

</dd> <dt>

**Ziel**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Behoben**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Das Ziel der Weiterleitungsdaten, z. B. ein Dateiname.

</dd> <dt>

**DestinationPattern**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Behoben**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Das Format, das zum Generieren des Ziels der Weiterleitungsdaten verwendet wird.

</dd> <dt>

**Fehler**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Behoben**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Eine Fehlermeldung, die einen aufgetretenen Fehler beschreibt. Diese Eigenschaft ist leer, wenn kein Fehler aufgetreten ist.

</dd> <dt>

**ForwarderType**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Behoben**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Der Dateityp, der die Weiterleitungsdaten enthält, z. B. ETL.

</dd> <dt>

**TargetEndpoint**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Schlüssel**](/windows/desktop/WmiSdk/key-qualifier), [**behoben**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Die Endpunktinformationen des Zielcomputers im für Menschen lesbaren Format. Diese Eigenschaft ist als *Host* formatiert:*Portzeichenfolge.* Beispiel: "127.0.0.1:50000".

</dd> <dt>

**TargetGuid**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Schlüssel**](/windows/desktop/WmiSdk/key-qualifier), [**behoben**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Die **SMBIOS-GUID** des Zielcomputers.

</dd> <dt>

**TargetMac**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Schlüssel**](/windows/desktop/WmiSdk/key-qualifier), [**behoben**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Die MAC-Adresse des Zielcomputers.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                                       |
| Namespace<br/>                | \\Stamm-Microsoft \\ Windows \\ BootEventCollector<br/>                                              |
| MOF<br/>                      | <dl> <dt>BootEventCollectorWMI.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>BEvtCol.exe</dt> </dl>               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[WMI-Anbieter für Startereignissammler](boot-event-collector-wmi-provider-portal.md)
</dt> </dl>

 

