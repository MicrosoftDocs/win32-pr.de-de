---
description: Ruft Metrikwerte ab.
ms.assetid: 71c614ef-a005-45aa-9999-a19dc9f9c0df
title: Getmetricvalues-Methode der Msvm_MetricService-Klasse
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
ms.openlocfilehash: fe3e32b21ec0baa497fcef781e1b48fae37fbf66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350918"
---
# <a name="getmetricvalues-method-of-the-msvm_metricservice-class"></a>Getmetricvalues-Methode der MSVM \_ metricservice-Klasse

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

*Definition* \[ in\]
</dt> <dd>

Gibt eine [**CIM- \_ basemetricdefinition**](cim-basemetricdefinition.md) an, für die Metriken zurückgegeben werden.

</dd> <dt>

*Bereich* \[ in\]
</dt> <dd>

Gibt an, wie die Instanzen ausgewählt werden. Der Algorithmus zum Anordnen von Wert Instanzen ist metrikdefinitionsspezifisch.

<dt>

<span id="Minimum"></span><span id="minimum"></span><span id="MINIMUM"></span>

**Minimal** (2)


</dt> <dd></dd> <dt>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>

**Maximum** (3)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF reserviert** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

**Hersteller spezifisch** (32768.65535)


</dt> <dd></dd> </dl> </dd> <dt>

*Anzahl* \[ in\]
</dt> <dd>

Gibt die maximale Anzahl von-Instanzen an, die von der-Methode zurückgegeben werden sollen.

</dd> <dt>

*Werte* \[ vorgenommen\]
</dt> <dd>

Nach erfolgreichem Abschluss der-Methode enthält Verweise auf Instanzen von [**CIM \_ basemetricvalue**](cim-basemetricvalue.md), die entsprechend den Werten der Eingabeparameter gefiltert werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt einen der folgenden Werte zurück:

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

 

 




