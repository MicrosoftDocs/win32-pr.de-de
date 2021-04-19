---
description: Wird verwendet, um die Sammlung von Metriken für ein verwaltetes Element oder Elemente zu steuern.
ms.assetid: 3DC043ED-A790-4322-BF80-55961E9946C2
title: Controlmetrics-Methode der Msvm_MetricService-Klasse
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
ms.openlocfilehash: b12fbf71b860571bb3bb5ee06cb58483e782f479
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362575"
---
# <a name="controlmetrics-method-of-the-msvm_metricservice-class"></a>Controlmetrics-Methode der MSVM \_ metricservice-Klasse

Wird verwendet, um die Sammlung von Metriken für ein verwaltetes Element oder Elemente zu steuern.

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

Eine [**CIM \_ managedelements**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) -Instanz, die die verwalteten Elemente identifiziert, für die Metriken erfasst werden. Wenn dieser Parameter **null** ist, werden die Metriken für alle verwalteten Elemente, die dem *Definitions* Parameter zugeordnet sind, gesammelt.

</dd> <dt>

*Definition* \[ in\]
</dt> <dd>

Eine [**MSVM \_ basemetricdefinition**](msvm-basemetricdefinition.md) -Instanz, die angibt, welche Metriken erfasst werden. Wenn dieser Parameter **null** ist, werden die Metriken für alle Definitionen, die dem verwalteten Element zugeordnet sind, das durch den *Subject* -Parameter identifiziert wird, erfasst.

</dd> <dt>

*Metriccollectionaktivierte* \[ in\]
</dt> <dd>

Gibt den Vorgang an, der für die metriksammlung auszuführen ist. Dabei muss es sich um einen der folgenden Werte handeln:

<dt>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>**Aktivieren** (2)


</dt> <dd>

Aktivieren Sie die metriksammlung.

</dd> <dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**Deaktivieren** (3)


</dt> <dd>

Deaktivieren Sie die metrikauflistung.

</dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Zurücksetzen** (4)


</dt> <dd>

Zurücksetzen von Metrikwerten.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Anbieter reserviert** (32768.65535)


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

## <a name="remarks"></a>Bemerkungen

Bei dieser Methode tritt in den folgenden Fällen ein Fehler auf:

-   Die Parameter " *Subject* " und " *Definition* " sind beide **null**.
-   Die Parameter " *Subject* " und " *Definition* " sind nicht **null** , und es ist keine Instanz von [**MSVM \_ metricdefforme**](msvm-metricdefforme.md) vorhanden, die die beiden Instanzen verknüpft.
-   Der *Definitions* Parameter ist ein Verweis auf eine Instanz von [**MSVM \_ basemetricdefinition**](msvm-basemetricdefinition.md) , die nicht mit MSVM [**\_ metricservice**](msvm-metricservice.md) über [**MSVM \_ serviceaffectselements**](msvm-serviceaffectselement.md)verknüpft ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MSVM \_ metricservice**](msvm-metricservice.md)
</dt> </dl>

 

