---
description: Konvertiert einen Videostream zwischen Farbformaten.
ms.assetid: 1c15dc2b-0e69-4d16-af02-8056a1eb2c5c
title: Farb Konverter DSP (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73a8418d6eeeffcf83a38452b19f18a6baa60bcc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484107"
---
# <a name="color-converter-dsp"></a>Farb Konverter-DSP

Konvertiert einen Videostream zwischen Farbformaten.

## <a name="clsid"></a>CLSID

CLSID \_ ccolorconvertdmo

## <a name="interfaces"></a>Schnittstellen

-   [**Imediaobject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject)
-   [**Imfrealtimeclient**](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient)
-   [**IMF-Transformation**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
-   [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)
-   [Iwmcolor-Eigenschaften](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcolorconvprops)

## <a name="input-formats"></a>Eingabeformate

-   RGB 24
-   RGB 32
-   RGB 555
-   RGB 565
-   RGB 8
-   Ayuv
-   I420
-   IYUV
-   NV11
-   NV12
-   UYVY
-   V216
-   V410
-   Im y41p
-   Y41T
-   Y42T
-   Im YUY2
-   YV12
-   YVU9
-   Im yvyu

## <a name="output-formats"></a>Ausgabeformate

-   RGB 24
-   RGB 32
-   RGB 555
-   RGB 565
-   RGB 8
-   Ayuv
-   I420
-   IYUV
-   NV11
-   NV12
-   UYVY
-   V216
-   V410
-   Im YUY2
-   YV12
-   Im yvyu

## <a name="properties"></a>Eigenschaften

-   [mfpkey \_ Color-v \_ srcleft](mfpkey-colorconv-srcleft.md)
-   [mfpkey \_ Color-v \_ srctop](mfpkey-colorconv-srctop.md)
-   [mfpkey \_ Color-v \_ dstleft](mfpkey-colorconv-dstleft.md)
-   [mfpkey \_ Color-v \_ dsttop](mfpkey-colorconv-dsttop.md)
-   [Breite von mfpkey \_ Color-v \_](mfpkey-colorconv-width.md)
-   [mfpkey \_ Color-v- \_ Höhe](mfpkey-colorconv-height.md)
-   [mfpkey \_ Color-v- \_ Modus](mfpkey-colorconv-mode.md)

## <a name="remarks"></a>Bemerkungen

Der Farb Konverter DSP ist als COM-Objekt implementiert, das als directxmedia-Objekt (DMO) oder Media Foundation Transformation (MFT) fungieren kann. Das-Objekt verfügt über einen einzelnen Klassen Bezeichner (CLSID), unabhängig davon, ob er als DMO oder MFT fungiert. Informationen dazu, wann ein DSP als DMO oder MFT fungiert, finden Sie unter [digitale Signal Prozessoren](windowsmediadigitalsignalprocessors.md).

Die global eindeutigen Bezeichner (GUIDs) für RGB-Medien Untertypen unterscheiden sich abhängig davon, ob ein DSP als DMO oder MFT fungiert. Die GUIDs für nicht-RGB-Medien Untertypen sind identisch, unabhängig davon, ob ein DSP als DMO oder MFT fungiert. Informationen zu den GUIDs, die Medien Untertypen darstellen, finden Sie [unter Video Untertyp-GUIDs](video-subtype-guids.md).

Standardmäßig kopiert dieser DSP das gesamte Quell Abbild in den Ausgabepuffer. Optional können Sie Quell-und Ziel Rechtecke angeben. Der DSP kopiert den Teil des Quell Bilds, der durch das Quell Rechteck definiert ist, und schreibt ihn in das Ziel Rechteck im Ausgabepuffer. Der DSP führt keine Skalierung aus. die Quell-und Ziel Rechtecke müssen dieselbe Größe aufweisen. Die Quell-und Ziel Rechtecke dürfen die Grenzen des Video Rahmens nicht überschreiten.

Alle Eigenschaften außer dem [**mfpkey \_ Color-v- \_ Modus**](mfpkey-colorconv-mode.md) müssen in einer Gruppe festgelegt werden. Wenn Sie eine dieser Eigenschaften festlegen, müssen Sie alle anderen festlegen. Andernfalls sind die Quell-und Ziel Rechtecke möglicherweise ungültig. in diesem Fall geben sowohl die [**imftransform::P rocess Output**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) -Methode als auch die [**imediaobject::P rocess Output**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processoutput) -Methode **E \_ invalidArg** zurück.

Der Farb Konverter unterstützt nicht jede Kombination aus Eingabeformat und Ausgabeformat. Normalerweise sollten Sie das Medienformat festlegen, das Sie wissen, entweder Eingabe oder Ausgabe, und dann die verfügbaren Formate im umgekehrten Stream auflisten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Colorcnv.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Digitale Signal Prozessoren](windowsmediadigitalsignalprocessors.md)
</dt> </dl>

 

 
