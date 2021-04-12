---
description: Die ID3DXTextureGutterHelper-Schnittstelle wird verwendet, um bundckbereiche in einer Textur zu erstellen und zu verwalten. Die Struktur der bundbereiche trennt die Texturen und ermöglicht bilineare Interpolationen, um das Rendern von Artefakten an Textur Grenzen zu vermeiden.
ms.assetid: 097e27bf-a1a6-4e7e-bdad-33015b50f91f
title: ID3DXTextureGutterHelper-Schnittstelle (D3DX9Mesh. h)
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
ms.openlocfilehash: ece03e14da490bd6d6f5aef69f9457939bc8bab7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355616"
---
# <a name="id3dxtexturegutterhelper-interface"></a>ID3DXTextureGutterHelper-Schnittstelle

Die ID3DXTextureGutterHelper-Schnittstelle wird verwendet, um bundckbereiche in einer Textur zu erstellen und zu verwalten. Die Struktur der bundbereiche trennt die Texturen und ermöglicht bilineare Interpolationen, um das Rendern von Artefakten an Textur Grenzen zu vermeiden.

Der Get... -Methoden ermöglichen den Zugriff auf die Datenstrukturen, die vom Apply... anzuwenden.

## <a name="members"></a>Member

Die **ID3DXTextureGutterHelper** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **ID3DXTextureGutterHelper** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DXTextureGutterHelper** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                   | BESCHREIBUNG                                                                                            |
|:-------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------|
| [**Applyguttersfloat**](id3dxtexturegutterhelper--applyguttersfloat.md) | Wendet die-Guster auf einen float-Textur Puffer an.<br/>                                                  |
| [**Applyguttersprt**](id3dxtexturegutterhelper--applyguttersprt.md)     | Wendet die-Guster auf ein [**ID3DXPRTBuffer**](id3dxprtbuffer.md) -Puffer Objekt an.<br/>               |
| [**Applygutterstex**](id3dxtexturegutterhelper--applygutterstex.md)     | Wendet die-Guster auf ein [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) -Textur Objekt an.<br/>        |
| [**Getbarymap**](id3dxtexturegutterhelper--getbarymap.md)               | Ruft texzentrische texzentrische Koordinaten ab.<br/>                                                    |
| [**Getfacemap**](id3dxtexturegutterhelper--getfacemap.md)               | Ruft den Index der Gitterfläche ab, zu der jeder textexgehört.<br/>                           |
| [**Getguttermap**](id3dxtexturegutterhelper--getguttermap.md)           | Empfängt einen Texel-Klassen Wert, der Texttypen entsprechend der Position jedes Texttyps angibt.<br/> |
| [**GetHeight**](id3dxtexturegutterhelper--getheight.md)                 | Ruft die Höhe der Textur in Pixel ab.<br/>                                             |
| [**Gettexelmap**](id3dxtexturegutterhelper--gettexelmap.md)             | Ruft die Texturkoordinaten (u, v) der einzelnen texaus.<br/>                                     |
| [**GetWidth**](id3dxtexturegutterhelper--getwidth.md)                   | Ruft die Breite der Textur in Pixel ab.<br/>                                              |
| [**Resampletex**](id3dxtexturegutterhelper--resampletex.md)             | Erstellt eine Textur in der Parametrisierung dieses gutterhelper neu.<br/>                              |
| [**Setbarymap**](id3dxtexturegutterhelper--setbarymap.md)               | Legt texzentrische texse-Koordinaten fest.<br/>                                                         |
| [**Setfacemap**](id3dxtexturegutterhelper--setfacemap.md)               | Legt den Index des Mesh-Blatts fest, zu dem die einzelnen textengehören.<br/>                                |
| [**Setguttermap**](id3dxtexturegutterhelper--setguttermap.md)           | Legt einen Texel-Klassen Wert fest, der Texttypen entsprechend der Position jedes Texttyps angibt.<br/>     |
| [**Settexelmap**](id3dxtexturegutterhelper--settexelmap.md)             | Legt die Texturkoordinaten (u, v) der einzelnen textsets fest.<br/>                                          |



 

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Bei Verwendung mit preberechneter Radiance Transfer (PRT) erfordert diese Schnittstelle eine eindeutige Parametrisierung des Modells. Alle textexendas müssen einem einzelnen Punkt auf der Oberfläche des Modells entsprechen und umgekehrt. Wenn das Modell mehrere Texturen enthält, muss es in separate Teile aufgeteilt werden, die jeweils ein bundfügobjekt pro Textur enthalten.

 

Diese Schnittstelle kann verwendet werden, um eine Karte im Textur Bereich zu generieren, in der jeder Texin einer von vier Klassen ist.



| Texel-Klasse | Textsort                                                                                                                                                                                                                                                                                                                                                                |
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0           | Ungültiger Punkt; Texel wird nicht verwendet.                                                                                                                                                                                                                                                                                                                                        |
| 1           | Innerhalb des Dreiecks.                                                                                                                                                                                                                                                                                                                                                              |
| 2           | Im bundbundbereich.                                                                                                                                                                                                                                                                                                                                                                |
| 4           | Im bundbundbereich; Texel wird als vollständiges Beispiel in der [**ID3DXTextureGutterHelper:: applyguttersfloat**](id3dxtexturegutterhelper--applyguttersfloat.md), [**ID3DXTextureGutterHelper:: applygutterstex**](id3dxtexturegutterhelper--applygutterstex.md)-Methode oder der [**ID3DXTextureGutterHelper:: applyguttersprt**](id3dxtexturegutterhelper--applyguttersprt.md) -Methode ausgewertet. |



 

Bei den Klassen 1 und 2 wird ein textpaar mit der Fläche gespeichert, zu der es gehört, zusammen mit den nicht auf die ersten beiden Scheitel Punkten der Fläche ausgerichteten Koordinaten. Der am nächsten liegenden Rand im Textur Bereich zugeordnete bundces.

Es ist keine Texel-Klasse 3 vorhanden.

Die **ID3DXTextureGutterHelper** -Schnittstelle wird durch Aufrufen der [**D3DXCreateTextureGutterHelper**](d3dxcreatetexturegutterhelper.md) -Funktion abgerufen.

Der LPD3DXTEXTUREGUTTERHELPER-Typ wird als Zeiger auf die **ID3DXTextureGutterHelper** -Schnittstelle definiert.


```
typedef interface ID3DXTextureGutterHelper ID3DXTextureGutterHelper;
typedef interface ID3DXTextureGutterHelper *LPD3DXTEXTUREGUTTERHELPER;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Schnittstellen](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
