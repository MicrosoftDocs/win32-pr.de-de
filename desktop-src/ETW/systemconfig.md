---
description: 'SystemConfig-Klasse: Diese Klasse ist die übergeordnete Klasse für Hardwarekonfigurationsereignisse. Die folgende Syntax wird aus MOF-Code vereinfacht.'
ms.assetid: 720c2366-bd68-4895-bfaf-74aa9b64ba4a
title: SystemConfig-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig
api_type:
- NA
api_location: ''
ms.openlocfilehash: 232214aa2c33485d909525d54965f59fdc891a29
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105868"
---
# <a name="systemconfig-class"></a>SystemConfig-Klasse

Diese Klasse ist die übergeordnete Klasse für Hardwarekonfigurationsereignisse.

Die folgende Syntax wird aus MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[Guid("{01853a65-418f-4f36-aefc-dc0f1d2fd235}"), EventVersion(2)]
class SystemConfig : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Member

Die **SystemConfig-Klasse** definiert keine Member.

## <a name="remarks"></a>Bemerkungen

Diese Ereignisse stellen die Hardwarekonfiguration des Computers bereit. Im Gegensatz zu anderen NT-Kernelprotokollierungsereignissen generiert die Kernelsitzung automatisch Hardwarekonfigurationsereignisse. Sie aktivieren diese Ereignisse nicht, wenn Sie die NT-Kernelprotokollierungssitzung starten.

Informationen zu Hardwarekonfigurationsereignissen unter Windows XP finden Sie in der [HWConfig-Klasse.](hwconfig.md)

Consumer der Ereignisablaufverfolgung können eine spezielle Verarbeitung für Hardwarekonfigurationsereignisse implementieren, indem sie die [**SetTraceCallback-Funktion**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) aufrufen und [**EventTraceConfigGuid**](nt-kernel-logger-constants.md) als *pGuid-Parameter* angeben. Verwenden Sie die folgenden Ereignistypen, um das tatsächliche Hardwarekonfigurationsereignis beim Nutzen von Ereignissen zu identifizieren.



| Ereignistyp                                                                      | BESCHREIBUNG                                                                                                                                                                         |
|---------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **EVENT \_ TRACE \_ TYPE \_ CONFIG \_ CPU**(Ereignistypwert ist 10)<br/>          | CPU-Konfigurationsereignis. Die [**\_ MOF-Klassen der SystemConfig-CPU**](systemconfig-cpu.md) definieren die Ereignisdaten für dieses Ereignis.                                                       |
| **EVENT \_ TRACE \_ TYPE \_ CONFIG \_ IDECHANNEL**(Ereignistypwert ist 23)<br/>   | Primäres und sekundäres IDE-Kanalkonfigurationsereignis. Die [**MOF-Klasse der SystemConfig \_ IDEChannel**](systemconfig-idechannel.md) MOF-Klassen definiert die Ereignisdaten für dieses Ereignis. |
| **EVENT \_ TRACE \_ TYPE \_ CONFIG \_ IRQ**(Ereignistypwert ist 21)<br/>          | IrQ-Ereignis (Interrupt Request). Die [**MOF-Klasse \_ "SystemConfig IRQ**](systemconfig-irq.md) MOF" definiert die Ereignisdaten für dieses Ereignis.                                       |
| **EVENT \_ TRACE \_ TYPE \_ CONFIG \_ LOGICALDISK**(Ereignistypwert ist 12)<br/>  | Logisches Datenträgerkonfigurationsereignis. Die [**MOF-Klasse der SystemConfig LogDisk-MOF-Klasse \_**](systemconfig-logdisk.md) definiert die Ereignisdaten für dieses Ereignis.                            |
| **EVENT \_ TRACE \_ TYPE \_ CONFIG \_ NETINFO**(Ereignistypwert ist 17)<br/>      | Netzwerk-iformationsereignis. Die [**SystemConfig \_ Network**](systemconfig-network.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.                                                |
| **EVENT \_ TRACE \_ TYPE \_ CONFIG \_ NIC**(Ereignistypwert ist 13)<br/>          | NIC-Konfigurationsereignis. Die [**MOF-Klassen \_ der SystemConfig-NIC**](systemconfig-nic.md) definieren die Ereignisdaten für dieses Ereignis.                                                       |
| **EVENT \_ TRACE \_ TYPE \_ CONFIG \_ PHYSICALDISK**(Ereignistypwert ist 11)<br/> | Physisches Datenträgerkonfigurationsereignis. Die [**MOF-Klassen von SystemConfig \_ PhyDisk**](systemconfig-phydisk.md) definieren die Ereignisdaten für dieses Ereignis.                                     |
| **EVENT \_ TRACE \_ TYPE \_ CONFIG \_ PNP**(Ereignistypwert ist 22)<br/>          | Plug &amp; Play-Ereignis. Die [**MOF-Klasse \_ der SystemConfig-PNP-MOF-Klasse**](systemconfig-pnp.md) definiert die Ereignisdaten für dieses Ereignis.                                                 |
| **EVENT \_ TRACE \_ TYPE \_ CONFIG \_ POWER**(Ereignistypwert ist 16)<br/>        | Energiekonfigurationsereignis. Die [**SystemConfig \_ Power**](systemconfig-power.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.                                                   |
| **EVENT \_ TRACE \_ TYPE \_ CONFIG \_ SERVICES**(Ereignistypwert ist 15)<br/>     | Dienstkonfigurationsereignis. Die [**MOF-Klasse von SystemConfig \_ Services**](systemconfig-services.md) definiert die Ereignisdaten für dieses Ereignis.                                          |
| **EVENT \_ TRACE \_ TYPE \_ CONFIG \_ VIDEO**(Ereignistypwert ist 14)<br/>        | Grafikadapterkonfigurationsereignis. Die [**SystemConfig \_ Video**](systemconfig-video.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.                                        |



 

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**MSNT \_ SystemTrace**](msnt-systemtrace.md)
</dt> <dt>

[**\_SystemConfig-CPU**](systemconfig-cpu.md)
</dt> <dt>

[**SystemConfig \_ IDEChannel**](systemconfig-idechannel.md)
</dt> <dt>

[**SystemConfig \_ IRQ**](systemconfig-irq.md)
</dt> <dt>

[**SystemConfig \_ LogDisk**](systemconfig-logdisk.md)
</dt> <dt>

[**SystemConfig \_ Network**](systemconfig-network.md)
</dt> <dt>

[**\_SystemConfig-NIC**](systemconfig-nic.md)
</dt> <dt>

[**SystemConfig \_ PhyDisk**](systemconfig-phydisk.md)
</dt> <dt>

[**\_SystemConfig-PNP**](systemconfig-pnp.md)
</dt> <dt>

[**SystemConfig \_ Power**](systemconfig-power.md)
</dt> <dt>

[**SystemConfig \_ Services**](systemconfig-services.md)
</dt> <dt>

[**\_SystemConfig-Video**](systemconfig-video.md)
</dt> <dt>

[**SystemConfig \_ V0**](systemconfig-v0.md)
</dt> </dl>

 

 
