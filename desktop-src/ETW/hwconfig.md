---
description: Die hwconfig-Klasse ist die übergeordnete Klasse für Hardware Konfigurations Ereignisse unter Windows XP. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: 47f062c0-fdf0-4beb-906d-257571324de9
title: Hwconfig-Klasse
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
ms.openlocfilehash: cfb194e09701dbc52b00279b624877f09ffac24b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868919"
---
# <a name="hwconfig-class"></a>Hwconfig-Klasse

Die **hwconfig** -Klasse ist die übergeordnete Klasse für Hardware Konfigurations Ereignisse unter Windows XP.

Die folgende Syntax wird durch den MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[Guid("{01853a65-418f-4f36-aefc-dc0f1d2fd235}")]
class HWConfig : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Member

Die **hwconfig** -Klasse definiert keine Member.

## <a name="remarks"></a>Bemerkungen

Diese Ereignisse stellen die Hardwarekonfiguration des Computers bereit. Im Gegensatz zu anderen NT-Kernel Protokollierungs Ereignissen werden von der Kernel Sitzung automatisch Hardware Konfigurations Ereignisse generiert. Sie aktivieren diese Ereignisse nicht, wenn Sie die NT Kernel Logger-Sitzung starten.

**Windows 2000:** Nicht unterstützt.

Informationen zu Hardware Konfigurations Ereignissen unter Windows Vista und Windows Server 2003 finden Sie in der [SystemConfig](systemconfig.md) -Klasse.

Ereignisablaufverfolgungs-Consumer können eine spezielle Verarbeitung für Hardware Konfigurations Ereignisse implementieren, indem Sie die [**settracecallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) -Funktion aufrufen und [**eventtraceconfigguid**](nt-kernel-logger-constants.md) als *pguid* -Parameter angeben. Verwenden Sie die folgenden Ereignis Typen, um das tatsächliche Hardware Konfigurations Ereignis beim Verarbeiten von Ereignissen zu identifizieren.



| Ereignistyp                                                                      | BESCHREIBUNG                                                                                                                                      |
|---------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| **Ereignis \_ Configuration \_ \_ \_ CPU**-Ablaufverfolgungstyp (Ereignistyp Wert ist 10)<br/>          | CPU-Konfigurations Ereignis. Die [**hwconfig \_ CPU**](hwconfig-cpu.md) MOF-Klassen definieren die Ereignisdaten für dieses Ereignis.                            |
| **Ereignis \_ Ablaufverfolgungstyp \_ \_ config \_ LogicalDisk**(Ereignistyp Wert ist 12)<br/>  | Konfigurations Ereignis des logischen Datenträgers. Die MOF-Klasse " [**hwconfig \_ logdisk**](hwconfig-logdisk.md) MOF Classes" definiert die Ereignisdaten für dieses Ereignis. |
| **Ereignis \_ \_Konfigurations- \_ \_ NIC des Ablauf Verfolgungs Typs**(Ereignistyp Wert ist 13)<br/>          | Nic-Konfigurations Ereignis. Die MOF-Klassen der [**hwconfig- \_ NIC**](hwconfig-nic.md) definieren die Ereignisdaten für dieses Ereignis.                            |
| **Ereignis \_ Typ der Ablaufverfolgungstyp \_ \_ config \_ PhysicalDisk**(Ereignistyp Wert ist 11)<br/> | Ereignis für die Konfiguration des physischen Datenträgers Die [**hwconfig \_ phydisk**](hwconfig-phydisk.md) -MOF-Klassen definieren die Ereignisdaten für dieses Ereignis.          |



 

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**MSNT \_ systemtrace**](msnt-systemtrace.md)
</dt> <dt>

[**Hwconfig- \_ CPU**](hwconfig-cpu.md)
</dt> <dt>

[**Hwconfig- \_ logdisk**](hwconfig-logdisk.md)
</dt> <dt>

[**Hwconfig- \_ NIC**](hwconfig-nic.md)
</dt> <dt>

[**Hwconfig- \_ phydisk**](hwconfig-phydisk.md)
</dt> </dl>

 

 
