---
description: Ändert die Framerate eines Videodaten Stroms.
ms.assetid: a66b9c52-a015-41d2-b27a-3ce6a4d95be9
title: Frame Rate Konverter DSP (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6197c29e9e753db6f327aa8b2797ba04131448d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749232"
---
# <a name="frame-rate-converter-dsp"></a>Frame Rate Konverter DSP

Ändert die Framerate eines Videodaten Stroms.

## <a name="clsid"></a>CLSID

CLSID \_ cframerateconvertdmo

## <a name="interfaces"></a>Schnittstellen

-   **Imediaobject**
-   **IMF-Transformation**
-   **IPropertyStore**

## <a name="formats"></a>Formate

-   ARGB 32
-   RGB 24
-   RGB 32
-   RGB 555
-   RGB 565
-   Ayuv
-   IYUV
-   UYVY
-   Y211
-   Y411
-   Im y41p
-   Im YUY2
-   Yuyv
-   YV12
-   Im yvyu

## <a name="properties"></a>Eigenschaften

-   [mfpkey, \_ \_ inputframerate](mfpkey-conv-inputframerate.md)
-   [mfpkey-" \_ \_ outputframerate"](mfpkey-conv-outputframerate.md)

## <a name="remarks"></a>Bemerkungen

Dieser DSP ändert die Framerate, indem Frames wiederholt oder gelöscht werden.

Standardmäßig ruft der DSP die Frameraten aus den Medientypen ab. Optional können Sie die Frameraten angeben, indem Sie die Eigenschaften "mfpkey", " \_ \_ inputframerate" und "mfpkey" für " \_ \_ outputframerate" festlegen. Diese Werte überschreiben die im Medientyp angegebene Framerate. Wenn Sie diesen DSP jedoch innerhalb der Media Foundation Pipeline verwenden, sollten Sie diese Eigenschaften nicht festlegen.

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

 

 




