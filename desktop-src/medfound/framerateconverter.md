---
description: Ändert die Bildfrequenz eines Videostreams.
ms.assetid: a66b9c52-a015-41d2-b27a-3ce6a4d95be9
title: Frame Rate Converter DSP (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ca4a728f37caa43ee99a0d293d5113e9c26cfb1dcfe51f399482fb614283737
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119600490"
---
# <a name="frame-rate-converter-dsp"></a>Bildfrequenzkonverter-DSP

Ändert die Bildfrequenz eines Videostreams.

## <a name="clsid"></a>CLSID

CLSID \_ CFrameRateConvertDmo

## <a name="interfaces"></a>Schnittstellen

-   **IMediaObject**
-   **VORRÜBERSETZUNGTransform**
-   **Ipropertystore**

## <a name="formats"></a>Formate

-   ARGB 32
-   RGB 24
-   RGB 32
-   RGB 555
-   RGB 565
-   AYUV
-   IYUV
-   UYVIG
-   Y211
-   Y411
-   Y41P
-   YUY2
-   YUYV
-   YV12
-   YVKY

## <a name="properties"></a>Eigenschaften

-   [MFPKEY \_ CONV \_ INPUTFRAMERATE](mfpkey-conv-inputframerate.md)
-   [MFPKEY \_ CONV \_ OUTPUTFRAMERATE](mfpkey-conv-outputframerate.md)

## <a name="remarks"></a>Hinweise

Dieser DSP ändert die Bildfrequenz durch Wiederholen oder Löschen von Frames.

Standardmäßig ruft der DSP die Bildraten aus den Medientypen ab. Optional können Sie die Frameraten angeben, indem Sie die Eigenschaften MFPKEY \_ CONV \_ INPUTFRAMERATE und MFPKEY \_ CONV \_ OUTPUTFRAMERATE festlegen. Diese Werte überschreiben die im Medientyp gegebene Bildfrequenz. Wenn Sie diesen DSP jedoch innerhalb der Media Foundation verwenden, sollten Sie diese Eigenschaften nicht festlegen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Mfvdsp.dll</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Digitale Signalprozessoren](windowsmediadigitalsignalprocessors.md)
</dt> </dl>

 

 




