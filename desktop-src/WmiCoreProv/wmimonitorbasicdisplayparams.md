---
description: Stellt die grundlegenden Anzeigefunktionen eines Computermonitors dar.
ms.assetid: 08405e7f-7824-4e44-9f37-da9bb5619cd6
title: Wmimonitorbasicdisplaypara-Klasse
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
ms.openlocfilehash: e457757a3542bbfc8ded7536396458ef3e592714
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359425"
---
# <a name="wmimonitorbasicdisplayparams-class"></a>Wmimonitorbasicdisplaypara-Klasse

Die **wmimonitorbasicdisplayparser** -WMI-Klasse stellt die grundlegenden Anzeigefunktionen eines Computermonitors dar. Der Wert der **videoinputtype** -Eigenschaft gibt an, ob der Monitor Analog oder Digital ist. Die Daten in dieser Klasse entsprechen den Daten im grundlegenden Anzeige Parameter/Features-Block des Video Electronics Standard Association (VESA) Enhanced Extended Display Identification Data (E-EDID) Standard.

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

Die **wmimonitorbasicdisplayparser** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **wmimonitorbasicdisplayparser** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Aktiv**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt den aktiven Monitor an.

</dd> <dt>

**Display Transfer Merkmal**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Übertragungs Merkmal anzeigen (100 \* Gamma-100).

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

**Maxhorizontalimagesize**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Maximale horizontale Bildgröße in Zentimeter. Weitere Informationen finden Sie in den Hinweisen.

</dd> <dt>

**Maxverticalimagesize**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Maximale vertikale Bildgröße in Zentimetern. Weitere Informationen finden Sie in den Hinweisen.

</dd> <dt>

**Supporteddisplayfeatures**
</dt> <dd> <dl> <dt>

Datentyp: **[ **supporteddisplayfeaturesdescriptor**](supporteddisplayfeaturesdescriptor.md)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Zeigt die vom Monitor unterstützten Funktionen an.

</dd> <dt>

**Videoinputtype**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Video Eingabetyp.



| Wert                                                                              | Bedeutung            |
|------------------------------------------------------------------------------------|--------------------|
| <dl> <dt>0 (0x0)</dt> </dl> | Ges<br/>  |
| <dl> <dt>1 (0x1)</dt> </dl> | Digital<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

**Maxhorizontalimagesize** und **maxverticalimagesize** stellen die maximalen Bild Dimensionen dar, die der Monitor für den gesamten Satz unterstützter Zeitachsen-und Format Kombinationen korrekt anzeigen kann. Die maximale Image Dimension wird durch einen viad-Standard (Video Image Area Definition) definiert und auf den nächsten Zentimeter gerundet. Das Host Computersystem kann diese Daten verwenden, um die Abbild Größe und das Seitenverhältnis auszuwählen, das den ordnungsgemäßen skalierten Text zulässt. Beachten Sie, dass das System keine Annahmen über die Anzeige Größe gibt, wenn eines oder beide Felder NULL sind. Beispielsweise kann die Größe einer Projektions Anzeige nicht bestimmt werden.

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

 

 




