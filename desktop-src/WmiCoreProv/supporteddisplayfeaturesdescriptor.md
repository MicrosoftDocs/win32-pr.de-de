---
description: Stellt die unterstützten Anzeigefunktionen des Monitors dar.
ms.assetid: 28eeead3-8fb9-4720-8d93-1c6757dfb31b
title: SupportedDisplayFeaturesDescriptor-Klasse
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
ms.openlocfilehash: a9e71eeda4ab47cba5e88a548421c89815b7d0d87d511709b9a73573e2582077
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118321536"
---
# <a name="supporteddisplayfeaturesdescriptor-class"></a>SupportedDisplayFeaturesDescriptor-Klasse

**SupportedDisplayFeaturesDescriptor** stellt die unterstützten Anzeigefunktionen des Monitors dar. Die Informationen in dieser Klasse entsprechen den Daten in der Videoeingabedefinition des E-EDID-Standards (Enhanced Extended Display Identification Data) der Video Electronics Standard Association (VESA).

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

Die **SupportedDisplayFeaturesDescriptor-Klasse** verfügt über folgende Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **SupportedDisplayFeaturesDescriptor-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**ActiveOffSupported**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Unterstützung für aktiv ausgeschaltete und sehr niedrige Stromversorgung. Die Anzeige verbraucht weniger Leistung, wenn sie ein Zeitsteuerungssignal empfängt, das sich außerhalb des deklarierten aktiven Betriebsbereichs befindet. Die Anzeige wird auf den normalen Betrieb zurückgesetzt, wenn das Zeitsteuerungssignal in den normalen Betriebsbereich zurückkehrt. Beispiele für Zeitsteuerungssignale außerhalb des normalen Betriebsbereichs sind keine Synchronisierungssignale oder kein DE-Signal.

</dd> <dt>

**DisplayType**
</dt> <dd> <dl> <dt>

Datentyp: **uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Anzeigetyp für den Monitor. In der folgenden Tabelle sind mögliche Werte aufgeführt.



| Wert                                                                              | Bedeutung                                 |
|------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>0 (0x0)</dt> </dl> | Monocolore/Graustufenanzeige<br/> |
| <dl> <dt>1 (0x1)</dt> </dl> | RGB-Farbanzeige<br/>            |
| <dl> <dt>2 (0x2)</dt> </dl> | Multicolor-Anzeige ohne RGB<br/>   |



 

</dd> <dt>

**GTFSupported**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die Anzeige GTF-Unterstützung hat. **True** gibt an, dass die Anzeige Zeitsteuerungen unterstützt, die auf dem GTF-Standard basieren, indem gtf-Standardparameterwerte verwendet werden.

</dd> <dt>

**HasPreferredTimingMode**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die Anzeige über einen bevorzugten Zeitsteuerungsmodus verfügt. **True** gibt an, dass der erste ausführliche Zeitsteuerungsblock den bevorzugten Zeitsteuerungsmodus des Monitors enthält. Die Verwendung des bevorzugten Zeitsteuerungsmodus ist für EDID v.1.3 und höher erforderlich.

</dd> <dt>

**sRGBSupported**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

**True** gibt an, dass die Anzeige sRGB unterstützt.

</dd> <dt>

**StandbySupported**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die Anzeige den Standbymodus "VESA Display Power Management Signaling (DPMS)" unterstützt. **True** gibt an, dass der DPMS-Standbymodus unterstützt wird.

</dd> <dt>

**SuspendSupported**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die Anzeige das Anhalten der VESA Display Power Management Signaling (DPMS) unterstützt. **True** gibt an, dass dpms suspend unterstützt wird.

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

 

 




