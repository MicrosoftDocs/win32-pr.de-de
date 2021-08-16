---
title: Bitmap-Quelleffekt
description: Verwenden Sie den Bitmap-Quelleffekt, um ein ID2D1Image aus einer IWICBitmapSource zur Verwendung als Eingabe in einem Effektdiagramm zu generieren.
ms.assetid: 86646111-208A-4E6D-A28C-7B23A1742D24
keywords:
- Bitmap-Quelleffekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19889372c7ebd4268f1b6fd8b77c360f290cc416631e9fb5e1cd3a0b0320844c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119833321"
---
# <a name="bitmap-source-effect"></a>Bitmap-Quelleffekt

Verwenden Sie den Bitmap-Quelleffekt, um ein [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) aus einer [**IWICBitmapSource**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource) zur Verwendung als Eingabe in einem Effektdiagramm zu generieren. Dieser Effekt führt skalierungs- und rotationsskalierend auf der CPU aus. Sie kann optional auch eine Systemspeicher-Mipmap generieren, die eine Leistungsoptimierung für die aktive Skalierung sehr großer Bilder mit verschiedenen reduzierten Auflösungen sein kann.

> [!Note]  
> Der Bitmapquelleneffekt nimmt seine Eingabe als Eigenschaft und nicht als Bildeingabe an. Sie müssen die [**SetValue-Methode**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)) verwenden, nicht die [**SetInput-Methode.**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1effect-setinput) In *der WicBitmapSource-Eigenschaft* geben Sie die Bildeingabedaten an.

 

Die CLSID für diesen Effekt ist CLSID \_ D2D1BitmapSource.

