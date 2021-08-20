---
description: Verwenden von komprimierten Texturen (Direct3D 9)
ms.assetid: 60892a8b-93f4-43ba-87ef-d5c7cc6fb8c6
title: Verwenden von komprimierten Texturen (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0f506cef8147ee5ef1fb0c99cf862254564240bb112e954884cc7a2a07d2d12
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119044018"
---
# <a name="using-compressed-textures-direct3d-9"></a>Verwenden von komprimierten Texturen (Direct3D 9)

## <a name="determining-support-for-compressed-textures"></a>Bestimmen der Unterstützung für komprimierte Texturen

Geben Sie zum Testen des Adapters ein beliebiges Pixelformat an, das DXT1, DXT2, DXT3, DXT4 oder DXT5 verwendet. Wenn [**IDirect3D9::CheckDeviceFormat**](/windows/desktop/api) D3D OK zurückgibt, kann das Gerät textur direkt aus einer komprimierten Texturoberfläche erstellen, die dieses \_ Format verwendet. Wenn ja, können Sie komprimierte Texturoberflächen direkt mit Direct3D verwenden, indem Sie die [**IDirect3DDevice9::SetTexture-Methode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) aufrufen. Im folgenden Codebeispiel wird veranschaulicht, wie Ermittelt wird, ob der Adapter ein komprimiertes Texturformat unterstützt.


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



Wenn das Gerät keine Textur von komprimierten Texturoberflächen unterstützt, können Sie Texturdaten weiterhin auf einer komprimierten Formatoberfläche speichern. Sie müssen jedoch alle komprimierten Texturen in ein unterstütztes Format konvertieren, bevor sie für die Texturierung verwendet werden können.

## <a name="creating-compressed-textures"></a>Erstellen komprimierter Texturen

Nachdem Sie ein Gerät erstellt haben, das ein komprimiertes Texturformat auf dem Adapter unterstützt, können Sie eine komprimierte Texturressource erstellen. Rufen [**Sie IDirect3DDevice9::CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) auf, und geben Sie ein komprimiertes Texturformat für den Format-Parameter an.

Rufen Sie vor dem Laden eines Bilds in ein Texturobjekt einen Zeiger auf die Texturoberfläche ab, indem Sie die [**IDirect3DTexture9::GetSurfaceLevel-Methode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-getsurfacelevel) aufrufen.

Jetzt können Sie eine beliebige D3DXLoadSurfacexxx-Funktion verwenden, um ein Bild auf die Oberfläche zu laden, die mithilfe von [**IDirect3DTexture9::GetSurfaceLevel abgerufen wurde.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-getsurfacelevel) Diese Funktionen verarbeiten die Konvertierung in und aus komprimierten Texturformaten.

Sie können komprimierte Texturdateien (Compressed Texture, DDS) mithilfe des DirectX Texture Editor (Dxtex.exe) erstellen und konvertieren, der mit dem DirectX SDK bereitgestellt wird. Sie können sich Dxtex.exe DirectX SDK darüber informieren. Informationen zum DirectX SDK finden Sie unter [Wo ist das DirectX SDK?](../directx-sdk--august-2009-.md).

Der Vorteil dieses Verhaltens ist, dass eine Anwendung den Inhalt einer komprimierten Oberfläche in eine Datei kopieren kann, ohne zu berechnen, wie viel Speicher für eine Oberfläche mit einer bestimmten Breite und Höhe im spezifischen Format erforderlich ist.

In der folgenden Tabelle sind die fünf Arten von komprimierten Texturen aufgeführt. Weitere Informationen zum Speichern der Daten finden Sie unter [Compressed Texture Formats (Direct3D 9) (Komprimierte Texturformate (Direct3D 9)).](compressed-texture-formats.md) Sie benötigen diese Informationen nur, wenn Sie Eigene Komprimierungsroutinen schreiben.



| FOURCC | Beschreibung        | Alpha-Prämultiplied? |
|--------|--------------------|----------------------|
| DXT1   | Nicht transparentes/1-Bit-Alpha | Nicht zutreffend                  |
| DXT2   | Explizites Alpha     | Ja                  |
| DXT3   | Explizites Alpha     | Nein                   |
| DXT4   | Interpoliertes Alpha | Ja                  |
| DXT5   | Interpoliertes Alpha | Nein                   |



 

Wenn Sie Daten aus einem nicht multipliierten Format in ein prämultipliiertes Format übertragen, skaliert Direct3D die Farben basierend auf den Alphawerten. Das Übertragen von Daten aus einem prämultipliierten Format in ein nicht vormultiplied-Format wird nicht unterstützt. Wenn Sie versuchen, Daten aus einer prämultipliierten Alphaquelle an ein nicht prämultipliiertes Alphaziel zu übertragen, gibt die Methode D3DERR \_ INVALIDCALL zurück. Wenn Sie Daten aus einer prämultipliierten Alphaquelle an ein Ziel ohne Alpha übertragen, werden die Quellfarbkomponenten, die mit Alpha skaliert wurden, wie befweislich kopiert.

## <a name="decompressing-compressed-texture-surfaces"></a>Dekomprimieren komprimierter Texturoberflächen

Wie beim Komprimieren einer Texturoberfläche erfolgt das Dekomprimieren einer komprimierten Textur über Direct3D-Kopierdienste.

Um eine komprimierte Texturoberfläche auf eine nicht komprimierte Texturoberfläche zu kopieren, verwenden Sie die [**Funktion D3DXLoadSurfaceFromSurface**](d3dxloadsurfacefromsurface.md). Diese Funktion verarbeitet die Komprimierung auf und von komprimierten und unkomprimierten Oberflächen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Komprimierte Texturressourcen](compressed-texture-resources.md)
</dt> </dl>

 

 
