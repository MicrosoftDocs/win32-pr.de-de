---
description: Zeigt Metriken nach Klasse an.
ms.assetid: a08c0749-b60b-4b8a-996f-b3bbaf1fb2d3
title: ShowMetricsByClass-Methode der Msvm_MetricService Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricService.ShowMetricsByClass
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 40865847b1deef877c70c1c99349c12915a464b394a38b5b804ea9139d5d0cf1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118147509"
---
# <a name="showmetricsbyclass-method-of-the-msvm_metricservice-class"></a>ShowMetricsByClass-Methode der Msvm \_ MetricService-Klasse

Zeigt Metriken nach Klasse an.

## <a name="syntax"></a>Syntax


```mof
uint32 ShowMetricsByClass(
  [in]  CIM_ManagedElement       REF Subject,
  [in]  CIM_BaseMetricDefinition REF Definition,
  [out] CIM_BaseMetricDefinition REF DefinitionList[],
  [out] string                       MetricNames[],
  [out] uint16                       MetricCollectionEnabled[]
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Betreff* \[ In\]
</dt> <dd>

Identifiziert eine CIM-Klasse, für die die Methode Verweise auf Instanzen von [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md) zurückgibt, die Metriken definieren, die für alle Instanzen der Klasse erfasst werden können.

</dd> <dt>

*Definition* \[ In\]
</dt> <dd>

Identifiziert eine Instanz von [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md). Die -Methode gibt Verweise auf Instanzen von [**CIM \_ ManagedElement**](cim-managedelement.md) zurück, für die von der Instanz von **CIM \_ BaseMetricDefinition** definierte Metriken gesammelt werden können.

</dd> <dt>

*DefinitionList* \[ out\]
</dt> <dd>

Nach erfolgreichem Abschluss der -Methode kann Verweise auf Instanzen von [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md) enthalten, die Metriken definieren, die für die Sammlung für [**das cim \_ ManagedElement**](cim-managedelement.md) verfügbar sind, das durch den *Subject-Parameter identifiziert* wird.

</dd> <dt>

*MetricNames* \[ out\]
</dt> <dd>

Nach erfolgreichem Abschluss der -Methode enthält jeder Arrayindex den Wert der **Name-Eigenschaft** für die Instanz von [**CIM \_ BaseMetricDefinition,**](cim-basemetricdefinition.md) auf die vom entsprechenden Arrayindex des *DefinitionList-Parameters verwiesen* wird.

</dd> <dt>

*MetricCollectionEnabled* \[ out\]
</dt> <dd>

Gibt an, ob eine Metrik für alle Instanzen einer Klasse verwalteter Elemente erfasst wird.

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**Aktiviert** (2)


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Deaktiviert** (3)


</dt> <dd></dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

**Reserviert** (4)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF Reserved** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Anbieter reserviert** (32768..65535)


</dt> <dd></dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt einen der folgenden Werte zurück:

<dl> <dt>

**Erfolg** ()
</dt> <dt>

**Nicht unterstützt** ()
</dt> <dt>

**Fehler** ()
</dt> <dt>

**Reservierte Methode** ()
</dt> <dt>

**Herstellerspezifisch** ()
</dt> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8.1<br/>                                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 R2<br/>                                                                       |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Msvm \_ MetricService**](msvm-metricservice.md)
</dt> </dl>

 

 




