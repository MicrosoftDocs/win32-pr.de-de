---
description: Tragbare Windows-Geräte unterstützen die folgenden Abbild Eigenschaften.
ms.assetid: fb1707a7-16b0-4073-b21d-2ba2f4fd76f7
title: Bildeigenschaften (portabledevice. h)
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
ms.openlocfilehash: 959a008d9c30991058226e52db6e45ed417ee6e4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371562"
---
# <a name="image-properties"></a>Bildeigenschaften

Tragbare Windows-Geräte unterstützen die folgenden Abbild Eigenschaften.



| Eigenschaft                                                                                                                                       | VarType     | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Bittiefe des WPD- \_ Bilds \_**                                                                                                                       | **VT \_ UI4** | Die Bittiefe des Bilds.                                                                                                                                                                                                                                                                                                                     |
| <span id="wpd_image_color_corrected_status"></span><span id="WPD_IMAGE_COLOR_CORRECTED_STATUS"></span>**Status der \_ \_ \_ korrigierten WPD-Bild Farbe \_** | **VT \_ UI4** | Eine mit der [**WPD- \_ Farbe \_ korrigierte \_ \_ statusvalues**](wpd-color-corrected-status-values.md) -Enumeration, die angibt, ob die Datei farblich korrigiert wurde. Dadurch wird verhindert, dass mehrere Geräte bei der Nachbearbeitung automatisch eine Farbkorrektur des Bilds vornehmen.<br/>                                                                       |
| **ausgeschnittener WPD- \_ Image \_ \_ Status**                                                                                                                | **VT \_ UI4** | Eine von [**WPD ausgeschnittene \_ \_ statuswertenenumeration \_**](wpd-cropped-status-values.md) , die angibt, ob die Datei abgeschnitten wurde. Dadurch wird verhindert, dass mehrere Geräte das Image während der Nachbearbeitung automatisch zuschneiden.<br/>                                                                                                        |
| **Index für WPD- \_ Image verfügbar \_ \_**                                                                                                                | **VT \_ UI4** | Ein-Wert, der die Einstellungen der Folien Geschwindigkeit identifiziert, wenn dieses Bild aufgezeichnet wurde. Die Einstellungen entsprechen den ISO-Bezeichnungen von ASA/DIN.<br/> In der Regel unterstützt ein Gerät diskrete Enumerationswerte, aber eine kontinuierliche Kontrolle über einen Bereich ist möglich.<br/> Der Wert 0xFFFFFFFF entspricht der automatischen ISO-Einstellung.<br/> |
| **Anzeigezeit für WPD- \_ Image \_ \_**                                                                                                                 | **VT \_ UI4** | Gibt die Auslösegeschwindigkeit des Geräts an, als das Abbild erfasst wurde. Einheiten werden in Sekunden von 10000 skaliert.<br/>                                                                                                                                                                                                                        |
| **WPD- \_ Image- \_ Nummer**                                                                                                                        | **VT \_ UI4** | Gibt die Einstellung für die Öffnung des Bilds an, wenn dieses Bild aufgezeichnet wurde. Einheiten sind gleich der durch 100 skalierten f-Nummer.<br/>                                                                                                                                                                                                              |
| **horizontale Auflösung des WPD- \_ Bilds \_ \_**                                                                                                         | **VT \_ R8**  | Gibt die horizontale Auflösung eines Bilds in dpi (dots per inch) an.                                                                                                                                                                                                                                                                       |
| **vertikale Auflösung des WPD- \_ Bilds \_ \_**                                                                                                           | **VT \_ R8**  | Gibt die vertikale Auflösung eines Bilds in dpi (dots per inch) an.                                                                                                                                                                                                                                                                         |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Portabledevice. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**WPD-Eigenschaften und-Attribute**](properties-and-attributes.md)
</dt> </dl>

 

 




