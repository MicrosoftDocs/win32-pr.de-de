---
description: Die ID3DXPRTBuffer-Schnittstelle wird als Datenpuffer verwendet, um Scheitelpunkt- und Pixeldaten für die Verwendung mit prt-Methoden und -Funktionen (Precomputed Radiance Transfer) zu speichern.
ms.assetid: 36c1fd13-0949-4991-93cb-41ace458802d
title: ID3DXPRTBuffer-Schnittstelle (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 69f4a40055adea1440436cc54cecc5735db95bc01787cb779cc8a7d6c51b0011
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119120544"
---
# <a name="id3dxprtbuffer-interface"></a>ID3DXPRTBuffer-Schnittstelle

Die ID3DXPRTBuffer-Schnittstelle wird als Datenpuffer verwendet, um Scheitelpunkt- und Pixeldaten für die Verwendung mit prt-Methoden und -Funktionen (Precomputed Radiance Transfer) zu speichern.

## <a name="members"></a>Member

Die **ID3DXPRTBuffer-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ID3DXPRTBuffer** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DXPRTBuffer-Schnittstelle** verfügt über diese Methoden.



| Methode                                                   | BESCHREIBUNG                                                                                                                                                                                   |
|:---------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddBuffer**](id3dxprtbuffer--addbuffer.md)           | Fügt dem **ID3DXPRTBuffer** einen weiteren Puffer hinzu und speichert die Ergebnisse in **ID3DXPRTBuffer.**<br/>                                                                                        |
| [**AttachGH**](id3dxprtbuffer--attachgh.md)             | Ordnet dem **ID3DXPRTBuffer-Objekt** ein [**ID3DXTextureGutterHelper-Objekt**](id3dxtexturegutterhelper.md) zu.<br/>                                                              |
| [**EvalGH**](id3dxprtbuffer--evalgh.md)                 | Wendet gespeicherte Textur-Gutterdaten auf einen **ID3DXPRTBuffer-Texturpuffer** an.<br/>                                                                                                        |
| [**ExtractTexture**](id3dxprtbuffer--extracttexture.md) | Extrahiert Koeffizientsdaten aus einem Farbkanal des Puffers für einen angegebenen Bereich von Koeffizienten und fügt die Daten einem [**IDirect3DTexture9-Objekt**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) hinzu.<br/> |
| [**ExtractToMesh**](id3dxprtbuffer--extracttomesh.md)   | Extrahiert Koeffizientsdaten aus einem Einkanalpuffer und fügt die Daten einem [**ID3DXMesh-Objekt**](id3dxmesh.md) hinzu.<br/>                                                              |
| [**Font.getheight**](id3dxprtbuffer--getheight.md)           | Ruft die Höhe der Textur in Pixel ab.<br/>                                                                                                                                    |
| [**GetNumChannels**](id3dxprtbuffer--getnumchannels.md) | Ruft die Anzahl der Farbkanäle ab, die im Arbeitsspeicher zum Speichern von Beispielen verwendet werden.<br/>                                                                                                            |
| [**GetNumCoeffs**](id3dxprtbuffer--getnumcoeffs.md)     | Ruft die Anzahl von Skalaren pro Farbkanal ab, die im Arbeitsspeicher zum Speichern von Stichproben verwendet werden.<br/>                                                                                                 |
| [**GetNumSamples**](id3dxprtbuffer--getnumsamples.md)   | Ruft die Anzahl der Scheitelpunkte (oder Texel) ab, die als Stichprobe entnommen wurden.<br/>                                                                                                                              |
| [**GetWidth**](id3dxprtbuffer--getwidth.md)             | Ruft die Breite der Textur in Pixel ab.<br/>                                                                                                                                     |
| [**IsTexture**](id3dxprtbuffer--istexture.md)           | Gibt an, ob der Puffer eine Textur enthält.<br/>                                                                                                                                   |
| [**LockBuffer**](id3dxprtbuffer--lockbuffer.md)         | Sperrt einen Bereich von Scheitelpunkt- oder Texel-Beispieldaten und ruft einen Zeiger auf die Position im Pufferspeicher ab.<br/>                                                                               |
| [**ReleaseGH**](id3dxprtbuffer--releasegh.md)           | Aufheben der Zuordnung eines angefügten [**ID3DXTextureGutterHelper-Objekts**](id3dxtexturegutterhelper.md) zum **ID3DXPRTBuffer-Objekt.**<br/>                                                   |
| [**Größe ändern**](id3dxprtbuffer--resize.md)                 | Ändert die Anzahl der im Puffer enthaltenen Stichproben.<br/>                                                                                                                             |
| [**ScaleBuffer**](id3dxprtbuffer--scalebuffer.md)       | Multipliziert jeden Wert im Puffer mit einem konstanten Wert.<br/>                                                                                                                          |
| [**UnlockBuffer**](id3dxprtbuffer--unlockbuffer.md)     | Beendet die Lebensdauer des ppData-Zeigers, der von [**ID3DXPRTBuffer::LockBuffer**](id3dxprtbuffer--lockbuffer.md)zurückgegeben wird.<br/>                                                              |



 

## <a name="remarks"></a>Hinweise

Die **ID3DXPRTBuffer-Schnittstelle** wird durch Aufrufen der Funktionen [**D3DXCreatePRTBuffer**](d3dxcreateprtbuffer.md) oder [**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md) abgerufen.

Der LPD3DXPRTBUFFER-Typ wird als Zeiger auf die **ID3DXPRTBuffer-Schnittstelle** definiert.


```
typedef interface ID3DXPRTBuffer ID3DXPRTBuffer;
typedef interface ID3DXPRTBuffer *LPD3DXPRTBUFFER;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[D3DX-Schnittstellen](dx9-graphics-reference-d3dx-interfaces.md)
</dt> <dt>

[**D3DXCreatePRTBuffer**](d3dxcreateprtbuffer.md)
</dt> <dt>

[**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md)
</dt> <dt>

[**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md)
</dt> </dl>

 

 
