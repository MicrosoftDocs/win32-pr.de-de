---
description: Zeigt die angegebenen Metriken an.
ms.assetid: 3716b5e6-b360-4719-a0f3-60b8d39deb31
title: ShowMetrics-Methode der Msvm_MetricService Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricService.ShowMetrics
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 052f708f07a8e1074eeaa6c8089ccd410bb63af478072545d5db92af7933fc49
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119521470"
---
# <a name="showmetrics-method-of-the-msvm_metricservice-class"></a>ShowMetrics-Methode der Msvm \_ MetricService-Klasse

Zeigt die angegebenen Metriken an.

## <a name="syntax"></a>Syntax


```mof
uint32 ShowMetrics(
  [in]  CIM_ManagedElement       REF Subject,
  [in]  CIM_BaseMetricDefinition REF Definition,
  [out] CIM_ManagedElement       REF ManagedElements[],
  [out] CIM_BaseMetricDefinition REF DefinitionList[],
  [out] string                       MetricNames[],
  [out] uint16                       MetricCollectionEnabled[]
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Betreff* \[ In\]
</dt> <dd>

Der Subject-Parameter identifiziert eine Instanz von [**CIM \_ ManagedElement,**](cim-managedelement.md) für die die -Methode Verweise auf Instanzen von [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md) zurückgibt, die Metriken definieren, die für **cim \_ ManagedElement erfasst werden.**

</dd> <dt>

*Definition* \[ In\]
</dt> <dd>

Der Definition-Parameter identifiziert eine Instanz von [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md). Die -Methode gibt Verweise auf Instanzen von [**CIM \_ ManagedElement**](cim-managedelement.md) zurück, für die von der Instanz von **CIM \_ BaseMetricDefinition** definierte Metriken gesammelt werden können.

</dd> <dt>

*ManagedElements* \[ out\]
</dt> <dd>

Nach erfolgreichem Abschluss der Methode kann der *ManagedElements-Parameter* Verweise auf \[ \] CIM [**\_ ManagedElement**](cim-managedelement.md) enthalten, für die die durch den *Definition-Parameter* identifizierte Metrik für die Auflistung verfügbar ist.

</dd> <dt>

*DefinitionList* \[ out\]
</dt> <dd>

Nach erfolgreichem Abschluss der -Methode kann der *DefinitionList-Parameter* Verweise auf Instanzen von [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md) enthalten, die Metriken definieren, die für die Sammlung für [**das CIM \_ ManagedElement**](cim-managedelement.md) verfügbar sind, das durch den *Subject-Parameter identifiziert* wird.

</dd> <dt>

*MetricNames* \[ out\]
</dt> <dd>

Nach erfolgreichem Abschluss der -Methode muss jeder Arrayindex des *Parameters MetricNames* den Wert der Name-Eigenschaft für die Instanz von [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md) enthalten, auf die vom entsprechenden Arrayindex des *DefinitionList-Parameters* verwiesen wird.

</dd> <dt>

*MetricCollectionEnabled* \[ out\]
</dt> <dd>

Der *Parameter MetricCollectionEnabled gibt* an, ob eine Metrik für ein verwaltetes Element erfasst wird.

<dt>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>

**Aktivieren** (2)


</dt> <dd></dd> <dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

**Deaktivieren** (3)


</dt> <dd></dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

**Reserviert** (4)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF Reserved** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Reservierter Anbieter** (32768..65535)


</dt> <dd></dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt einen der folgenden Werte zurück.

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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Msvm \_ MetricService**](msvm-metricservice.md)
</dt> </dl>

 

 




