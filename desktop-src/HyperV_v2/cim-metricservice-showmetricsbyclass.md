---
description: 'Meldet Folgendes: die verfügbaren Metriken, die für alle Instanzen einer CIM-Klasse gesammelt werden können, die CIM-Klassen, für die eine durch eine Instanz von CIM BaseMetricDefinition definierte Metrik verfügbar ist, und ob derzeit eine bestimmte Metrik für ein verwaltetes Element gesammelt \_ wird.'
ms.assetid: 0115a5b5-2824-4c43-a8dc-757524c5d3dd
title: ShowMetricsByClass-Methode der CIM_MetricService Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricService.ShowMetricsByClass
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c70d81f153471e841803dde195f09886137f29b390298c2c7d09ce69ad1648e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119694950"
---
# <a name="showmetricsbyclass-method-of-the-cim_metricservice-class"></a>ShowMetricsByClass-Methode der CIM \_ MetricService-Klasse

Meldet Folgendes: die verfügbaren Metriken, die für alle Instanzen einer CIM-Klasse gesammelt werden können, die CIM-Klassen, für die eine durch eine Instanz von [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md) definierte Metrik verfügbar ist, und ob derzeit eine bestimmte Metrik für ein verwaltetes Element gesammelt wird.

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

Bei Erfolg kann Verweise auf Instanzen von [**CIM \_ BaseMetricDefinition-Objekten**](cim-basemetricdefinition.md) enthalten, die Metriken definieren, die für die Sammlung für [**das cim \_ ManagedElement**](cim-managedelement.md) verfügbar sind, das durch den *Subject-Parameter identifiziert* wird.

</dd> <dt>

*MetricNames* \[ out\]
</dt> <dd>

Bei Erfolg muss jeder Arrayindex den Wert der **Name-Eigenschaft** für die Instanz von [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md) enthalten, auf die durch den entsprechenden Arrayindex des *DefinitionList-Parameters verwiesen* wird.

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

Gibt bei Erfolg eine 0 zurück. andernfalls gibt einen Fehler zurück.

<dl> <dt>

**Erfolg** (0)
</dt> <dt>

**Nicht unterstützt** (1)
</dt> <dt>

**Fehler** (2)
</dt> <dt>

**Reservierte Methode** (..)
</dt> <dt>

**Herstellerspezifisch** (32768..65535)
</dt> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8.1<br/>                                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 R2<br/>                                                                       |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CIM \_ MetricService**](cim-metricservice.md)
</dt> </dl>

 

 




