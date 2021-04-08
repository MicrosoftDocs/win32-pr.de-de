---
description: Passt die Farbmerkmale eines Videostreams an.
ms.assetid: 738c1f0c-8417-4b12-a7f1-9bbf3c7e9dd3
title: Color Control Transform DSP (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b94c8314bfd2be85a3bbc392bfa0e83767ff0b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749345"
---
# <a name="color-control-transform-dsp"></a>Farb Steuerungs Transformation (DSP)

Passt die Farbmerkmale eines Videostreams an.

## <a name="clsid"></a>CLSID

CLSID \_ ccolorcontroldmo

## <a name="interfaces"></a>Schnittstellen

-   **Imediaobject**
-   **IMF-Transformation**
-   **IPropertyStore**

## <a name="formats"></a>Formate

-   RGB 24
-   RGB 32
-   RGB 555
-   RGB 565
-   Ayuv
-   UYVY
-   Im YUY2
-   YV12

## <a name="properties"></a>Eigenschaften

-   [mfpkey- \_ Farb \_ Helligkeit](mfpkey-color-brightness.md)
-   [Kontrast zwischen mfpkey- \_ Farbe \_](mfpkey-color-contrast.md)
-   [mfpkey \_ - \_ farbfarbton](mfpkey-color-hue.md)
-   [\_Farbsättigung für mfpkey \_](mfpkey-color-saturation.md)

## <a name="remarks"></a>Bemerkungen

Dieser DSP ändert den Inhalt des Videodaten Stroms. Bei der Wiedergabe können Sie mit der **imfvideoprocessor** -Schnittstelle, die die Videoverarbeitung auf der Grafikkarte steuert, eine effizientere Wirkung erzielen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Mfvdsp.dll</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Digitale Signal Prozessoren](windowsmediadigitalsignalprocessors.md)
</dt> </dl>

 

 




