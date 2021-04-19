---
description: Ändert die Größe eines Videodaten Stroms.
ms.assetid: 4acd6366-1abf-43f3-b6c9-4ea17a335cec
title: Video Resizer DSP (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff7826f21cadc6d30bc2b8b04bbcc741c2bf31bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106355561"
---
# <a name="video-resizer-dsp"></a>Video Resizer DSP

Ändert die Größe eines Videodaten Stroms.

## <a name="clsid"></a>CLSID

CLSID- \_ Erweiterung

## <a name="interfaces"></a>Schnittstellen

-   [**Imediaobject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject)
-   [**Imfrealtimeclient**](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient)
-   [**IMF-Transformation**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
-   [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)
-   [**Iwmresizer-Eigenschaften**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmresizerprops)

## <a name="formats"></a>Formate

Das Video Resizer DSP unterstützt die folgenden Eingabe-/ausgabemedienuntertypen, wenn diese als DirectX-Medienobjekt (DMO) fungieren.

-   mediasubtype \_ IYUV
-   Mediasubtype \_ im YUY2
-   mediasubtype \_ UYVY
-   Mediasubtype \_ I420
-   Mediasubtype \_ RGB32
-   Mediasubtype \_ RGB24
-   Mediasubtype \_ RGB565
-   Mediasubtype \_ RGB8
-   Mediasubtype \_ RGB555
-   mediasubtype \_ ayuv
-   Mediasubtype \_ V216
-   Mediasubtype \_ YV12

Das Video Resizer DSP unterstützt die folgenden Eingabe-/ausgabemedienuntertypen, wenn diese als Media Foundation Transform (MFT) fungieren.

-   MF-Format ( \_ IYUV)
-   MF-Format \_ im YUY2
-   MF-Format ( \_ UYVY)
-   MF-Format \_ I420
-   MF-Format \_ RGB32
-   MF-Format \_ RGB24
-   MF-Format \_ RGB565
-   MF-Format \_ RGB8
-   MF-Format \_ RGB555
-   MF-Format ( \_ ayuv)
-   MF-Format \_ V216
-   MF-Format \_ YV12

## <a name="properties"></a>Eigenschaften

-   [mfpkey- \_ Größenänderung für \_ src \_ left](mfpkey-resize-src-left.md)
-   [mfpkey- \_ Größenänderung, \_ \_ oben](mfpkey-resize-src-top.md)
-   [mfpkey- \_ Größe für \_ src- \_ Breite](mfpkey-resize-src-width.md)
-   [mfpkey- \_ Größenänderung für \_ src- \_ Höhe](mfpkey-resize-src-height.md)
-   [mfpkey- \_ Größe nach \_ \_ Links ändern](mfpkey-resize-dst-left.md)
-   [mfpkey \_ Größenänderung nach \_ \_ oben](mfpkey-resize-dst-top.md)
-   [mfpkey- \_ \_ DST- \_ Breite ändern](mfpkey-resize-dst-width.md)
-   [mfpkey- \_ \_ DST- \_ Höhe ändern](mfpkey-resize-dst-height.md)
-   [mfpkey- \_ Qualität der Größenänderung \_](mfpkey-resize-quality.md)
-   [mfpkey- \_ interspitze für die Größenänderung \_](mfpkey-resize-interlace.md)
-   [mfpkey \_ Ändern von \_ geomapx](mfpkey-resize-geomapx.md)
-   [mfpkey \_ Ändern der \_ geomapy](mfpkey-resize-geomapy.md)
-   [mfpkey \_ Ändern von \_ geomapwidth](mfpkey-resize-geomapwidth.md)
-   [mfpkey- \_ Größe für \_ geomapheight ändern](mfpkey-resize-geomapheight.md)
-   [mfpkey- \_ Größe ändern \_ minapx](mfpkey-resize-minapx.md)
-   [mfpkey- \_ Größe ändern \_](mfpkey-resize-minapy.md)
-   [mfpkey- \_ Größe ändern \_ minapwidth](mfpkey-resize-minapwidth.md)
-   [mfpkey-Wert für \_ \_ minapheight ändern](mfpkey-resize-minapheight.md)
-   [mfpkey- \_ Größe ändern von \_ panscanapx](mfpkey-resize-panscanapx.md)
-   [mfpkey \_ Resize \_ panscanapy](mfpkey-resize-panscanapy.md)
-   [mfpkey- \_ Größe ändern von \_ panscanapwidth](mfpkey-resize-panscanapwidth.md)
-   [mfpkey- \_ Größe ändern von \_ panscanapheight](mfpkey-resize-panscanapheight.md)
-   [mfpkey \_ pixelaspectratio](mfpkey-pixelaspectratio.md)

## <a name="remarks"></a>Bemerkungen

Das Video Resizer DSP ist als COM-Objekt implementiert, das als DMO oder MFT fungieren kann. Das-Objekt verfügt über einen einzelnen Klassen Bezeichner (CLSID), unabhängig davon, ob er als DMO oder MFT fungiert. Informationen dazu, wann ein DSP als DMO oder MFT fungiert, finden Sie unter [digitale Signal Prozessoren](windowsmediadigitalsignalprocessors.md).

Die global eindeutigen Bezeichner (GUIDs) für RGB-Medien Untertypen unterscheiden sich abhängig davon, ob ein DSP als DMO oder MFT fungiert. Die GUIDs für nicht-RGB-Medien Untertypen sind identisch, unabhängig davon, ob ein DSP als DMO oder MFT fungiert. Informationen zu den GUIDs, die Medien Untertypen darstellen, finden Sie [unter Video Untertyp-GUIDs](video-subtype-guids.md).

Dieser DSP kann sowohl das Zuschneiden als auch das Skalieren des Video Bilds durchführen. Das Format des Ausgabe Typs muss mit dem Format des Eingabetyps identisch sein. Der DSP führt keine Farb Raum Konvertierungen aus.

Bevor Sie den Ausgabetyp festlegen können, können Sie mithilfe der in dieser Tabelle aufgeführten Eigenschaften eine beliebige der folgenden Regionen definieren.



| Region                   | Eigenschaften                                                                                                                                                       |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Quell Rechteck         | mfpkey- \_ Größenänderung für \_ src \_ left<br/> mfpkey- \_ Größenänderung, \_ \_ oben<br/> mfpkey- \_ Größe für \_ src- \_ Breite<br/> mfpkey- \_ Größenänderung für \_ src- \_ Höhe<br/>            |
| Ziel Rechteck    | mfpkey- \_ Größe nach \_ \_ Links ändern<br/> mfpkey \_ Größenänderung nach \_ \_ oben<br/> mfpkey- \_ \_ DST- \_ Breite ändern<br/> mfpkey- \_ \_ DST- \_ Höhe ändern<br/>            |
| Geometrische Öffnung       | mfpkey \_ Ändern von \_ geomapx<br/> mfpkey \_ Ändern der \_ geomapy<br/> mfpkey \_ Ändern von \_ geomapwidth<br/> mfpkey- \_ Größe für \_ geomapheight ändern<br/>             |
| Minimale Anzeige Öffnung | mfpkey- \_ Größe ändern \_ minapx<br/> mfpkey- \_ Größe ändern \_<br/> mfpkey- \_ Größe ändern \_ minapwidth<br/> mfpkey-Wert für \_ \_ minapheight ändern<br/>                 |
| Bereich schwenken/Scannen          | mfpkey- \_ Größe ändern von \_ panscanapx<br/> mfpkey \_ Resize \_ panscanapy<br/> mfpkey- \_ Größe ändern von \_ panscanapwidth<br/> mfpkey- \_ Größe ändern von \_ panscanapheight<br/> |



 

In jedem Fall müssen Sie alle zugeordneten Eigenschaften festlegen, damit die Einstellung wirksam wird.

Der DSP kopiert den Teil des Quell Bilds, der durch das Quell Rechteck definiert ist, und streckt oder komprimiert ihn auf das Ziel Rechteck im Ausgabepuffer. Die Quell-und Ziel Rechtecke müssen nicht die gleiche Größe aufweisen. Die Frame Größe im Ausgabe Medientyp muss groß genug sein, um das Ziel Rechteck aufnehmen zu können.

Die geometrische Öffnung, die minimale Anzeige Öffnung und der Pan/Scan-Bereich haben keine Auswirkung darauf, wie die Größe des Videos von DSP geändert wird. Sie können sich jedoch darauf auswirken, wie die Downstreamkomponente den Videoframe interpretiert. Insbesondere verwendet der Enhanced Video Renderer (EVR) diese Werte, wenn er das Bildseiten Verhältnis und den Anzeigebereich berechnet.

Wenn Sie Media Foundation Medientypen verwenden, können Sie die geometrische Öffnung, die minimale Anzeige Öffnung und die Pan/Scan-Bereiche direkt im Ausgabe Medientyp festlegen. Wenn Sie DMO-Medientypen verwenden, legen Sie diese mithilfe der Eigenschaften fest.

Weitere Informationen finden Sie unter den folgenden Themen:

-   [**\_geometrische Monte-MT- \_ \_ Öffnung**](mf-mt-geometric-aperture-attribute.md)
-   [**minimale Anzahl von MF- \_ MT- \_ \_ anzeigen \_**](mf-mt-minimum-display-aperture-attribute.md)
-   [**MF- \_ MT- \_ Schwenken- \_ Überprüfung \_**](mf-mt-pan-scan-aperture-attribute.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vidreszr.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Digitale Signal Prozessoren](windowsmediadigitalsignalprocessors.md)
</dt> </dl>

 

 
