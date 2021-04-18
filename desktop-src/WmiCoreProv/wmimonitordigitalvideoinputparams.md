---
description: Stellt Eingabeparameter für digitales Video dar.
ms.assetid: aa459612-db79-477b-891f-28c9d0b1b497
title: Wmimonitordigitalvideoinputparameams-Klasse
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
ms.openlocfilehash: a08e38a38bb5f5e8d539fabdf69c429c42f4b1f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366071"
---
# <a name="wmimonitordigitalvideoinputparams-class"></a>Wmimonitordigitalvideoinputparameams-Klasse

**Wmimonitordigitalvideoinputparameams** stellt Eingabeparameter für digitales Video dar. Die Daten in dieser Klasse entsprechen den Daten in der Videoeingabe Definition von "velectronics Standard Association (VESA) Enhanced Extended Display Identification Data (E-EDID) Standard". Eine Instanz dieser Klasse ist nur verfügbar, wenn der Wert der **videoinputtype** -Eigenschaft der [**wmimonitorbasicdisplaypara**](wmimonitorbasicdisplayparams.md) -Klasse "Digital" ist.

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

Die **wmimonitordigitalvideoinputparameams** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **wmimonitordigitalvideoinputparser** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Aktiv**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt den aktiven Monitor an.

</dd> <dt>

**InstanceName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Schlüssel**
</dt> </dl>

Der Name der spezifischen Monitor Instanz.

</dd> <dt>

**IsDFP1xCompatible**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

VESA DFP 1. x oder kompatibel. Wenn diese Option festgelegt ist, ist die Schnittstelle Signal kompatibel mit VESA Digital Flat Panel (DFP) 1. x Übergang minimids (Minimum Differential signds) crgb, 1 Pixel/Clock, bis zu 8 Bits/Farbe, das am signifikantesten (am wichtigsten ist), de aktiv hoch.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                         |
| Namespace<br/>                | WMI-Stammdatei \\<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>WMI Core. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MSMonitorClass**](msmonitorclass.md)
</dt> </dl>

 

 




