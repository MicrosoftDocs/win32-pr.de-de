---
description: 'Meldet Folgendes: die Metriken, die für ein verwaltetes Element erfasst werden können, die verwalteten Elemente, für die eine Metrik, die durch eine Instanz von CIM \_ basemetricdefinition definiert ist, zur Erfassung verfügbar ist, und ob eine bestimmte Metrik aktuell für ein verwaltetes Element erfasst wird.'
ms.assetid: 5af430d2-9ab3-4bee-ad51-d9045b51172a
title: Showmetrics-Methode der CIM_MetricService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricService.ShowMetrics
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1e0e062adaefd6c6d9bdabe6f168bd64e789acc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131748"
---
# <a name="showmetrics-method-of-the-cim_metricservice-class"></a>Showmetrics-Methode der CIM \_ metricservice-Klasse

Meldet Folgendes: die Metriken, die für ein verwaltetes Element erfasst werden können, die verwalteten Elemente, für die eine Metrik, die durch eine Instanz von [**CIM \_ basemetricdefinition**](cim-basemetricdefinition.md) definiert ist, zur Erfassung verfügbar ist, und ob eine bestimmte Metrik aktuell für ein verwaltetes Element erfasst wird.

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

*Betreff* \[ in\]
</dt> <dd>

Identifiziert eine Instanz von [**CIM \_ managedelta**](cim-managedelement.md) , für die die Methode Verweise auf Instanzen von [**CIM \_ basemetricdefinition**](cim-basemetricdefinition.md) zurückgibt, die Metriken definieren, die für das **CIM- \_ managedelta-Element** erfasst werden.

</dd> <dt>

*Definition* \[ in\]
</dt> <dd>

Identifiziert eine Instanz von [**CIM \_ basemetricdefinition**](cim-basemetricdefinition.md). Die-Methode gibt Verweise auf Instanzen von [**CIM \_ managedelta**](cim-managedelement.md) aus, für die von der Instanz von **CIM \_ basemetricdefinition** definierte Metriken zur Erfassung verfügbar sind.

</dd> <dt>

*Managedelements* \[ vorgenommen\]
</dt> <dd>

Bei Erfolg enthält möglicherweise Verweise auf [**CIM \_ managedelta**](cim-managedelement.md) -Objekte, für die die vom *Definitions* Parameter identifizierte Metrik für die Sammlung verfügbar ist.

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

Gibt an, ob eine Metrik für ein verwaltetes Element erfasst wird.

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

 

 




