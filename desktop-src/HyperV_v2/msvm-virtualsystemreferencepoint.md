---
description: Stellt einen Referenzpunkt für ein virtuelles System dar.
ms.assetid: b3ba4fa7-3b77-4a1d-ab8f-d38af12ab5dd
title: Msvm_VirtualSystemReferencePoint-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePoint
- Msvm_VirtualSystemReferencePoint.InstanceID
- Msvm_VirtualSystemReferencePoint.ReferencePointType
- Msvm_VirtualSystemReferencePoint.ConsistencyLevel
- Msvm_VirtualSystemReferencePoint.VirtualSystemIdentifier
- Msvm_VirtualSystemReferencePoint.HasAssociatedData
- Msvm_VirtualSystemReferencePoint.VirtualDiskIdentifiers
- Msvm_VirtualSystemReferencePoint.ResilientChangeTrackingIdentifiers
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: add160cf44a592462634704ddf783cd8f4084068
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106353256"
---
# <a name="msvm_virtualsystemreferencepoint-class"></a>MSVM \_ virtualsystemreferencepoint-Klasse

Stellt einen Referenzpunkt für ein virtuelles System dar.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemReferencePoint : CIM_ManagedElement
{
  string  InstanceID;
  uint16  ReferencePointType;
  uint16  ConsistencyLevel;
  string  VirtualSystemIdentifier;
  boolean HasAssociatedData;
  string  VirtualDiskIdentifiers[];
  string  ResilientChangeTrackingIdentifiers[];
};
```

## <a name="members"></a>Member

Die **MSVM \_ virtualsystemreferencepoint** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSVM \_ virtualsystemreferencepoint** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**ConsistencyLevel**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Die Konsistenz Ebene des Bezugspunkts.

<dt>

<span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

<span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>**Anwendungs konsistent** (1)


</dt> <dd>

Der Bezugspunkt gibt einen Zeitpunkt an, an dem sich das virtuelle System in einem Anwendungs konsistenten Zustand befunden hat.

</dd> <dt>

<span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>

<span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>**Absturz konsistent** (2)


</dt> <dd>

Der Bezugspunkt gibt einen Zeitpunkt an, an dem sich das virtuelle System in einem Absturz konsistenten Zustand befunden hat.

</dd> </dl>

</dd> <dt>

**Hasassociateddata**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Auf **true** festgelegt, wenn der Verweis Punkt über zugeordnete Daten verfügt. Dies gilt nur für Protokoll basierte Referenzpunkte. Bei RCT-basierten Bezugspunkten wird **hasassociateddata** auf **false** festgelegt. Bei Protokoll basierten Referenzpunkten wird **hasassociateddata** , sobald das Protokoll verworfen wird, **false**.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceId"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Eindeutige Identifikation eines Referenzpunkt Objekts.

</dd> <dt>

**Referencepointtype**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt den Typ des Bezugspunkts an.

<dt>

<span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>

<span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>**Protokoll basiert** (1)


</dt> <dd>

Protokoll Nachverfolgung für Hyper-V-Replikate.

</dd> <dt>

<span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>

<span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>**RCT basiert** (2)


</dt> <dd>

Basierend auf robusten Änderungsnachverfolgung von virtuellen Datenträgern.

</dd> </dl>

</dd> <dt>

**Resilientchangetrackingidentifier**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Array von RCT-IDs, die den virtuellen Datenträgern der VM zum Zeitpunkt der Erstellung dieses Bezugspunkts entsprechen. Dieses Feld ist nur für RCT-basierte Referenzpunkte gültig.

</dd> <dt>

**Virtualdiskidentifier**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Array von WMI-Instanz-IDs, die den virtuellen Datenträgern der VM zum Zeitpunkt der Erstellung dieses Bezugspunkts entsprechen. Diesen virtuellen Datenträgern sind RCT-IDs zugeordnet.

</dd> <dt>

**Virtualsystemidentifier**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ Computersystem**](cim-computersystem.md).**Name**")
</dt> </dl>

Der Name des [**CIM- \_ Computer Systems**](cim-computersystem.md) , zu dem dieser Bezugspunkt gehört.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 10 \[ -Desktop-Apps\]<br/>                                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM- \_ managedelta**](cim-managedelement.md)
</dt> </dl>

 

