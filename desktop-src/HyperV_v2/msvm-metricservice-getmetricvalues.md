---
description: Ruft Metrikwerte ab.
ms.assetid: 71c614ef-a005-45aa-9999-a19dc9f9c0df
title: GetMetricValues-Methode der Msvm_MetricService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricService.GetMetricValues
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c22aa9adab9fc69876329f6be0ff011765da61a714c518241c47d3b2bd882ec2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119521460"
---
# <a name="getmetricvalues-method-of-the-msvm_metricservice-class"></a>GetMetricValues-Methode der Msvm \_ MetricService-Klasse

Ruft Metrikwerte ab.

## <a name="syntax"></a>Syntax


```mof
uint32 GetMetricValues(
  [in]  CIM_BaseMetricDefinition REF Definition,
  [in]  uint16                       Range,
  [in]  uint16                       Count,
  [out] CIM_BaseMetricValue      REF Values[]
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Definition* \[ In\]
</dt> <dd>

Identifiziert eine [**CIM \_ BaseMetricDefinition,**](cim-basemetricdefinition.md) für die Metriken zurückgegeben werden.

</dd> <dt>

*Bereich* \[ In\]
</dt> <dd>

Gibt an, wie die Instanzen ausgewählt werden. Der Algorithmus zum Sortieren von Wertinstanzen ist metrikdefinitionsspezifisch.

<dt>

<span id="Minimum"></span><span id="minimum"></span><span id="MINIMUM"></span>

**Minimum** (2)


</dt> <dd></dd> <dt>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>

**Maximal** (3)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF Reserved** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

**Herstellerspezifisch** (32768..65535)


</dt> <dd></dd> </dl> </dd> <dt>

*Anzahl* \[ In\]
</dt> <dd>

Gibt die maximale Anzahl von -Instanzen an, die von der -Methode zurückgegeben werden sollen.

</dd> <dt>

*Werte* \[ out\]
</dt> <dd>

Enthält nach erfolgreichem Abschluss der Methode Verweise auf Instanzen von [**CIM \_ BaseMetricValue,**](cim-basemetricvalue.md)gefiltert nach den Werten der Eingabeparameter.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt einen der folgenden Werte zurück:

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
| Namespace<br/>                | \\Root-Virtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Msvm \_ MetricService**](msvm-metricservice.md)
</dt> </dl>

 

 




