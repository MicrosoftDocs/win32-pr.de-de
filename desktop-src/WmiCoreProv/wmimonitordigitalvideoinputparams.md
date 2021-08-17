---
description: Stellt Eingabeparameter für digitales Video dar.
ms.assetid: aa459612-db79-477b-891f-28c9d0b1b497
title: WmiMonitorDigitalVideoInputParams-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorDigitalVideoInputParams
- WmiMonitorDigitalVideoInputParams.Active
- WmiMonitorDigitalVideoInputParams.InstanceName
- WmiMonitorDigitalVideoInputParams.IsDFP1xCompatible
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: fa86add32d77a5b2838fc78eaf097c11b8a15db3f0fde9186f93046691ebc3f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117926566"
---
# <a name="wmimonitordigitalvideoinputparams-class"></a>WmiMonitorDigitalVideoInputParams-Klasse

**WmiMonitorDigitalVideoInputParams** stellt Eingabeparameter für digitale Videos dar. Die Daten in dieser Klasse entsprechen Daten im E-EDID-Standard (Video Input Definition of Video Electronics Standard Association) Enhanced Extended Display Identification Data (VESA). Eine Instanz dieser Klasse ist nur verfügbar, wenn der Wert der **VideoInputType-Eigenschaft** der [**WmiMonitorBasicDisplayParams-Klasse**](wmimonitorbasicdisplayparams.md) "Digital" ist.

## <a name="syntax"></a>Syntax

``` syntax
class WmiMonitorDigitalVideoInputParams : MSMonitorClass
{
  boolean Active;
  string  InstanceName;
  boolean IsDFP1xCompatible;
};
```

## <a name="members"></a>Member

Die **WmiMonitorDigitalVideoInputParams-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **WmiMonitorDigitalVideoInputParams-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Aktiv**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt den aktiven Monitor an.

</dd> <dt>

**InstanceName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Schlüssel**
</dt> </dl>

Name der spezifischen Monitorinstanz.

</dd> <dt>

**IsDFP1xCompatible**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

VESA DFP 1.x oder kompatibel. Wenn festgelegt, ist die Schnittstelle signalkompatibel mit VESA Digital Flat Panel (DFP) 1.x Transition Minimized Differential Signaling (TMDS) CRGB, 1 Pixel/Uhr, bis zu 8 Bits/Farbe am signifikantesten Bit (MSB) ausgerichtet, DE aktiv hoch.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                         |
| Namespace<br/>                | Root \\ wmi<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>WmiCore.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**MSMonitorClass**](msmonitorclass.md)
</dt> </dl>

 

 




