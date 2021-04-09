---
description: 'Gibt Folgendes an: die verfügbaren Metriken für alle Instanzen einer CIM-Klasse, die CIM-Klassen, für die eine von einer Instanz von CIM \_ basemetricdefinition definierte Metrik zur Erfassung verfügbar ist, und ob für ein verwaltetes Element zurzeit eine bestimmte Metrik erfasst wird.'
ms.assetid: 0115a5b5-2824-4c43-a8dc-757524c5d3dd
title: Showmetricsbyclass-Methode der CIM_MetricService-Klasse
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
ms.openlocfilehash: f843c835e6c92e39c4ac1f9628d0479b94a691bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865540"
---
# <a name="showmetricsbyclass-method-of-the-cim_metricservice-class"></a>Showmetricsbyclass-Methode der CIM \_ metricservice-Klasse

Gibt Folgendes an: die verfügbaren Metriken für alle Instanzen einer CIM-Klasse, die CIM-Klassen, für die eine von einer Instanz von [**CIM \_ basemetricdefinition**](cim-basemetricdefinition.md) definierte Metrik zur Erfassung verfügbar ist, und ob für ein verwaltetes Element zurzeit eine bestimmte Metrik erfasst wird.

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

*Betreff* \[ in\]
</dt> <dd>

Identifiziert eine CIM-Klasse, für die die-Methode Verweise auf Instanzen von [**CIM \_ basemetricdefinition**](cim-basemetricdefinition.md) zurückgibt, die Metriken definieren, die für alle Instanzen der Klasse aufgezeichnet werden können.

</dd> <dt>

*Definition* \[ in\]
</dt> <dd>

Identifiziert eine Instanz von [**CIM \_ basemetricdefinition**](cim-basemetricdefinition.md). Die-Methode gibt Verweise auf Instanzen von [**CIM \_ managedelta**](cim-managedelement.md) aus, für die von der Instanz von **CIM \_ basemetricdefinition** definierte Metriken zur Erfassung verfügbar sind.

</dd> <dt>

*DefinitionList* \[ vorgenommen\]
</dt> <dd>

Bei Erfolg enthält möglicherweise Verweise auf Instanzen von [**CIM \_ basemetricdefinition**](cim-basemetricdefinition.md) -Objekten, die Metriken definieren, die für die Sammlung für das [**CIM- \_ managedelta**](cim-managedelement.md) verfügbar sind, das durch den *Subject* -Parameter identifiziert wird.

</dd> <dt>

*Metricnames* \[ vorgenommen\]
</dt> <dd>

Bei Erfolg muss jeder Array Index den Wert der **Name** -Eigenschaft für die Instanz von [**CIM \_ basemetricdefinition**](cim-basemetricdefinition.md) enthalten, auf die durch den entsprechenden Array Index des *DefinitionList* -Parameters verwiesen wird.

</dd> <dt>

*Metriccollectionaktivierte* \[ vorgenommen\]
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

**DMTF reserviert** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Anbieter reserviert** (32768.65535)


</dt> <dd></dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 (null) zurück. Andernfalls wird ein Fehler zurückgegeben.

<dl> <dt>

**Erfolg** (0)
</dt> <dt>

**Nicht unterstützt** (1)
</dt> <dt>

Fehler **(2** )
</dt> <dt>

**Reservierte Methode** (..)
</dt> <dt>

**Hersteller spezifisch** (32768.65535)
</dt> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8.1<br/>                                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 R2<br/>                                                                       |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM- \_ metricservice**](cim-metricservice.md)
</dt> </dl>

 

 




