---
description: Verwenden von komprimierten Texturen (Direct3D 9)
ms.assetid: 60892a8b-93f4-43ba-87ef-d5c7cc6fb8c6
title: Verwenden von komprimierten Texturen (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 643b0618043f12ff3e1a84b806c86edb780ad929
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747601"
---
# <a name="using-compressed-textures-direct3d-9"></a>Verwenden von komprimierten Texturen (Direct3D 9)

## <a name="determining-support-for-compressed-textures"></a>Festlegen der Unterstützung für komprimierte Texturen

Wenn Sie den Adapter testen möchten, geben Sie ein beliebiges Pixel Format an, das DXT1, DXT2, DXT3, DXT4 oder DXT5 verwendet. Wenn [**IDirect3D9:: CheckDeviceFormat**](/windows/desktop/api) D3D OK zurückgibt \_ , kann das Gerät Textur direkt aus einer komprimierten Textur Oberfläche erstellen, die das Format verwendet. Wenn dies der Fall ist, können Sie komprimierte Textur Oberflächen direkt mit Direct3D verwenden, indem Sie die [**IDirect3DDevice9:: SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) -Methode aufrufen. Im folgenden Codebeispiel wird veranschaulicht, wie bestimmt wird, ob der Adapter ein komprimiertes Textur Format unterstützt.


```
BOOL IsCompressedTextureFormatOk( D3DFORMAT TextureFormat, 
                                  D3DFORMAT AdapterFormat ) 
{
    HRESULT hr = pD3D->CheckDeviceFormat( D3DADAPTER_DEFAULT,
                                          D3DDEVTYPE_HAL,
                                          AdapterFormat,
                                          0,
                                          D3DRTYPE_TEXTURE,
                                          TextureFormat);

    return SUCCEEDED( hr );
}
```



Wenn das Gerät Texturierung von komprimierten Textur Oberflächen nicht unterstützt, können Sie Textur Daten trotzdem in einer komprimierten Formatierungs Oberfläche speichern, aber Sie müssen alle komprimierten Texturen in ein unterstütztes Format konvertieren, bevor Sie für die Texturierung verwendet werden können.

## <a name="creating-compressed-textures"></a>Erstellen komprimierter Texturen

Nachdem Sie ein Gerät erstellt haben, das ein komprimiertes Textur Format auf dem Adapter unterstützt, können Sie eine komprimierte Textur Ressource erstellen. Aufrufen von [**IDirect3DDevice9:: kreatetexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) und Angeben eines komprimierten Textur Formats für den Format-Parameter.

Bevor Sie ein Bild in ein Textur Objekt laden, rufen Sie einen Zeiger auf die Textur Oberfläche ab, indem Sie die [**IDirect3DTexture9:: GetSurfaceLevel**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-getsurfacelevel) -Methode aufrufen.

Nun können Sie eine beliebige D3DXLoadSurfacexxx-Funktion verwenden, um ein Bild auf die-Oberfläche zu laden, die mit [**IDirect3DTexture9:: GetSurfaceLevel**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-getsurfacelevel)abgerufen wurde. Diese Funktionen behandeln die Konvertierung in und aus komprimierten Textur Formaten.

Sie können komprimierte Textur Dateien (DDS) mit dem DirectX-Textur-Editor (Dxtex.exe) erstellen und konvertieren, der mit dem DirectX SDK bereitgestellt wird. Sie erhalten Dxtex.exe und erfahren mehr über das DirectX SDK. Weitere Informationen zum DirectX SDK finden Sie unter [wo ist das DirectX SDK?](../directx-sdk--august-2009-.md).

Der Vorteil dieses Verhaltens besteht darin, dass eine Anwendung den Inhalt einer komprimierten Oberfläche in eine Datei kopieren kann, ohne zu berechnen, wie viel Speicher für eine Oberfläche einer bestimmten Breite und Höhe im jeweiligen Format erforderlich ist.

In der folgenden Tabelle sind die fünf Typen komprimierter Texturen aufgeführt. Weitere Informationen zum Speichern der Daten finden Sie unter [komprimierte Textur Formate (Direct3D 9)](compressed-texture-formats.md). Diese Informationen sind nur erforderlich, wenn Sie eigene Komprimierungs Routinen schreiben.



| FOURCC | BESCHREIBUNG        | Alpha in der Vorschau? |
|--------|--------------------|----------------------|
| DXT1   | Undurchsichtiges/1-Bit-Alpha | –                  |
| DXT2   | Explizites Alpha     | Ja                  |
| DXT3   | Explizites Alpha     | Nein                   |
| DXT4   | Interpoliert Alpha | Ja                  |
| DXT5   | Interpoliert Alpha | Nein                   |



 

Wenn Sie Daten aus einem nicht vorab multiplizierten Format in ein vorab multipliziertes Format übertragen, skaliert Direct3D die Farben auf der Grundlage der Alpha Werte. Das Übertragen von Daten aus einem prämultiplizierten Format in ein nicht vorab multipliziertes Format wird nicht unterstützt. Wenn Sie versuchen, Daten aus einer vorab multiplizierten Alpha Quelle in ein nicht prämultipliziertes Alpha Ziel zu übertragen, gibt die Methode D3DERR \_ invalidcallzurück. Wenn Sie Daten aus einer vormultiplizierten Alpha Quelle an ein Ziel mit keinem Alpha übertragen, werden die Quell Farbkomponenten, die durch Alpha skaliert wurden, unverändert kopiert.

## <a name="decompressing-compressed-texture-surfaces"></a>Komprimieren komprimierter Textur Oberflächen

Wie beim Komprimieren einer Textur Oberfläche wird die Komprimierung einer komprimierten Textur über Direct3D-Kopierdienste durchgeführt.

Um eine komprimierte Textur Oberfläche in eine nicht komprimierte Textur Oberfläche zu kopieren, verwenden Sie die [**D3DXLoadSurfaceFromSurface**](d3dxloadsurfacefromsurface.md)-Funktion. Diese Funktionen verarbeiten die Komprimierung zu und von komprimierten und unkomprimierten Oberflächen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Komprimierte Textur Ressourcen](compressed-texture-resources.md)
</dt> </dl>

 

 
