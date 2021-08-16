---
description: Wird verwendet, um die Auflistung von Metriken für ein oder mehrere verwaltete Elemente zu steuern.
ms.assetid: 3DC043ED-A790-4322-BF80-55961E9946C2
title: ControlMetrics-Methode der Msvm_MetricService Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricService.ControlMetrics
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 051a08f261432c817bc0e56cab323c56cd11935c1541c40357b6b151a14f4074
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118645846"
---
# <a name="controlmetrics-method-of-the-msvm_metricservice-class"></a>ControlMetrics-Methode der Msvm \_ MetricService-Klasse

Wird verwendet, um die Auflistung von Metriken für ein oder mehrere verwaltete Elemente zu steuern.

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

Eine [**CIM \_ ManagedElement-Instanz,**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) die die verwalteten Elemente identifiziert, für die Metriken gesammelt werden. Wenn dieser Parameter NULL **ist,** werden die Metriken für alle verwalteten Elemente erfasst, die dem *Definition-Parameter* zugeordnet sind.

</dd> <dt>

*Definition* \[ In\]
</dt> <dd>

Eine [**Msvm \_ BaseMetricDefinition-Instanz,**](msvm-basemetricdefinition.md) die angibt, welche Metriken gesammelt werden. Wenn dieser Parameter NULL **ist,** werden die Metriken für alle Definitionen erfasst, die dem verwalteten Element zugeordnet sind, das durch den *Subject-Parameter* identifiziert wird.

</dd> <dt>

*MetricCollectionEnabled* \[ In\]
</dt> <dd>

Gibt den Vorgang an, der für die Metriksammlung durchgeführt werden soll. Dies muss einer der folgenden Werte sein.

<dt>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>**Aktivieren** (2)


</dt> <dd>

Aktivieren Der Sammlung von Metriken.

</dd> <dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**Deaktivieren** (3)


</dt> <dd>

Deaktivieren Sie die Sammlung von Metriken.

</dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Zurücksetzen** (4)


</dt> <dd>

Zurücksetzen von Metrikwerten.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Reservierter Anbieter** (32768..65535)


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

## <a name="remarks"></a>Hinweise

Diese Methode kann in den folgenden Instanzen nicht verwendet werden:

-   Die *Parameter Subject* und *Definition* sind beide **NULL.**
-   Die *Parameter Subject* und *Definition* sind beide nicht **NULL,** und es gibt keine Instanz von [**Msvm \_ MetricDefForME,**](msvm-metricdefforme.md) die die beiden Instanzen zugibt.
-   Der *Definition-Parameter* ist ein Verweis auf eine Instanz von [**Msvm \_ BaseMetricDefinition,**](msvm-basemetricdefinition.md) die [**msvm \_ MetricService**](msvm-metricservice.md) über [**Msvm \_ ServiceAffectsElement**](msvm-serviceaffectselement.md)nicht zugeordnet ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Msvm \_ MetricService**](msvm-metricservice.md)
</dt> </dl>

 