-   [Effect-Eigenschaften](#effect-properties)
-   [Interpolationsmodi](#interpolation-modes)
-   [Orientation](#orientation)
-   [Alphamodi](#alpha-modes)
-   [Anmerkungen](#remarks)
-   [Requirements](#requirements)
-   [Zugehörige Themen](#related-topics)

## <a name="effect-properties"></a>Effect-Eigenschaften



| Anzeigename und Indexenumeration                                                          | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WicBitmapSource<br/> D2D1 \_ BITMAPSOURCE \_ PROP \_ WIC \_ BITMAP \_ SOURCE<br/>         | Die [IWICBitmapSource,](/windows/desktop/wic/-wic-imp-iwicbitmapsource) die die zu ladenden Bilddaten enthält.<br/> Der Typ ist [IWICBitmapSource.](/windows/desktop/wic/-wic-imp-iwicbitmapsource)<br/> Der Standardwert ist NULL.<br/>                                                                                                                                                                                                                   |
| Skalieren<br/> D2D1 \_ BITMAPSOURCE \_ PROP \_ SCALE<br/>                                 | Die Skalierungsmenge in X- und Y-Richtung. Der Effekt multipliziert die Breite mit dem X-Wert und die Höhe mit dem Y-Wert. Diese Eigenschaft ist ein D2D1 \_ VECTOR \_ 2F, der wie folgt definiert ist: (X-Skalierung, Y-Skalierung). Die Skalierungsbeträge sind FLOAT, einheitenlos und müssen positiv oder 0 sein.<br/> Der Typ ist D2D1 \_ VECTOR \_ 2F.<br/> Der Standardwert ist {1.0f, 1.0f}.<br/>                                                                           |
| Interpolationmode.<br/> D2D1 \_ BITMAPSOURCE \_ PROP \_ INTERPOLATION \_ MODE<br/>      | Der Interpolationsmodus, der zum Skalieren des Bilds verwendet wird. Weitere Informationen finden Sie [unter Interpolationsmodi.](#interpolation-modes)<br/> Wenn der Modus die Mipmap deaktiviert, speichert BitmapSouce das Bild mit der Auflösung zwischen, die durch die Eigenschaften Scale und EnableDPICorrection bestimmt wird.<br/> Der Typ ist D2D1 \_ BITMAPSOURCE \_ INTERPOLATION \_ MODE.<br/> Der Standardwert ist D2D1 \_ BITMAPSOURCE \_ INTERPOLATION \_ MODE \_ LINEAR.<br/> |
| EnableDPICorrection<br/> D2D1 \_ BITMAPSOURCE \_ PROP \_ ENABLE \_ DPI \_ CORRECTION<br/> | Wenn Sie diese Einstellung auf TRUE festlegen, skaliert der Effekt das Eingabebild, um den von [**IWICBitmapSource**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource) gemeldeten DPI in den DPI des Gerätekontexts zu konvertieren. Der Effekt verwendet den Interpolationsmodus, den Sie mit der InterpolationMode-Eigenschaft festgelegt haben. Wenn Sie diese Einstellung auf FALSE festlegen, verwendet der Effekt einen DPI-Wert von 96.0 für das Ausgabebild.<br/> Der Typ ist BOOL.<br/> Der Standardwert ist FALSE.<br/>   |
| AlphaMode<br/> D2D1 \_ BITMAPSOURCE \_ PROP \_ ALPHA \_ MODE<br/>                       | Der Alphamodus der Ausgabe. Dies kann entweder prämultiplizierend oder direkt sein. Weitere Informationen finden Sie [unter Alphamodi.](#alpha-modes)<br/> Der Typ ist D2D1 \_ BITMAPSOURCE \_ ALPHA \_ MODE.<br/> Der Standardwert ist D2D1 \_ BITMAPSOURCE \_ ALPHA MODE \_ \_ PREMULTIPLIED.<br/>                                                                                                                                                              |
| Orientation<br/> D2D1 \_ BITMAPSOURCE \_ PROP \_ ORIENTATION<br/>                     | Ein Flip- und/oder Drehungsvorgang, der für das Bild ausgeführt werden soll. Weitere Informationen finden Sie unter [Ausrichtung.](#orientation)<br/> Der Typ ist D2D1 \_ BITMAPSOURCE \_ ORIENTATION.<br/> Der Standardwert ist D2D1 \_ BITMAPSOURCE \_ ORIENTATION \_ DEFAULT.<br/>                                                                                                                                                                                 |



 

## <a name="interpolation-modes"></a>Interpolationsmodi

Der Effekt interpoliert mit diesem Modus, wenn er ein Bild skaliert oder den DPI korrigiert. Die von diesem Effekt verwendeten Interpolationsmodi werden von der CPU und nicht von der GPU berechnet.



| Name                                                       | BESCHREIBUNG                                                                                                                                                                                                                          |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ BITMAPSOURCE \_ INTERPOLATION \_ MODE \_ NEAREST \_ NEIGHBOR | Probieren Sie den nächstgelegenen einzelnen Punkt aus, und verwendet diesen. Generiert keine Mipmap.                                                                                                                                                           |
| D2D1 \_ BITMAPSOURCE \_ INTERPOLATION \_ MODE \_ LINEAR            | Verwendet eine Vier-Punkt-Stichprobe und lineare Interpolation. Generiert keine Mipmap.                                                                                                                                                        |
| D2D1 \_ BITMAPSOURCE \_ INTERPOLATION \_ MODE \_ KUBISCH             | Verwendet einen kubischen Kernel mit 16 Beispielen für die Interpolation. Generiert keine Mipmap.                                                                                                                                                          |
| D2D1 \_ BITMAPSOURCE \_ INTERPOLATION \_ MODE \_ MINIMIERUNG              | Verwendet die WIC-Interpolation, die mit der [**IWICBitmapScaler-Schnittstelle**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapscaler) identisch ist. Generiert keine Mipmap.                                                                                       |
| D2D1 \_ BITMAPSOURCE \_ INTERPOLATION \_ MODE \_ MIPMAP \_ LINEAR    | Generiert eine Mipmapkette im Systemspeicher mit bilinearer Interpolation. Für jede Mipmap skaliert der Effekt mithilfe der bilinearen Interpolation auf das nächste Vielfache von 0,5 und skaliert dann die verbleibende Menge mit linearer Interpolation. |



 

## <a name="orientation"></a>Orientation

Die Orientation-Eigenschaft kann verwendet werden, um ein EXIF-Ausrichtungsflag anzuwenden, das in ein Bild eingebettet ist.



| Name                                                                    | BESCHREIBUNG                                                        |
|-------------------------------------------------------------------------|--------------------------------------------------------------------|
| D2D1 \_ BITMAPSOURCE \_ ORIENTATION \_ DEFAULT                                | Standard. Der Effekt ändert nicht die Ausrichtung der Eingabe.   |
| D2D1 \_ BITMAPSOURCE \_ ORIENTATION \_ FLIP \_ HORIZONTAL                       | Das Bild wird horizontal gekippt.                                      |
| D2D1 \_ BITMAPSOURCE \_ ORIENTATION \_ ROTATE \_ CLOCKWISE180                   | Rotiert das Bild im Uhrzeigersinn um 180 Grad.                           |
| D2D1 \_ BITMAPSOURCE \_ ORIENTATION \_ ROTATE \_ CLOCKWISE180 \_ FLIP \_ HORIZONTAL | Rotiert das Bild im Uhrzeigersinn um 180 Grad und flippt es horizontal. |
| D2D1 \_ BITMAPSOURCE \_ ORIENTATION \_ ROTATE \_ CLOCKWISE270 \_ FLIP \_ HORIZONTAL | Rotiert das Bild im Uhrzeigersinn um 270 Grad und flippt es horizontal. |
| D2D1 \_ BITMAPSOURCE \_ ORIENTATION \_ ROTATE \_ CLOCKWISE90                    | Rotiert das Bild im Uhrzeigersinn um 90 Grad.                            |
| D2D1 \_ BITMAPSOURCE \_ ORIENTATION \_ ROTATE \_ CLOCKWISE90 \_ FLIP \_ HORIZONTAL  | Dreht das Bild im Uhrzeigersinn um 90 Grad und flippt es horizontal.  |
| D2D1 \_ BITMAPSOURCE \_ ORIENTATION \_ ROTATE \_ CLOCKWISE270                   | Rotiert das Bild im Uhrzeigersinn um 270 Grad.                           |



 

Dieser Codeausschnitt veranschaulicht die Konvertierung von EXIF-Ausrichtungswerten (definiert in propkey.h) in D2D1 \_ BITMAPSOURCE \_ ORIENTATION-Werte.


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



## <a name="alpha-modes"></a>Alphamodi



| Name                                           | BESCHREIBUNG                                            |
|------------------------------------------------|--------------------------------------------------------|
| D2D1 \_ BITMAPSOURCE \_ ALPHA \_ MODE \_ PREMULTIPLIED | Die Effektausgabe verwendet prämultipliiertes Alpha.<br/> |
| D2D1 \_ BITMAPSOURCE \_ ALPHA \_ MODE \_ STRAIGHT      | Die Effektausgabe verwendet gerades Alpha.<br/>      |



 

## <a name="remarks"></a>Hinweise

Um die Leistung bei der gemeinsamen Verwendung von WIC und [Direct2D](./direct2d-portal.md) zu optimieren, sollten Sie [**IWICFormatConverter**](/windows/desktop/api/wincodec/nn-wincodec-iwicformatconverter) verwenden, um basierend auf Ihrem App-Szenario und der nativen Genauigkeit des Bilds in ein geeignetes Pixelformat zu konvertieren.

In den meisten Fällen erfordert entweder die [Direct2D-Pipeline](./direct2d-portal.md) Ihrer App nur eine Genauigkeit von 8 Bits pro Kanal (bpc), oder das Bild bietet nur eine Genauigkeit von 8 BPC. Daher sollten Sie in die GUID \_ WICPixelFormat32bppPBGRA konvertieren. Wenn Sie jedoch die zusätzliche Genauigkeit nutzen möchten, die von einem Bild bereitgestellt wird (z. B. eine JPEG-XR oder TIFF, die mit einer Genauigkeit von mehr als 8 BPC gespeichert ist), sollten Sie ein RGBA-basiertes Pixelformat verwenden. Die folgende Tabelle enthält weitere Details.



| Gewünschte Genauigkeit   | Native Genauigkeit des Bilds | Empfohlenes Pixelformat                |
|---------------------|-------------------------------|-----------------------------------------|
| 8 Bits pro Kanal  | <= 8 Bits pro Kanal      | GUID \_ WICPixelFormat32bppPBGRA          |
| So hoch wie möglich | <= 8 Bits pro Kanal      | GUID \_ WICPixelFormat32bppPBGRA          |
| So hoch wie möglich | > 8 Bits pro Kanal       | RGBA-Kanalreihenfolge, prämultipliziertes Alpha |



 

Da viele Bildformate mehrere Genauigkeitsebenen unterstützen, sollten Sie [**IWICBitmapSource::GetPixelFormat**](/windows/desktop/wic/-wic-codec-iwicbitmapsource-getpixelformat-proxy) verwenden, um das systemeigene Pixelformat des Bilds abzurufen, und dann [**IWICPixelFormatInfo**](/windows/desktop/api/wincodec/nn-wincodec-iwicpixelformatinfo) verwenden, um zu bestimmen, wie viele Bits pro Genauigkeitskanal für dieses Format verfügbar sind. Beachten Sie auch, dass nicht alle Hardware Pixelformate mit hoher Genauigkeit unterstützt. In diesen Fällen muss Ihre App möglicherweise auf das WARP-Gerät zurückgreifen, um hohe Genauigkeit zu unterstützen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client) | Windows 8 und Plattformupdate für Windows 7 \[ Desktop-Apps \| Windows Store Apps\] |
| Unterstützte Mindestversion (Server) | Windows 8 und Plattformupdate für Windows 7 \[ Desktop-Apps \| Windows Store Apps\] |
| Header                   | d2d1effects.h                                                                      |
| Bibliothek                  | d2d1.lib, dxguid.lib                                                               |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

