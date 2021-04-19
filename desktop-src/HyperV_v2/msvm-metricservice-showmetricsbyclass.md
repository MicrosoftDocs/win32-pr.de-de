---
description: Zeigt Metriken nach Klasse an.
ms.assetid: a08c0749-b60b-4b8a-996f-b3bbaf1fb2d3
title: Showmetricsbyclass-Methode der Msvm_MetricService-Klasse
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
ms.openlocfilehash: 93f132b24c6c20826b1551e979c128b1aa38c8d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349201"
---
# <a name="showmetricsbyclass-method-of-the-msvm_metricservice-class"></a>Showmetricsbyclass-Methode der MSVM \_ metricservice-Klasse

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

Nach erfolgreichem Abschluss der-Methode enthält möglicherweise Verweise auf Instanzen von [**CIM \_ basemetricdefinition**](cim-basemetricdefinition.md) , die Metriken definieren, die für die Sammlung für das [**CIM- \_ managedelta**](cim-managedelement.md) verfügbar sind, das durch den *Subject* -Parameter identifiziert wird.

</dd> <dt>

*Metricnames* \[ vorgenommen\]
</dt> <dd>

Nach erfolgreichem Abschluss der-Methode enthält jeder Array Index den Wert der **Name** -Eigenschaft für die Instanz von [**CIM \_ basemetricdefinition**](cim-basemetricdefinition.md) , auf die durch den entsprechenden Array Index des *DefinitionList* -Parameters verwiesen wird.

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

Diese Methode gibt einen der folgenden Werte zurück:

<dl> <dt>

**Erfolg** ()
</dt> <dt>

**Nicht unterstützt** ()
</dt> <dt>

Fehler **()**
</dt> <dt>

**Reservierte Methode** ()
</dt> <dt>

**Hersteller spezifisch** ()
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

 

 




