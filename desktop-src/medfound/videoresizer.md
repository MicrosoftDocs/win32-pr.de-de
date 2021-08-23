---
description: Ändern der Größe eines Videostreams.
ms.assetid: 4acd6366-1abf-43f3-b6c9-4ea17a335cec
title: Video Resizer DSP (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58d26dcc53baf38336656d870acc5583066e0816a0bf963217db1da54513ee18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119721320"
---
# <a name="video-resizer-dsp"></a>Video Resizer DSP

Ändern der Größe eines Videostreams.

## <a name="clsid"></a>CLSID

CLSID \_ CResizerDMO

## <a name="interfaces"></a>Schnittstellen

-   [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject)
-   [**VERALTENRealTimeClient**](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient)
-   [**VORRÜBERSETZUNGTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
-   [**Ipropertystore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)
-   [**IWMResizerProps**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmresizerprops)

## <a name="formats"></a>Formate

Der Video Resizer-DSP unterstützt die folgenden Eingabe-/Ausgabemedienuntertypen, wenn er als DirectX Media Object (DMO.

-   MEDIASUBTYPE \_ IYUV
-   MEDIASUBTYPE \_ YUY2
-   MEDIASUBTYPE \_ UY WIE
-   MEDIASUBTYPE \_ I420
-   MEDIASUBTYPE \_ RGB32
-   MEDIASUBTYPE \_ RGB24
-   MEDIASUBTYPE \_ RGB565
-   MEDIASUBTYPE \_ RGB8
-   MEDIASUBTYPE \_ RGB555
-   MEDIASUBTYPE \_ AYUV
-   MEDIASUBTYPE \_ V216
-   MEDIASUBTYPE \_ YV12

Der Video Resizer-DSP unterstützt die folgenden Eingabe-/Ausgabemedienuntertypen, wenn er als MFT (Media Foundation Transform) agiert.

-   MFVideoFormat \_ IYUV
-   MFVideoFormat \_ YUY2
-   MFVideoFormat \_ UY WIES
-   MFVideoFormat \_ I420
-   MFVideoFormat \_ RGB32
-   MFVideoFormat \_ RGB24
-   MFVideoFormat \_ RGB565
-   MFVideoFormat \_ RGB8
-   MFVideoFormat \_ RGB555
-   MFVideoFormat \_ AYUV
-   MFVideoFormat \_ V216
-   MFVideoFormat \_ YV12

## <a name="properties"></a>Eigenschaften

-   [MFPKEY \_ RESIZE \_ SRC \_ LEFT](mfpkey-resize-src-left.md)
-   [MFPKEY \_ RESIZE \_ SRC \_ TOP](mfpkey-resize-src-top.md)
-   [MFPKEY \_ RESIZE \_ SRC \_ WIDTH](mfpkey-resize-src-width.md)
-   [MFPKEY \_ RESIZE \_ SRC \_ HEIGHT](mfpkey-resize-src-height.md)
-   [MFPKEY \_ RESIZE \_ DST \_ LEFT](mfpkey-resize-dst-left.md)
-   [MFPKEY \_ RESIZE \_ DST \_ TOP](mfpkey-resize-dst-top.md)
-   [MFPKEY \_ RESIZE \_ DST \_ WIDTH](mfpkey-resize-dst-width.md)
-   [MFPKEY \_ RESIZE \_ DST \_ HEIGHT](mfpkey-resize-dst-height.md)
-   [MFPKEY \_ RESIZE \_ QUALITY](mfpkey-resize-quality.md)
-   [MFPKEY \_ RESIZE \_ INTERLACE](mfpkey-resize-interlace.md)
-   [MFPKEY \_ RESIZE \_ GEOMAPX](mfpkey-resize-geomapx.md)
-   [MFPKEY \_ RESIZE \_ GEOMAPY](mfpkey-resize-geomapy.md)
-   [MFPKEY \_ RESIZE \_ GEOMAPWIDTH](mfpkey-resize-geomapwidth.md)
-   [MFPKEY \_ RESIZE \_ GEOMAPHEIGHT](mfpkey-resize-geomapheight.md)
-   [MFPKEY \_ RESIZE \_ MINAPX](mfpkey-resize-minapx.md)
-   [MFPKEY \_ RESIZE \_ MINAPY](mfpkey-resize-minapy.md)
-   [MFPKEY \_ RESIZE \_ MINAPWIDTH](mfpkey-resize-minapwidth.md)
-   [MFPKEY \_ RESIZE \_ MINAPHEIGHT](mfpkey-resize-minapheight.md)
-   [MFPKEY \_ RESIZE \_ PANSCANAPX](mfpkey-resize-panscanapx.md)
-   [MFPKEY \_ RESIZE \_ PANSCANAPY](mfpkey-resize-panscanapy.md)
-   [MFPKEY \_ RESIZE \_ PANSCANAPWIDTH](mfpkey-resize-panscanapwidth.md)
-   [MFPKEY \_ RESIZE \_ PANSCANAPHEIGHT](mfpkey-resize-panscanapheight.md)
-   [MFPKEY \_ PIXELASPECTRATIO](mfpkey-pixelaspectratio.md)

## <a name="remarks"></a>Hinweise

Der Video Resizer-DSP wird als COM-Objekt implementiert, das als DMO MFT fungieren kann. Das -Objekt verfügt über einen einzelnen Klassenbezeichner (CLSID), unabhängig davon, ob es als DMO oder MFT fungiert. Informationen dazu, wann ein DSP als DMO oder MFT fungiert, finden Sie unter [Digital Signal Processors](windowsmediadigitalsignalprocessors.md).

Die GUIDs (Globally Unique Identifiers) für RGB-Medienuntertypen unterscheiden sich je nachdem, ob ein DSP als DMO oder MFT agiert. Die GUIDs für Nicht-RGB-Medienuntertypen sind identisch, unabhängig davon, ob ein DSP als DMO oder MFT agiert. Informationen zu den GUIDs, die Medienuntertypen darstellen, finden Sie unter [Video Subtype GUIDs](video-subtype-guids.md).

Dieser DSP kann das Videobild sowohl zuschneiden als auch skalieren. Das Format des Ausgabetyps muss mit dem Format des Eingabetyps übereinstimmen. Der DSP führt keine Farbraumkonvertierungen durch.

Vor dem Festlegen des Ausgabetyps können Sie eine der folgenden Regionen definieren, indem Sie die in dieser Tabelle aufgeführten Eigenschaften verwenden.



| Region                   | Eigenschaften                                                                                                                                                       |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Quellrechteck         | MFPKEY \_ RESIZE \_ SRC \_ LEFT<br/> MFPKEY \_ RESIZE \_ SRC \_ TOP<br/> MFPKEY \_ RESIZE \_ SRC \_ WIDTH<br/> MFPKEY \_ RESIZE \_ SRC \_ HEIGHT<br/>            |
| Zielrechteck    | MFPKEY \_ RESIZE \_ DST \_ LEFT<br/> MFPKEY \_ RESIZE \_ DST \_ TOP<br/> MFPKEY \_ RESIZE \_ DST \_ WIDTH<br/> MFPKEY \_ RESIZE \_ DST \_ HEIGHT<br/>            |
| Geometrische Öffnung       | MFPKEY \_ RESIZE \_ GEOMAPX<br/> MFPKEY \_ RESIZE \_ GEOMAPY<br/> MFPKEY \_ RESIZE \_ GEOMAPWIDTH<br/> MFPKEY \_ RESIZE \_ GEOMAPHEIGHT<br/>             |
| Minimale Anzeigeblende | MFPKEY \_ RESIZE \_ MINAPX<br/> MFPKEY \_ RESIZE \_ MINAPY<br/> MFPKEY \_ RESIZE \_ MINAPWIDTH<br/> MFPKEY \_ RESIZE \_ MINAPHEIGHT<br/>                 |
| Schwenk-/Scanbereich          | MFPKEY \_ RESIZE \_ PANSCANAPX<br/> MFPKEY \_ RESIZE \_ PANSCANAPY<br/> MFPKEY \_ RESIZE \_ PANSCANAPWIDTH<br/> MFPKEY \_ RESIZE \_ PANSCANAPHEIGHT<br/> |



 

In jedem Fall müssen Sie alle zugeordneten Eigenschaften festlegen, damit die Einstellung wirksam wird.

Der DSP kopiert den Teil des Quellbilds, der durch das Quellrechteck definiert ist, und streckt oder komprimiert ihn auf das Zielrechteck im Ausgabepuffer. Die Quell- und Zielrechtecke müssen nicht die gleiche Größe haben. Die Framegröße im Ausgabemedientyp muss groß genug sein, um das Zielrechteck aufzunehmen.

Die geometrische Blende, die minimale Anzeigeblende und der Schwenk-/Scanbereich wirken sich nicht darauf aus, wie die Größe des Videos durch den DSP geändert wird. Sie können sich jedoch darauf auswirken, wie die Downstreamkomponente den Videoframe interpretiert. Insbesondere verwendet der erweiterte Videorenderer (EVR) diese Werte, wenn er das Seitenverhältnis des Bilds und den Anzeigebereich berechnet.

Wenn Sie Media Foundation Medientypen verwenden, können Sie die geometrische Blende, die minimale Anzeigeblende und die Schwenk-/Scan-Bereiche direkt im Ausgabemedientyp festlegen. Wenn Sie andere Medientypen DMO, legen Sie sie mithilfe der Eigenschaften fest.

Weitere Informationen finden Sie in den folgenden Themen:

-   [**MF \_ MT \_ GEOMETRIC \_ APERTURE**](mf-mt-geometric-aperture-attribute.md)
-   [**MF \_ MT \_ MINIMUM \_ DISPLAY \_ APERTURE**](mf-mt-minimum-display-aperture-attribute.md)
-   [**MF \_ MT \_ PAN \_ SCAN \_ APERTURE**](mf-mt-pan-scan-aperture-attribute.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vidreszr.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Digitale Signalprozessoren](windowsmediadigitalsignalprocessors.md)
</dt> </dl>

 

 
