---
description: Stellt die Farbmerkmale der International Commission on Illumination (CIE) eines Computermonitors dar.
ms.assetid: 476aefae-11c0-46be-a2bb-83fbafd70421
title: Wmimonitorcolorcharacteristics-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorColorCharacteristics
- WmiMonitorColorCharacteristics.Active
- WmiMonitorColorCharacteristics.Blue
- WmiMonitorColorCharacteristics.DefaultWhite
- WmiMonitorColorCharacteristics.Green
- WmiMonitorColorCharacteristics.InstanceName
- WmiMonitorColorCharacteristics.Red
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 9fbb7d56e56519576d257b077311a144e923d6bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346508"
---
# <a name="wmimonitorcolorcharacteristics-class"></a>Wmimonitorcolorcharacteristics-Klasse

Die **wmimonitorcolorcharacteristics** -Klasse stellt die Farbmerkmale der International Commission on Illumination (CIE) eines Computermonitors dar. Die Daten entsprechen den Daten im Block Color Characteristics der "Video Electronics Standard Association (VESA) Enhanced Enhanced Display Identification Data (E-EDID)"-Struktur.

## <a name="syntax"></a>Syntax

``` syntax
class WmiMonitorColorCharacteristics : MSMonitorClass
{
  boolean  Active;
  XYZinCIE Blue;
  XYZinCIE DefaultWhite;
  XYZinCIE Green;
  string   InstanceName;
  XYZinCIE Red;
};
```

## <a name="members"></a>Member

Die **wmimonitorcolorcharacteristics** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **wmimonitorcolorproperties** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Aktiv**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt den aktiven Monitor an.

</dd> <dt>

**Blau**
</dt> <dd> <dl> <dt>

Datentyp: **[ **xyzincie**](xyzincie.md)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

CIE-Koordinaten für blau, dargestellt durch eine Instanz der [**xyzincie**](xyzincie.md) -Klasse.

</dd> <dt>

**Defaultweiß**
</dt> <dd> <dl> <dt>

Datentyp: **[ **xyzincie**](xyzincie.md)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Standardmäßige weiße CIE-Koordinaten.

</dd> <dt>

**Grün**
</dt> <dd> <dl> <dt>

Datentyp: **[ **xyzincie**](xyzincie.md)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

CIE-Koordinaten für Grün, dargestellt durch eine Instanz der [**xyzincie**](xyzincie.md) -Klasse.

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

**Rot**
</dt> <dd> <dl> <dt>

Datentyp: **[ **xyzincie**](xyzincie.md)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

CIE-Koordinaten für Rot, dargestellt durch eine Instanz der [**xyzincie**](xyzincie.md) -Klasse.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die Werte von "Chromaticity" und "White Point" werden mithilfe eines Codierungs Formats als Bruchzahlen ausgedrückt. Dieses Format ist mit dem Tausendstel der Länge von 10 Bits genau. Das signifikanteste Bit (MSB) repräsentiert 2 ^-1, und das unwichtigste Bit (LSB) stellt 2 ^-10 Koeffizienten dar. Die Genauigkeit der gespeicherten Werte in der E-EDID v1. x-Struktur sollte auf +/-0,005 des tatsächlichen Werts zutreffen.

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

 

 




