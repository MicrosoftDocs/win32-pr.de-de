---
description: Zeigt die angegebenen Metriken an.
ms.assetid: 3716b5e6-b360-4719-a0f3-60b8d39deb31
title: Showmetrics-Methode der Msvm_MetricService-Klasse
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
ms.openlocfilehash: 9823ea61864b0d87245ebe8b171195a2fd3c411a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868507"
---
# <a name="showmetrics-method-of-the-msvm_metricservice-class"></a>Showmetrics-Methode der MSVM \_ metricservice-Klasse

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

*Betreff* \[ in\]
</dt> <dd>

Der Subject-Parameter identifiziert eine Instanz von [**CIM \_ managedelta**](cim-managedelement.md) , für die die Methode Verweise auf Instanzen von [**CIM \_ basemetricdefinition**](cim-basemetricdefinition.md) zurückgibt, die Metriken definieren, die für das **CIM- \_ managedelta-Element** erfasst werden.

</dd> <dt>

*Definition* \[ in\]
</dt> <dd>

Der Definitions Parameter identifiziert eine Instanz von [**CIM \_ basemetricdefinition**](cim-basemetricdefinition.md). Die-Methode gibt Verweise auf Instanzen von [**CIM \_ managedelta**](cim-managedelement.md) aus, für die von der Instanz von **CIM \_ basemetricdefinition** definierte Metriken zur Erfassung verfügbar sind.

</dd> <dt>

*Managedelements* \[ vorgenommen\]
</dt> <dd>

Nach erfolgreichem Abschluss der-Methode kann der *managedelements* - \[ \] Parameter Verweise auf [**CIM \_ managedelate**](cim-managedelement.md) enthalten, für die die durch den *Definitions* Parameter identifizierte Metrik für die Sammlung verfügbar ist.

</dd> <dt>

*DefinitionList* \[ vorgenommen\]
</dt> <dd>

Nach erfolgreichem Abschluss der-Methode enthält der *DefinitionList* -Parameter möglicherweise Verweise auf Instanzen von [**CIM \_ basemetricdefinition**](cim-basemetricdefinition.md) , die Metriken definieren, die für die Sammlung für das [**CIM- \_ managedelta**](cim-managedelement.md) verfügbar sind, das durch den *Subject* -Parameter identifiziert wird.

</dd> <dt>

*Metricnames* \[ vorgenommen\]
</dt> <dd>

Nach erfolgreichem Abschluss der Methode muss jeder Array Index des *metricnames* -Parameters den Wert der Name-Eigenschaft für die Instanz von [**CIM \_ basemetricdefinition**](cim-basemetricdefinition.md) enthalten, auf die durch den entsprechenden Array Index des *DefinitionList* -Parameters verwiesen wird.

</dd> <dt>

*Metriccollectionaktivierte* \[ vorgenommen\]
</dt> <dd>

Der *metriccollectionaktivierte* Parameter gibt an, ob eine Metrik für ein verwaltetes Element erfasst wird.

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

Diese Methode gibt einen der folgenden Werte zurück.

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

[**MSVM \_ metricservice**](msvm-metricservice.md)
</dt> </dl>

 

 




