---
title: Auswirkungen der Bitmapquelle
description: Verwenden Sie den Bitmap-Quell Effekt, um eine ID2D1Image aus einer IWICBitmapSource zu generieren, die als Eingabe in einem Effekt Diagramm verwendet werden soll.
ms.assetid: 86646111-208A-4E6D-A28C-7B23A1742D24
keywords:
- Auswirkungen der Bitmapquelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a439c94f0f520b318b3cb3511775dbec58b6e139
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859228"
---
# <a name="bitmap-source-effect"></a>Auswirkungen der Bitmapquelle

Verwenden Sie den Bitmap-Quell Effekt, um eine [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) aus einer [**IWICBitmapSource**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource) zu generieren, die als Eingabe in einem Effekt Diagramm verwendet werden soll. Dieser Effekt führt die Skalierung und Drehung auf der CPU durch. Außerdem kann optional eine MipMap für den System Arbeitsspeicher generiert werden. Dies kann eine Leistungsoptimierung für die aktive Skalierung sehr großer Abbilder mit unterschiedlichen reduzierten Auflösungen sein.

> [!Note]  
> Der Bitmap-Quell Effekt nimmt seine Eingabe als Eigenschaft und nicht als Bild Eingabe an. Sie müssen die [**SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)) -Methode und nicht die [**SetInput**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1effect-setinput) -Methode verwenden. In der *wicbitmapsource* -Eigenschaft geben Sie die Bild Eingabedaten an.

 

Die CLSID für diesen Effekt ist CLSID \_ D2D1BitmapSource.

