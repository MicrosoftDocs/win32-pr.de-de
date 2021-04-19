---
description: Stellt die unterstützten Anzeigefunktionen des Monitors dar.
ms.assetid: 28eeead3-8fb9-4720-8d93-1c6757dfb31b
title: Supporteddisplayfeaturesdescriptor-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SupportedDisplayFeaturesDescriptor
- SupportedDisplayFeaturesDescriptor.ActiveOffSupported
- SupportedDisplayFeaturesDescriptor.DisplayType
- SupportedDisplayFeaturesDescriptor.GTFSupported
- SupportedDisplayFeaturesDescriptor.HasPreferredTimingMode
- SupportedDisplayFeaturesDescriptor.sRGBSupported
- SupportedDisplayFeaturesDescriptor.StandbySupported
- SupportedDisplayFeaturesDescriptor.SuspendSupported
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 30350d477533b7e51ba8b3130c5a24d81c12f10e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356836"
---
# <a name="supporteddisplayfeaturesdescriptor-class"></a>Supporteddisplayfeaturesdescriptor-Klasse

Der **supporteddisplayfeaturesdescriptor** stellt die unterstützten Anzeigefunktionen des Monitors dar. Die Informationen in dieser Klasse entsprechen den Daten in der Videoeingabe Definition des standardmäßigen Enhanced Display Identification Data (E-EDID)-Standards von Video Electronics Standard Association (VESA).

## <a name="syntax"></a>Syntax

``` syntax
class SupportedDisplayFeaturesDescriptor
{
  boolean ActiveOffSupported;
  uint8   DisplayType;
  boolean GTFSupported;
  boolean HasPreferredTimingMode;
  boolean sRGBSupported;
  boolean StandbySupported;
  boolean SuspendSupported;
};
```

## <a name="members"></a>Member

Die **supporteddisplayfeaturesdescriptor** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **supporteddisplayfeaturesdescriptor** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Activeoffsupported**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Unterstützung für aktive und sehr geringe Leistung. Die Anzeige beansprucht weniger Leistung, wenn Sie ein Zeit Steuerungs Signal empfängt, das außerhalb des deklarierten aktiven Betriebsbereichs liegt. Die Anzeige wird auf den normalen Vorgang zurückgesetzt, wenn das Zeit Steuerungs Signal in den normalen Betriebsbereich zurückkehrt. Beispiele für Zeit Steuerungs Signale außerhalb des normalen Betriebsbereichs sind keine Synchronisierungs Signale oder kein Signal.

</dd> <dt>

**Display Type**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Typ der Anzeige für den Monitor. In der folgenden Tabelle sind die möglichen Werte aufgeführt.



| Wert                                                                              | Bedeutung                                 |
|------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>0 (0x0)</dt> </dl> | Monochrome/Graustufen Anzeige<br/> |
| <dl> <dt>1 (0x1)</dt> </dl> | RGB-Farbanzeige<br/>            |
| <dl> <dt>2 (0x2)</dt> </dl> | Nicht-RGB-multifarbanzeige<br/>   |



 

</dd> <dt>

**Unterstützt**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die Anzeige über eine Unterstützung von GTF verfügt **True** gibt an, dass die Anzeigezeit Angaben unterstützt, die auf dem standardmäßigen GTF-Parameter basieren.

</dd> <dt>

**Haspreferredtimingmode**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die Anzeige über einen bevorzugten Zeit Steuerungs Modus verfügt. **True** gibt an, dass der erste ausführliche Zeit Steuerungs Block den bevorzugten Zeit Steuerungs Modus des Monitors enthält. Die Verwendung des bevorzugten Zeit Steuerungs Modus ist für EDID v. 1.3 und höher erforderlich.

</dd> <dt>

**srgbsupported**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

**True** gibt an, dass die Anzeige sRGB unterstützt.

</dd> <dt>

**Standbysupported**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die Anzeige den VESA-Display-/DPMS-Standbymodus unterstützt. **True** gibt an, dass DPMS Standby unterstützt wird.

</dd> <dt>

**Suspendsupported**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die Anzeige das anbrechen der VESA-Anzeige Energie Verwaltung (DPMS) unterstützt. **True** gibt an, dass DPMS Suspend unterstützt wird.

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

 

 




