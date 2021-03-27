---
description: Diese Klasse ist die übergeordnete Klasse für Hardware Konfigurations Ereignisse. Die folgende Syntax wird durch den MOF-Code vereinfacht.
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
ms.openlocfilehash: 3332d396005deb2fb811d101a99827544ebc6df0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869288"
---
# <a name="systemconfig-class"></a>SystemConfig-Klasse

Diese Klasse ist die übergeordnete Klasse für Hardware Konfigurations Ereignisse.

Die folgende Syntax wird durch den MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[Guid("{01853a65-418f-4f36-aefc-dc0f1d2fd235}"), EventVersion(2)]
class SystemConfig : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Member

Die **SystemConfig** -Klasse definiert keine Member.

## <a name="remarks"></a>Bemerkungen

Diese Ereignisse stellen die Hardwarekonfiguration des Computers bereit. Im Gegensatz zu anderen NT-Kernel Protokollierungs Ereignissen werden von der Kernel Sitzung automatisch Hardware Konfigurations Ereignisse generiert. Sie aktivieren diese Ereignisse nicht, wenn Sie die NT Kernel Logger-Sitzung starten.

Informationen zu Hardware Konfigurations Ereignissen unter Windows XP finden Sie in der [hwconfig](hwconfig.md) -Klasse.

Ereignisablaufverfolgungs-Consumer können eine spezielle Verarbeitung für Hardware Konfigurations Ereignisse implementieren, indem Sie die [**settracecallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) -Funktion aufrufen und [**eventtraceconfigguid**](nt-kernel-logger-constants.md) als *pguid* -Parameter angeben. Verwenden Sie die folgenden Ereignis Typen, um das tatsächliche Hardware Konfigurations Ereignis beim Verarbeiten von Ereignissen zu identifizieren.



| Ereignistyp                                                                      | BESCHREIBUNG                                                                                                                                                                         |
|---------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Ereignis \_ Configuration \_ \_ \_ CPU**-Ablaufverfolgungstyp (Ereignistyp Wert ist 10)<br/>          | CPU-Konfigurations Ereignis. Die MOF-Klassen der [**SystemConfig- \_ CPU**](systemconfig-cpu.md) definieren die Ereignisdaten für dieses Ereignis.                                                       |
| **Ereignis \_ \_Parametertyp \_ config- \_ idechannel**(Ereignistyp Wert ist 23)<br/>   | Konfigurations Ereignis für primäres und sekundäres IDE-Channel Die MOF-Klasse der [**SystemConfig- \_ idechannel**](systemconfig-idechannel.md) -MOF-Klassen definiert die Ereignisdaten für dieses Ereignis. |
| **Ereignis \_ Ablaufverfolgungstyp \_ \_ config \_ UNQ**(Ereignistyp Wert ist 21)<br/>          | UNQ-Ereignis (Interrupt Request). Die MOF-Klasse [**SystemConfig \_ UNQ**](systemconfig-irq.md) MOF-Klassen definiert die Ereignisdaten für dieses Ereignis.                                       |
| **Ereignis \_ Ablaufverfolgungstyp \_ \_ config \_ LogicalDisk**(Ereignistyp Wert ist 12)<br/>  | Konfigurations Ereignis des logischen Datenträgers. Die MOF-Klasse " [**SystemConfig \_ logdisk**](systemconfig-logdisk.md) MOF Classes" definiert die Ereignisdaten für dieses Ereignis.                            |
| **Ereignis \_ Ablaufverfolgungstyp \_ \_ config \_ NetInfo**(Ereignistyp Wert ist 17)<br/>      | Netzwerk-Informationen-Ereignis. Die MOF-Klasse [**SystemConfig \_ Network**](systemconfig-network.md) definiert die Ereignisdaten für dieses Ereignis.                                                |
| **Ereignis \_ \_Konfigurations- \_ \_ NIC des Ablauf Verfolgungs Typs**(Ereignistyp Wert ist 13)<br/>          | Nic-Konfigurations Ereignis. Die MOF-Klassen der [**SystemConfig- \_ NIC**](systemconfig-nic.md) definieren die Ereignisdaten für dieses Ereignis.                                                       |
| **Ereignis \_ Typ der Ablaufverfolgungstyp \_ \_ config \_ PhysicalDisk**(Ereignistyp Wert ist 11)<br/> | Ereignis für die Konfiguration des physischen Datenträgers Die MOF-Klassen von [**SystemConfig \_ phydisk**](systemconfig-phydisk.md) definieren die Ereignisdaten für dieses Ereignis.                                     |
| **Ereignis \_ Ablaufverfolgungstyp \_ \_ config \_ PnP**(Ereignistyp Wert ist 22)<br/>          | Plug & amp; Play-Ereignis. Die MOF-Klasse der [**SystemConfig \_ PnP**](systemconfig-pnp.md) MOF-Klassen definiert die Ereignisdaten für dieses Ereignis.                                                 |
| **Ereignis \_ Konfiguration des Ablaufverfolgungstyp \_ \_ config \_**(Ereignistyp Wert ist 16)<br/>        | Power Configuration-Ereignis. Die " [**SystemConfig \_ Power**](systemconfig-power.md) MOF"-Klasse definiert die Ereignisdaten für dieses Ereignis.                                                   |
| **Ereignis \_ \_ \_ Konfigurations \_ Dienste des Ablauf Verfolgungs Typs**(Ereignistyp Wert ist 15)<br/>     | Dienst Konfigurations Ereignis. Die MOF-Klasse der [**SystemConfig- \_ Dienste**](systemconfig-services.md) definiert die Ereignisdaten für dieses Ereignis.                                          |
| **Ereignis \_ \_ \_ Konfigurationstyp config \_ Video**(Ereignistyp Wert ist 14)<br/>        | Konfigurations Ereignis des Grafikadapters. Die [**SystemConfig \_ Video**](systemconfig-video.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.                                        |



 

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**MSNT \_ systemtrace**](msnt-systemtrace.md)
</dt> <dt>

[**SystemConfig- \_ CPU**](systemconfig-cpu.md)
</dt> <dt>

[**SystemConfig- \_ idechannel**](systemconfig-idechannel.md)
</dt> <dt>

[**SystemConfig \_ UNQ**](systemconfig-irq.md)
</dt> <dt>

[**SystemConfig- \_ logdisk**](systemconfig-logdisk.md)
</dt> <dt>

[**SystemConfig- \_ Netzwerk**](systemconfig-network.md)
</dt> <dt>

[**SystemConfig- \_ NIC**](systemconfig-nic.md)
</dt> <dt>

[**SystemConfig- \_ phydisk**](systemconfig-phydisk.md)
</dt> <dt>

[**SystemConfig \_ PnP**](systemconfig-pnp.md)
</dt> <dt>

[**\_Systemkonfigurationsstrom**](systemconfig-power.md)
</dt> <dt>

[**SystemConfig- \_ Dienste**](systemconfig-services.md)
</dt> <dt>

[**SystemConfig- \_ Video**](systemconfig-video.md)
</dt> <dt>

[**SystemConfig \_ v0**](systemconfig-v0.md)
</dt> </dl>

 

 
