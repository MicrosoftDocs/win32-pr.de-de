---
description: Die HWConfig-Klasse ist die übergeordnete Klasse für Hardwarekonfigurationsereignisse auf Windows XP. Die folgende Syntax wird durch einen MOF-Code vereinfacht.
ms.assetid: 47f062c0-fdf0-4beb-906d-257571324de9
title: HWConfig-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HWConfig
api_type:
- NA
api_location: ''
ms.openlocfilehash: e1d4b8f69784729ffe5d51f3068b03fc0b4154182b2d05f2896e4556a05f7eba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118394680"
---
# <a name="hwconfig-class"></a>HWConfig-Klasse

Die **HWConfig-Klasse** ist die übergeordnete Klasse für Hardwarekonfigurationsereignisse auf Windows XP.

Die folgende Syntax wird durch einen MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[Guid("{01853a65-418f-4f36-aefc-dc0f1d2fd235}")]
class HWConfig : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Member

Die **HWConfig-Klasse** definiert keine Member.

## <a name="remarks"></a>Hinweise

Diese Ereignisse stellen die Hardwarekonfiguration des Computers zur Verfügung. Im Gegensatz zu anderen NT-Kernelprotokollierungsereignissen generiert die Kernelsitzung automatisch Hardwarekonfigurationsereignisse. Sie aktivieren diese Ereignisse nicht, wenn Sie die NT-Kernelprotokollierungssitzung starten.

**Windows 2000:** Nicht unterstützt.

Hardwarekonfigurationsereignisse auf Windows Vista und Windows Server 2003 finden Sie in der [SystemConfig-Klasse.](systemconfig.md)

Ereignisverfolgungsverbraucher können eine spezielle Verarbeitung für Hardwarekonfigurationsereignisse implementieren, indem sie die [**SetTraceCallback-Funktion**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) aufrufen und [**EventTraceConfigGuid**](nt-kernel-logger-constants.md) als *pGuid-Parameter* angeben. Verwenden Sie die folgenden Ereignistypen, um das tatsächliche Hardwarekonfigurationsereignis bei der Nutzung von Ereignissen zu identifizieren.



| Ereignistyp                                                                      | BESCHREIBUNG                                                                                                                                      |
|---------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| **EVENT \_ TRACE \_ TYPE \_ CONFIG \_ CPU**(Ereignistypwert ist 10)<br/>          | CPU-Konfigurationsereignis. Die [**HWConfig-CPU-MOF-Klassen \_**](hwconfig-cpu.md) definieren die Ereignisdaten für dieses Ereignis.                            |
| **EVENT \_ TRACE \_ TYPE \_ CONFIG \_ LOGICALDISK**(Ereignistypwert ist 12)<br/>  | Logisches Datenträgerkonfigurationsereignis. Die [**MOF-Klasse HWConfig \_ LogDisk**](hwconfig-logdisk.md) MOF definiert die Ereignisdaten für dieses Ereignis. |
| **EVENT \_ TRACE \_ TYPE \_ CONFIG \_ NIC**(Ereignistypwert ist 13)<br/>          | NIC-Konfigurationsereignis. Die [**MOF-Klassen \_ der HWConfig-NIC**](hwconfig-nic.md) definieren die Ereignisdaten für dieses Ereignis.                            |
| **EVENT \_ TRACE \_ TYPE \_ CONFIG \_ PHYSICALDISK**(Ereignistypwert ist 11)<br/> | Physisches Datenträgerkonfigurationsereignis. Die [**HWConfig \_ PhyDisk**](hwconfig-phydisk.md) MOF-Klassen definieren die Ereignisdaten für dieses Ereignis.          |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**MSNT \_ SystemTrace**](msnt-systemtrace.md)
</dt> <dt>

[**\_HWConfig-CPU**](hwconfig-cpu.md)
</dt> <dt>

[**HWConfig \_ LogDisk**](hwconfig-logdisk.md)
</dt> <dt>

[**\_HWConfig-NIC**](hwconfig-nic.md)
</dt> <dt>

[**HWConfig \_ PhyDisk**](hwconfig-phydisk.md)
</dt> </dl>

 

 