-   [Effekt Eigenschaften](#effect-properties)
-   [Interpolations Modi](#interpolation-modes)
-   [Ausrichtung](#orientation)
-   [Alpha-Modi](#alpha-modes)
-   [Anmerkungen](#remarks)
-   [Anforderungen](#requirements)
-   [Zugehörige Themen](#related-topics)

## <a name="effect-properties"></a>Effekt Eigenschaften



| Anzeige Name und indexenumeration                                                          | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Wicbitmapsource<br/> D2D1 \_ BitmapSource- \_ Prop \_ WIC \_ Bitmap- \_ Quelle<br/>         | Das [IWICBitmapSource](/windows/desktop/wic/-wic-imp-iwicbitmapsource) -Element, das die zu ladenden Bilddaten enthält.<br/> Der Typ ist " [IWICBitmapSource](/windows/desktop/wic/-wic-imp-iwicbitmapsource)".<br/> Der Standardwert ist NULL.<br/>                                                                                                                                                                                                                   |
| Skalieren<br/> D2D1 \_ BitmapSource- \_ Prop- \_ Skala<br/>                                 | Der Skalierungs Betrag in der X-und Y-Richtung. Der Effekt multipliziert die Breite mit dem X-Wert und der Höhe um den Y-Wert. Diese Eigenschaft ist ein D2D1 \_ Vector \_ 2F, definiert als: (X Skala, Y-Skala). Die Skalierungs Beträge sind float, unitless und müssen positiv oder 0 sein.<br/> Der Typ ist "D2D1 \_ Vector \_ 2F".<br/> Der Standardwert ist {1.0 f, 1.0 f}.<br/>                                                                           |
| InterpolationMode.<br/> D2D1 \_ BitmapSource- \_ Prop- \_ Interpolations \_ Modus<br/>      | Der Interpolations Modus, der zum Skalieren des Bilds verwendet wird. Weitere Informationen finden Sie unter [Interpolations Modi](#interpolation-modes) .<br/> Wenn der Modus die MipMap deaktiviert, speichert bitmapsouce das Bild mit der Auflösung, die durch die Eigenschaften Scale und enabledpicorrection festgelegt wird.<br/> Der Typ ist der D2D1 \_ BitmapSource- \_ Interpolations \_ Modus.<br/> Der Standardwert ist der D2D1 \_ BitmapSource- \_ Interpolations \_ Modus \_ linear.<br/> |
| Enabledpicorrection<br/> D2D1 \_ BitmapSource- \_ Prop \_ Aktivieren der dpi- \_ \_ Korrektur<br/> | Wenn Sie diese Einstellung auf "true" festlegen, wird das Eingabebild durch die Auswirkung skaliert, um den von [**IWICBitmapSource**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource) gemeldeten dpi-Wert in den dpi-Wert des Geräte Kontexts zu konvertieren. Der Effekt verwendet den Interpolations Modus, den Sie mit der InterpolationMode-Eigenschaft festlegen. Wenn Sie diese Einstellung auf "false" festlegen, verwendet der Effekt einen dpi-Wert von 96,0 für das Ausgabe Image.<br/> Der Typ ist "bool".<br/> Der Standardwert ist FALSE.<br/>   |
| Alpha AMODE<br/> D2D1 \_ BitmapSource- \_ Prop- \_ alpha- \_ Modus<br/>                       | Der Alpha-Modus der Ausgabe. Dies kann entweder vorab multipliziert oder direkt erfolgen. Weitere Informationen finden Sie unter [Alpha-Modi](#alpha-modes) .<br/> Der Typ ist der D2D1 \_ BitmapSource- \_ alpha- \_ Modus.<br/> Der Standardwert ist "D2D1 \_ BitmapSource \_ Alpha Mode" ( \_ \_ vorab multipliziert).<br/>                                                                                                                                                              |
| Orientation<br/> D2D1 \_ BitmapSource \_ - \_ Ausrichtung<br/>                     | Ein Flip-und/oder Drehung-Vorgang, der für das Bild ausgeführt werden soll. Weitere Informationen finden Sie unter [Ausrichtung](#orientation) .<br/> Der Typ ist D2D1 \_ BitmapSource- \_ Ausrichtung.<br/> Der Standardwert ist D2D1 \_ BitmapSource \_ Orientation \_ default.<br/>                                                                                                                                                                                 |



 

## <a name="interpolation-modes"></a>Interpolations Modi

Der Effekt interpoliert die Verwendung dieses Modus, wenn ein Bild skaliert wird oder der dpi-Wert korrigiert wird. Die von dieser Auswirkung verwendeten Interpolations Modi werden von der CPU berechnet, nicht von der GPU.



| Name                                                       | BESCHREIBUNG                                                                                                                                                                                                                          |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ BitmapSource- \_ Interpolations \_ Modus \_ Nächster \_ Nachbar | Verwendet den nächsten einzelnen Punkt und verwendet diesen. Generiert keine MipMap.                                                                                                                                                           |
| D2D1 \_ BitmapSource- \_ Interpolations \_ Modus \_ linear            | Verwendet ein vier-Punkt-Beispiel und eine lineare interpolung. Generiert keine MipMap.                                                                                                                                                        |
| D2D1 \_ BitmapSource- \_ Interpolations \_ Modus ( \_ kubisch)             | Verwendet einen 16-beispielkubischen Kernel für Interpolationen. Generiert keine MipMap.                                                                                                                                                          |
| D2D1 \_ BitmapSource- \_ Interpolations \_ Modus \_              | Verwendet die WIC-"Fant Interpolations", die mit der [**IWICBitmapScaler**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapscaler) -Schnittstelle identisch ist. Generiert keine MipMap.                                                                                       |
| D2D1 \_ BitmapSource \_ Interpolations \_ Modus \_ MipMap \_ linear    | Generiert eine MipMap-Kette im Systemspeicher mithilfe der bilinearen interpolung. Für jede MipMap wird die Auswirkung auf das nächstgelegene Vielfache von 0,5 mithilfe der bilinearen interpolung skaliert, und anschließend wird der verbleibende Betrag mithilfe der linearen interpolung skaliert. |



 

## <a name="orientation"></a>Orientation

Die Orientation-Eigenschaft kann verwendet werden, um ein EXIF-ausrichtungsflag anzuwenden, das in ein Bild eingebettet ist.



| Name                                                                    | BESCHREIBUNG                                                        |
|-------------------------------------------------------------------------|--------------------------------------------------------------------|
| D2D1 \_ BitmapSource- \_ Ausrichtung ( \_ Standard)                                | Standard. Der Effekt ändert nicht die Ausrichtung der Eingabe.   |
| D2D1 \_ BitmapSource \_ - \_ Ausrichtung \_ Horizontal kippen                       | Flippt das Bild horizontal.                                      |
| D2D1 \_ BitmapSource- \_ Ausrichtung \_ drehen \_ CLOCKWISE180                   | Dreht das Bild um 180 Grad im Uhrzeigersinn.                           |
| D2D1 \_ BitmapSource \_ - \_ Ausrichtung \_ drehen \_ CLOCKWISE180 \_ Horizontal kippen | Dreht das Bild im Uhrzeigersinn um 180 Grad im Uhrzeigersinn und dreht es horizontal. |
| D2D1 \_ BitmapSource \_ - \_ Ausrichtung \_ drehen \_ CLOCKWISE270 \_ Horizontal kippen | Dreht das Bild im Uhrzeigersinn um 270 Grad im Uhrzeigersinn und dreht es horizontal. |
| D2D1 \_ BitmapSource- \_ Ausrichtung \_ drehen \_ CLOCKWISE90                    | Dreht das Bild um 90 Grad im Uhrzeigersinn.                            |
| D2D1 \_ BitmapSource \_ - \_ Ausrichtung \_ drehen \_ CLOCKWISE90 \_ Horizontal kippen  | Dreht das Bild im Uhrzeigersinn um 90 Grad im Uhrzeigersinn und dreht es horizontal.  |
| D2D1 \_ BitmapSource- \_ Ausrichtung \_ drehen \_ CLOCKWISE270                   | Dreht das Bild um 270 Grad im Uhrzeigersinn.                           |



 

Dieser Code Ausschnitt veranschaulicht, wie Sie aus den in "propkey. h" definierten EXIF-Ausrichtungs Werten in D2D1 \_ BitmapSource- \_ Orientierungswerte konvertieren.


```C++
#include <propkey.h>
#include <d2d1effects.h>

D2D1_BITMAPSOURCE_ORIENTATION GetBitmapSourceOrientation(unsigned short PhotoOrientation)
{
       switch (PhotoOrientation)
       {
       case PHOTO_ORIENTATION_NORMAL:
              return D2D1_BITMAPSOURCE_ORIENTATION_DEFAULT;
       case PHOTO_ORIENTATION_FLIPHORIZONTAL:
              return D2D1_BITMAPSOURCE_ORIENTATION_FLIP_HORIZONTAL;
       case PHOTO_ORIENTATION_ROTATE180:
              return D2D1_BITMAPSOURCE_ORIENTATION_ROTATE_CLOCKWISE180;
       case PHOTO_ORIENTATION_FLIPVERTICAL:
              return D2D1_BITMAPSOURCE_ORIENTATION_ROTATE_CLOCKWISE180_FLIP_HORIZONTAL;
       case PHOTO_ORIENTATION_TRANSPOSE: 
              return D2D1_BITMAPSOURCE_ORIENTATION_ROTATE_CLOCKWISE90_FLIP_HORIZONTAL;
       case PHOTO_ORIENTATION_ROTATE270:
              return D2D1_BITMAPSOURCE_ORIENTATION_ROTATE_CLOCKWISE90;
       case PHOTO_ORIENTATION_TRANSVERSE:
              return D2D1_BITMAPSOURCE_ORIENTATION_ROTATE_CLOCKWISE270_FLIP_HORIZONTAL;
       case PHOTO_ORIENTATION_ROTATE90:
              return D2D1_BITMAPSOURCE_ORIENTATION_ROTATE_CLOCKWISE270;
       default:
              return D2D1_BITMAPSOURCE_ORIENTATION_DEFAULT;
       }
}
```



## <a name="alpha-modes"></a>Alpha-Modi



| Name                                           | BESCHREIBUNG                                            |
|------------------------------------------------|--------------------------------------------------------|
| Der D2D1 \_ BitmapSource- \_ alpha \_ Modus ist \_ vormultipliziert. | Die Effekt Ausgabe verwendet ein prämultipliziertes alpha.<br/> |
| D2D1 \_ BitmapSource \_ alpha \_ Modus \_ direkt      | Die Effekt Ausgabe verwendet gerade alpha.<br/>      |



 

## <a name="remarks"></a>Bemerkungen

Um die Leistung bei der gemeinsamen Verwendung von WIC und [Direct2D](./direct2d-portal.md) zu optimieren, sollten Sie [**IWICFormatConverter**](/windows/desktop/api/wincodec/nn-wincodec-iwicformatconverter) verwenden, um in ein entsprechendes Pixel Format zu konvertieren, das in Ihrem App-Szenario und in der nativen Genauigkeit des Images basiert.

In den meisten Fällen ist für die [Direct2D](./direct2d-portal.md) -Pipeline ihrer app nur eine Genauigkeit von 8 Bits pro Kanal (BPC) erforderlich, oder das Image bietet nur 8 bpc-Genauigkeit. Daher sollten Sie in GUID \_ WICPixelFormat32bppPBGRA konvertieren. Wenn Sie jedoch die von einem Abbild bereitgestellte zusätzliche Genauigkeit nutzen möchten (z. b. ein JPEG-XR oder TIFF, das mit mehr als 8 bpc-Genauigkeit gespeichert ist), sollten Sie ein RGBA-basiertes Pixel Format verwenden. In der folgenden Tabelle finden Sie weitere Details.



| Gewünschte Genauigkeit   | Systemeigene Genauigkeit des Bilds | Empfohlenes Pixel Format                |
|---------------------|-------------------------------|-----------------------------------------|
| 8 Bits pro Kanal  | <= 8 Bits pro Kanal      | GUID \_ WICPixelFormat32bppPBGRA          |
| So hoch wie möglich | <= 8 Bits pro Kanal      | GUID \_ WICPixelFormat32bppPBGRA          |
| So hoch wie möglich | > 8 Bits pro Kanal       | RGBA-Kanal Reihenfolge, prämultipliziertes Alpha |



 

Da viele Bildformate mehrere Genauigkeits Stufen unterstützen, sollten Sie [**IWICBitmapSource:: GetPixelFormat**](/windows/desktop/wic/-wic-codec-iwicbitmapsource-getpixelformat-proxy) verwenden, um das systemeigene Pixel Format von Image abzurufen. verwenden Sie dann [**iwicpixelformatinfo**](/windows/desktop/api/wincodec/nn-wincodec-iwicpixelformatinfo) , um zu bestimmen, wie viele Bits pro Kanal Genauigkeit für dieses Format verfügbar sind. Beachten Sie auch, dass nicht alle Hardware Pixel Formate mit hoher Genauigkeit unterstützt. In diesen Fällen muss Ihre APP möglicherweise auf das Warp-Gerät zurückgreifen, um eine hohe Genauigkeit zu unterstützen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client) | Windows 8 und Platt Form Update für Windows 7 \[ -Desktop-Apps für \| Windows Store-Apps\] |
| Unterstützte Mindestversion (Server) | Windows 8 und Platt Form Update für Windows 7 \[ -Desktop-Apps für \| Windows Store-Apps\] |
| Header                   | d2d1effects. h                                                                      |
| Bibliothek                  | d2d1. lib, dxguid. lib                                                               |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

