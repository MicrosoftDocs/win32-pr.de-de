---
description: Stellt die grundlegenden Anzeigefunktionen eines Computermonitors dar.
ms.assetid: 08405e7f-7824-4e44-9f37-da9bb5619cd6
title: WmiMonitorBasicDisplayParams-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorBasicDisplayParams
- WmiMonitorBasicDisplayParams.Active
- WmiMonitorBasicDisplayParams.DisplayTransferCharacteristic
- WmiMonitorBasicDisplayParams.InstanceName
- WmiMonitorBasicDisplayParams.MaxHorizontalImageSize
- WmiMonitorBasicDisplayParams.MaxVerticalImageSize
- WmiMonitorBasicDisplayParams.SupportedDisplayFeatures
- WmiMonitorBasicDisplayParams.VideoInputType
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 958eb9134062d5380a2afda77eeaad3034a2da7430d2f6a3094916ceae211e4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117926782"
---
# <a name="wmimonitorbasicdisplayparams-class"></a>WmiMonitorBasicDisplayParams-Klasse

Die **WMI-Klasse WmiMonitorBasicDisplayParams** stellt die grundlegenden Anzeigefunktionen eines Computermonitors dar. Der Wert der **VideoInputType-Eigenschaft** gibt an, ob der Monitor analog oder digital ist. Daten in dieser Klasse entsprechen Daten im Block Grundlegende Anzeigeparameter/-features des E-EDID-Standards (Enhanced Extended Display Identification Data) von Video Electronics Standard Association (VESA).

## <a name="syntax"></a>Syntax

``` syntax
class WmiMonitorBasicDisplayParams : MSMonitorClass
{
  boolean                            Active;
  uint8                              DisplayTransferCharacteristic;
  string                             InstanceName;
  uint8                              MaxHorizontalImageSize;
  uint8                              MaxVerticalImageSize;
  SupportedDisplayFeaturesDescriptor SupportedDisplayFeatures;
  uint8                              VideoInputType;
};
```

## <a name="members"></a>Member

Die **WmiMonitorBasicDisplayParams-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **WmiMonitorBasicDisplayParams-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Aktiv**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt den aktiven Monitor an.

</dd> <dt>

**DisplayTransferCharacteristic**
</dt> <dd> <dl> <dt>

Datentyp: **uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Anzeigeübertragungseigenschaft (100 \* Gamma-100).

</dd> <dt>

**InstanceName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Schlüssel**
</dt> </dl>

Name der spezifischen Monitorinstanz.

</dd> <dt>

**MaxHorizontalImageSize**
</dt> <dd> <dl> <dt>

Datentyp: **uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Maximale horizontale Bildgröße in Zentimetern. Weitere Informationen finden Sie in den Hinweisen.

</dd> <dt>

**MaxVerticalImageSize**
</dt> <dd> <dl> <dt>

Datentyp: **uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Maximale vertikale Bildgröße in Zentimetern. Weitere Informationen finden Sie in den Hinweisen.

</dd> <dt>

**SupportedDisplayFeatures**
</dt> <dd> <dl> <dt>

Datentyp: **[ **SupportedDisplayFeaturesDescriptor**](supporteddisplayfeaturesdescriptor.md)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Anzeigen von Funktionen, die vom Monitor unterstützt werden.

</dd> <dt>

**VideoInputType**
</dt> <dd> <dl> <dt>

Datentyp: **uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Videoeingabetyp.



| Wert                                                                              | Bedeutung            |
|------------------------------------------------------------------------------------|--------------------|
| <dl> <dt>0 (0x0)</dt> </dl> | Analoge<br/>  |
| <dl> <dt>1 (0x1)</dt> </dl> | Digital<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Hinweise

**MaxHorizontalImageSize** und **MaxVerticalImageSize** stellen die maximalen Bilddimensionen dar, die der Monitor für den gesamten Satz unterstützter Zeitsteuerungs- und Formatkombinationen ordnungsgemäß anzeigen kann. Die maximale Bilddimension wird durch DEN VESA Video Image Area Definition (VIAD) Standard definiert und auf die nächste 10000000000000-Fläche gerundet. Das Hostcomputersystem kann diese Daten verwenden, um die Bildgröße und das Seitenverhältnis auszuwählen, die ordnungsgemäß skalierten Text zulassen. Beachten Sie, dass das System keine Annahmen über die Anzeigegröße trifft, wenn eines oder beide dieser Felder 0 (null) sind. Beispielsweise kann die Größe einer Projektionsanzeige unbestimmt sein.

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

 

 




