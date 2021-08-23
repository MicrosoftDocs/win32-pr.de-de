---
description: Passt die Farbmerkmale eines Videostreams an.
ms.assetid: 738c1f0c-8417-4b12-a7f1-9bbf3c7e9dd3
title: Color Control Transform DSP (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c51321a8ffd725306f570619b9bcbe70fe7160e784358ce265157145b40347e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119606210"
---
# <a name="color-control-transform-dsp"></a>Farbsteuerelementtransformations-DSP

Passt die Farbmerkmale eines Videostreams an.

## <a name="clsid"></a>CLSID

CLSID \_ CColorControlDmo

## <a name="interfaces"></a>Schnittstellen

-   **IMediaObject**
-   **ÜBERTRANSFORM**
-   **Ipropertystore**

## <a name="formats"></a>Formate

-   RGB 24
-   RGB 32
-   RGB 555
-   RGB 565
-   AYUV
-   UYVY
-   YUY2
-   YV12

## <a name="properties"></a>Eigenschaften

-   [MFPKEY \_ COLOR \_ BRIGHTNESS](mfpkey-color-brightness.md)
-   [\_ \_ MFPKEY-FARBKONTRAST](mfpkey-color-contrast.md)
-   [MFPKEY \_ COLOR \_ HUE](mfpkey-color-hue.md)
-   [\_MFPKEY-FARBSÄTTIGUNG \_](mfpkey-color-saturation.md)

## <a name="remarks"></a>Hinweise

Dieser DSP ändert den Inhalt des Videostreams. Für die Wiedergabe können Sie ähnliche Effekte möglicherweise effizienter erzielen, indem Sie die **SCHNITTSTELLE "DEBITVideoProcessor"** verwenden, die die Videoverarbeitung auf der Grafikkarte steuert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Mfvdsp.dll</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Digitale Signalprozessoren](windowsmediadigitalsignalprocessors.md)
</dt> </dl>

 

 




