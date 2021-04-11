---
description: Aktiviert und deaktiviert die Auflistung von Metriken.
ms.assetid: afb90863-e70a-46e5-b1b7-d959dcacc306
title: Controlmetrics-Methode der CIM_MetricService-Klasse
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
ms.openlocfilehash: 60a7d0b34227594cf7146a988aa7e0d232f2d6cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216249"
---
# <a name="controlmetrics-method-of-the-cim_metricservice-class"></a>Controlmetrics-Methode der CIM \_ metricservice-Klasse

Aktiviert und deaktiviert die Auflistung von Metriken. **Controlmetrics** wird verwendet, um die Sammlung der einzelnen metrikmetriken für ein [**CIM- \_ managedelement**](cim-managedelement.md), die Sammlung eines bestimmten metriktyps für alle verwalteten Elemente oder die Auflistung einer bestimmten Metrik für ein bestimmtes verwaltetes Element zu steuern.

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

*Betreff* \[ in\]
</dt> <dd>

Ein [**CIM- \_ managedelement**](cim-managedelement.md) , das verwaltete (n) Elemente identifiziert, für die Metriken gesteuert werden.

</dd> <dt>

*Definition* \[ in\]
</dt> <dd>

Gibt eine [**CIM- \_ basemetricdefinition**](cim-basemetricdefinition.md) an, für die Metriken gesteuert werden.

</dd> <dt>

*Metriccollectionaktivierte* \[ in\]
</dt> <dd>

Gibt den für die Metriken auszuführenden gewünschten Vorgang an.

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

 

 




