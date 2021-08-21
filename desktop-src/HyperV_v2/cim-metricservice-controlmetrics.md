---
description: 'ControlMetrics-Methode der CIM_MetricService-Klasse: Aktiviert und deaktiviert die Sammlung von Metriken.'
ms.assetid: afb90863-e70a-46e5-b1b7-d959dcacc306
title: ControlMetrics-Methode der CIM_MetricService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricService.ControlMetrics
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c78f575bb68673c364fe627766b3709944c2a062e0407f927262ff019764b7d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068650"
---
# <a name="controlmetrics-method-of-the-cim_metricservice-class"></a>ControlMetrics-Methode der CIM \_ MetricService-Klasse

Aktiviert und deaktiviert die Erfassung von Metriken. **ControlMetrics** wird verwendet, um die Sammlung der einzelnen Metriktypen für ein [**CIM \_ ManagedElement,**](cim-managedelement.md)die Sammlung eines bestimmten Metriktyps für alle verwalteten Elemente oder die Sammlung einer bestimmten Metrik für ein bestimmtes verwaltetes Element zu steuern.

## <a name="syntax"></a>Syntax


```mof
uint32 ControlMetrics(
  [in] CIM_ManagedElement       REF Subject,
  [in] CIM_BaseMetricDefinition REF Definition,
  [in] uint16                       MetricCollectionEnabled
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Betreff* \[ In\]
</dt> <dd>

Ein [**CIM \_ ManagedElement,**](cim-managedelement.md) das verwaltete Elemente identifiziert, für die Metriken gesteuert werden.

</dd> <dt>

*Definition* \[ In\]
</dt> <dd>

Identifiziert eine [**CIM \_ BaseMetricDefinition,**](cim-basemetricdefinition.md) für die Metriken gesteuert werden.

</dd> <dt>

*MetricCollectionEnabled* \[ In\]
</dt> <dd>

Gibt den gewünschten Vorgang an, der für die Metriken ausgeführt werden soll.

<dt>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>

**Aktivieren** (2)


</dt> <dd></dd> <dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

**Deaktivieren** (3)


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

**Zurücksetzen** (4)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF Reserved** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Reservierter Anbieter** (32768..65535)


</dt> <dd></dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg den Wert 0 zurück. andernfalls wird ein Fehler zurückgegeben.

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

[**CIM \_ MetricService**](cim-metricservice.md)
</dt> </dl>

 

 




