---
description: Windows Portable Geräte unterstützen die folgenden Bildeigenschaften.
ms.assetid: fb1707a7-16b0-4073-b21d-2ba2f4fd76f7
title: Bildeigenschaften (PortableDevice.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Image
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 0d2ebe552a66dadf6b9bec6a0a741d85e1c7f1f018ef108e36ec1bb3cb4b6165
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118430759"
---
# <a name="image-properties"></a>Bildeigenschaften

Windows Portable Geräte unterstützen die folgenden Bildeigenschaften.



| Eigenschaft                                                                                                                                       | VarType     | Beschreibung                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **WPD \_ IMAGE \_ BITDEPTH**                                                                                                                       | **VT \_ UI4** | Die Bittiefe des Bilds.                                                                                                                                                                                                                                                                                                                     |
| <span id="wpd_image_color_corrected_status"></span><span id="WPD_IMAGE_COLOR_CORRECTED_STATUS"></span>**\_WPD-BILDFARBE \_ \_ \_ KORRIGIERTER STATUS** | **VT \_ UI4** | Eine [**WPD \_ COLOR CORRECTED \_ STATUS \_ \_ VALUES-Enumeration,**](wpd-color-corrected-status-values.md) die angibt, ob die Datei farblich korrigiert wurde. Dadurch wird verhindert, dass mehrere Geräte das Bild während der Nachbearbeitung automatisch farblich korrigieren.<br/>                                                                       |
| **\_WPD-BILD– \_ ZUSCHNEIDESTATUS \_**                                                                                                                | **VT \_ UI4** | Eine [**WPD \_ CROPPED \_ STATUS \_ VALUES-Enumeration,**](wpd-cropped-status-values.md) die angibt, ob die Datei zugeschnitten wurde. Dadurch wird verhindert, dass mehrere Geräte das Bild während der Nachbearbeitung automatisch zuschneiden.<br/>                                                                                                        |
| **WPD \_ IMAGE \_ EXPOSURE \_ INDEX**                                                                                                                | **VT \_ UI4** | Ein -Wert, der die Einstellungen für die Filmgeschwindigkeit identifiziert, als dieses Bild erfasst wurde. Die Einstellungen entsprechen den ISO-Bezeichnungen von ASA/DIN.<br/> In der Regel unterstützt ein Gerät diskrete aufzählte Werte, aber eine kontinuierliche Kontrolle über einen Bereich ist möglich.<br/> Der Wert 0xFFFFFFFF der automatischen ISO-Einstellung entspricht.<br/> |
| **\_ \_ WPD-BILDBELICHTUNGSZEIT \_**                                                                                                                 | **VT \_ UI4** | Gibt die Geschwindigkeit des Geräts an, als dieses Bild erfasst wurde. Einheiten werden in Sekunden um 10.000 skaliert.<br/>                                                                                                                                                                                                                        |
| **WPD \_ IMAGE \_ FNUMBER**                                                                                                                        | **VT \_ UI4** | Identifiziert die Öffnungseinstellung des Ziels, als dieses Bild erfasst wurde. Einheiten sind gleich der f-Zahl, die um 100 skaliert wird.<br/>                                                                                                                                                                                                              |
| **\_WPD-BILD \_ – HORIZONTALE \_ AUFLÖSUNG**                                                                                                         | **VT \_ R8**  | Gibt die horizontale Auflösung eines Bilds in DPI (Dots per Inch) an.                                                                                                                                                                                                                                                                       |
| **\_WPD-BILD \_ – VERTIKALE \_ AUFLÖSUNG**                                                                                                           | **VT \_ R8**  | Gibt die vertikale Auflösung eines Bilds in DPI (Dots per Inch) an.                                                                                                                                                                                                                                                                         |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**WPD-Eigenschaften und -Attribute**](properties-and-attributes.md)
</dt> </dl>

 

 




