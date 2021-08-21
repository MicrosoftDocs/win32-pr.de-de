---
description: Die ID3DXTextureGutterHelper-Schnittstelle wird zum Erstellen und Verwalten von Bundstegbereichen in einer Textur verwendet. Gutterbereiche trennen Texturen und ermöglichen eine bilineare Interpolation, um das Rendern von Artefakten an Texturgrenzen zu vermeiden.
ms.assetid: 097e27bf-a1a6-4e7e-bdad-33015b50f91f
title: ID3DXTextureGutterHelper-Schnittstelle (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e8e72814c036e297111a4a2f3825574a2a088310cb17d484902c59875958e7e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118093954"
---
# <a name="id3dxtexturegutterhelper-interface"></a>ID3DXTextureGutterHelper-Schnittstelle

Die ID3DXTextureGutterHelper-Schnittstelle wird zum Erstellen und Verwalten von Bundstegbereichen in einer Textur verwendet. Gutterbereiche trennen Texturen und ermöglichen eine bilineare Interpolation, um das Rendern von Artefakten an Texturgrenzen zu vermeiden.

The Get... -Methoden bieten Zugriff auf die Datenstrukturen, die von Apply... Methoden.

## <a name="members"></a>Member

Die **ID3DXTextureGutterHelper-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ID3DXTextureGutterHelper** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DXTextureGutterHelper-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                   | Beschreibung                                                                                            |
|:-------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------|
| [**ApplyGuttersFloat**](id3dxtexturegutterhelper--applyguttersfloat.md) | Wendet Gutter auf einen FLOAT-Texturpuffer an.<br/>                                                  |
| [**ApplyGuttersPRT**](id3dxtexturegutterhelper--applyguttersprt.md)     | Wendet Gutter auf ein [**ID3DXPRTBuffer-Pufferobjekt**](id3dxprtbuffer.md) an.<br/>               |
| [**ApplyGuttersTex**](id3dxtexturegutterhelper--applygutterstex.md)     | Wendet Gutter auf ein [**IDirect3DTexture9-Texturobjekt**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) an.<br/>        |
| [**GetBaryMap**](id3dxtexturegutterhelper--getbarymap.md)               | Ruft balyzentrische Texelkoordinaten ab.<br/>                                                    |
| [**GetFaceMap**](id3dxtexturegutterhelper--getfacemap.md)               | Ruft den Index des Netzgesichts ab, zu dem jedes Texel gehört.<br/>                           |
| [**GetGutterMap**](id3dxtexturegutterhelper--getguttermap.md)           | Empfängt einen Texelklassenwert, der die Texelklasse entsprechend dem Standort jedes Texels angibt.<br/> |
| [**Font.getheight**](id3dxtexturegutterhelper--getheight.md)                 | Ruft die Höhe der Textur in Pixel ab.<br/>                                             |
| [**GetTexelMap**](id3dxtexturegutterhelper--gettexelmap.md)             | Ruft die Texturkoordinaten (u, v) der einzelnen Texel ab.<br/>                                     |
| [**GetWidth**](id3dxtexturegutterhelper--getwidth.md)                   | Ruft die Breite der Textur in Pixel ab.<br/>                                              |
| [**ResampleTex**](id3dxtexturegutterhelper--resampletex.md)             | Resamples a texture into this gutterhelper es parametrisiert.<br/>                              |
| [**SetBaryMap**](id3dxtexturegutterhelper--setbarymap.md)               | Legt balyzentrische Texelkoordinaten fest.<br/>                                                         |
| [**SetFaceMap**](id3dxtexturegutterhelper--setfacemap.md)               | Legt den Index des Netzgesichts fest, zu dem jedes Texel gehört.<br/>                                |
| [**SetGutterMap**](id3dxtexturegutterhelper--setguttermap.md)           | Legt einen Texelklassenwert fest, der die Texelklasse entsprechend der Position jedes Texels angibt.<br/>     |
| [**SetTexelMap**](id3dxtexturegutterhelper--settexelmap.md)             | Legt die Texturkoordinaten (u, v) der einzelnen Texel fest.<br/>                                          |



 

## <a name="remarks"></a>Hinweise

> [!Note]  
> Bei Verwendung mit vorausberechnener Radianceübertragung (PRT) erfordert diese Schnittstelle eine eindeutige Parametrisierung des Modells. Jedes Texel muss einem einzelnen Punkt auf der Oberfläche des Modells entsprechen und umgekehrt. Wenn das Modell mehrere Texturen enthält, muss es in separate Teile aufgeteilt werden, die jeweils ein Bundsteghilfsobjekt pro Textur enthalten.

 

Diese Schnittstelle kann verwendet werden, um eine Karte im Texturraum zu generieren, in der sich jedes Texel in einer von vier Klassen befindet.



| Texel-Klasse | Texel-Standort                                                                                                                                                                                                                                                                                                                                                                |
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0           | Ungültiger Punkt; Texel wird nicht verwendet.                                                                                                                                                                                                                                                                                                                                        |
| 1           | Innerhalb des Dreiecks.                                                                                                                                                                                                                                                                                                                                                              |
| 2           | Innerhalb des Bundstegs.                                                                                                                                                                                                                                                                                                                                                                |
| 4           | Innerhalb des Bundstegs; texel wird als vollständiges Beispiel in den Methoden [**ID3DXTextureGutterHelper::ApplyGuttersFloat,**](id3dxtexturegutterhelper--applyguttersfloat.md) [**ID3DXTextureGutterHelper::ApplyGuttersTex**](id3dxtexturegutterhelper--applygutterstex.md)oder [**ID3DXTextureGutterHelper::ApplyGuttersPRT**](id3dxtexturegutterhelper--applyguttersprt.md) ausgewertet. |



 

Für die Klassen 1 und 2 wird ein Texel zusammen mit den balyzentrischen Koordinaten der ersten beiden Scheitelpunkte dieses Gesichts mit dem Gesicht gespeichert, zu dem es gehört. Guttervertices werden dem nächsten Rand im Texturraum zugewiesen.

Es gibt keine Texelklasse 3.

Die **ID3DXTextureGutterHelper-Schnittstelle** wird durch Aufrufen der [**D3DXCreateTextureGutterHelper-Funktion**](d3dxcreatetexturegutterhelper.md) abgerufen.

Der LPD3DXTEXTUREGUTTERHELPER-Typ wird als Zeiger auf die **ID3DXTextureGutterHelper-Schnittstelle** definiert.


```
typedef interface ID3DXTextureGutterHelper ID3DXTextureGutterHelper;
typedef interface ID3DXTextureGutterHelper *LPD3DXTEXTUREGUTTERHELPER;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Schnittstellen](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
