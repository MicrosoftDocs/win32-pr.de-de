---
description: Konvertiert einen Videostream zwischen Farbformaten.
ms.assetid: 1c15dc2b-0e69-4d16-af02-8056a1eb2c5c
title: Farbkonverter-DSP (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e97db9f3131ed7cea9076255005149544363ba8d6b548736a211973cda3999d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117880662"
---
# <a name="color-converter-dsp"></a>Farbkonverter-DSP

Konvertiert einen Videostream zwischen Farbformaten.

## <a name="clsid"></a>CLSID

CLSID \_ CColorConvertDMO

## <a name="interfaces"></a>Schnittstellen

-   [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject)
-   [**VERALTENRealTimeClient**](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient)
-   [**ÜBERTRANSFORM**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
-   [**Ipropertystore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)
-   [IWMColorConvProps](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcolorconvprops)

## <a name="input-formats"></a>Eingabeformate

-   RGB 24
-   RGB 32
-   RGB 555
-   RGB 565
-   RGB 8
-   AYUV
-   I420
-   IYUV
-   NV11
-   NV12
-   UYVY
-   V216
-   V410
-   Y41P
-   Y41T
-   Y42T
-   YUY2
-   YV12
-   YVU9
-   YVYU

## <a name="output-formats"></a>Ausgabeformate

-   RGB 24
-   RGB 32
-   RGB 555
-   RGB 565
-   RGB 8
-   AYUV
-   I420
-   IYUV
-   NV11
-   NV12
-   UYVY
-   V216
-   V410
-   YUY2
-   YV12
-   YVYU

## <a name="properties"></a>Eigenschaften

-   [MFPKEY \_ COLORCONV \_ SRCLEFT](mfpkey-colorconv-srcleft.md)
-   [MFPKEY \_ COLORCONV \_ SRCTOP](mfpkey-colorconv-srctop.md)
-   [MFPKEY \_ COLORCONV \_ DSTLEFT](mfpkey-colorconv-dstleft.md)
-   [MFPKEY \_ COLORCONV \_ DSTTOP](mfpkey-colorconv-dsttop.md)
-   [MFPKEY \_ COLORCONV \_ WIDTH](mfpkey-colorconv-width.md)
-   [MFPKEY \_ COLORCONV \_ HEIGHT](mfpkey-colorconv-height.md)
-   [MFPKEY \_ \_ COLORCONV-MODUS](mfpkey-colorconv-mode.md)

## <a name="remarks"></a>Hinweise

Der Farbkonverter-DSP wird als COM-Objekt implementiert, das als DirectXMedia-Objekt (DMO) oder als Media Foundation Transform (MFT) fungieren kann. Das Objekt verfügt über einen einzelnen Klassenbezeichner (CLSID), unabhängig davon, ob es als DMO oder MFT fungiert. Informationen dazu, wann ein DSP als DMO oder MFT fungiert, finden Sie unter [Digitale Signalprozessoren.](windowsmediadigitalsignalprocessors.md)

Die GUIDs (Globally Unique Identifiers) für RGB-Medienuntertypen unterscheiden sich je nachdem, ob ein DSP als DMO oder MFT fungiert. Die GUIDs für Nicht-RGB-Medienuntertypen sind identisch, unabhängig davon, ob ein DSP als DMO oder MFT fungiert. Informationen zu den GUIDs, die Medienuntertypen darstellen, finden Sie unter [Video-Untertyp-GUIDs.](video-subtype-guids.md)

Standardmäßig kopiert dieser DSP das gesamte Quellimage in den Ausgabepuffer. Optional können Sie Quell- und Zielrechtecke angeben. Der DSP kopiert den durch das Quellrechteck definierten Teil des Quellbilds und schreibt ihn in das Zielrechteck im Ausgabepuffer. Der DSP führt keine Skalierung durch. Die Quell- und Zielrechtecke müssen die gleiche Größe haben. Die Quell- und Zielrechtecke dürfen die Grenzen des Videoframes nicht überschreiten.

Alle Eigenschaften außer [**MFPKEY \_ COLORCONV \_ MODE**](mfpkey-colorconv-mode.md) müssen in einer Gruppe festgelegt werden. Wenn Sie eine dieser Eigenschaften festlegen, müssen Sie alle anderen Eigenschaften festlegen. Andernfalls sind die Quell- und Zielrechtecke möglicherweise ungültig. In diesem Fall geben sowohl die [**METHODEN RECTANGLETransform::P rocessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) als [**auch IMediaObject::P rocessOutput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processoutput) **E \_ INVALIDARG** zurück.

Der Farbkonverter unterstützt nicht jede Kombination aus Eingabeformat und Ausgabeformat. In der Regel sollten Sie das medienformat festlegen, das Sie kennen, entweder Eingabe oder Ausgabe, und dann die verfügbaren Formate im entgegengesetzten Stream aufzählen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Colorcnv.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Digitale Signalprozessoren](windowsmediadigitalsignalprocessors.md)
</dt> </dl>

 

 
