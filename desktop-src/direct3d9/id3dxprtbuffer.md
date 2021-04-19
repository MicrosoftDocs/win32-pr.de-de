---
description: Die ID3DXPRTBuffer-Schnittstelle wird als Datenpuffer zum Speichern von Scheitelpunkt-und Pixeldaten für die Verwendung mit PRT-Methoden und-Funktionen verwendet.
ms.assetid: 36c1fd13-0949-4991-93cb-41ace458802d
title: ID3DXPRTBuffer-Schnittstelle (D3DX9Mesh. h)
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
ms.openlocfilehash: daadb5b0ad8155062e75ea4eca566a0afbf3631b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106350736"
---
# <a name="id3dxprtbuffer-interface"></a>ID3DXPRTBuffer-Schnittstelle

Die ID3DXPRTBuffer-Schnittstelle wird als Datenpuffer zum Speichern von Scheitelpunkt-und Pixeldaten für die Verwendung mit PRT-Methoden und-Funktionen verwendet.

## <a name="members"></a>Member

Die **ID3DXPRTBuffer** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **ID3DXPRTBuffer** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DXPRTBuffer** -Schnittstelle verfügt über diese Methoden.



| Methode                                                   | BESCHREIBUNG                                                                                                                                                                                   |
|:---------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Addbuffer**](id3dxprtbuffer--addbuffer.md)           | Fügt der **ID3DXPRTBuffer** einen weiteren Puffer hinzu und speichert die Ergebnisse in **ID3DXPRTBuffer**.<br/>                                                                                        |
| [**Attachgh**](id3dxprtbuffer--attachgh.md)             | Verknüpft ein [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) -Objekt mit dem **ID3DXPRTBuffer** -Objekt.<br/>                                                              |
| [**Evalgh**](id3dxprtbuffer--evalgh.md)                 | Wendet gespeicherte Textur Daten auf einen **ID3DXPRTBuffer** -Textur Puffer an.<br/>                                                                                                        |
| [**Extracttexture**](id3dxprtbuffer--extracttexture.md) | Extrahiert Koeffizient Daten aus einem Farbkanal des Puffers für einen angegebenen Bereich von Koeffizienten und fügt die Daten einem [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) -Objekt hinzu.<br/> |
| [**Extracttomesh**](id3dxprtbuffer--extracttomesh.md)   | Extrahiert Koeffizienten-Daten aus einem Puffer mit einem einzelnen Kanal und fügt die Daten einem [**ID3DXMesh**](id3dxmesh.md) -Objekt hinzu.<br/>                                                              |
| [**GetHeight**](id3dxprtbuffer--getheight.md)           | Ruft die Höhe der Textur in Pixel ab.<br/>                                                                                                                                    |
| [**Getnumchannels**](id3dxprtbuffer--getnumchannels.md) | Ruft die Anzahl der Farbkanäle ab, die im Arbeitsspeicher zum Speichern von Beispielen verwendet werden.<br/>                                                                                                            |
| [**Getnumcoeffs**](id3dxprtbuffer--getnumcoeffs.md)     | Ruft die Anzahl der skalare pro Farbkanal ab, die im Arbeitsspeicher zum Speichern von Beispielen verwendet werden.<br/>                                                                                                 |
| [**Getnumsamples**](id3dxprtbuffer--getnumsamples.md)   | Ruft die Anzahl der abtasteten Scheitel Punkte (oder Texels) ab.<br/>                                                                                                                              |
| [**GetWidth**](id3dxprtbuffer--getwidth.md)             | Ruft die Breite der Textur in Pixel ab.<br/>                                                                                                                                     |
| [**IsTexture**](id3dxprtbuffer--istexture.md)           | Gibt an, ob der Puffer eine Textur enthält.<br/>                                                                                                                                   |
| [**LockBuffer**](id3dxprtbuffer--lockbuffer.md)         | Sperrt einen Bereich von Vertex-oder Texel-Beispiel Daten und erhält einen Zeiger auf die Position im Pufferspeicher.<br/>                                                                               |
| [**Releasegh**](id3dxprtbuffer--releasegh.md)           | Hebt die Zuordnung eines angefügten [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) -Objekts zum **ID3DXPRTBuffer** -Objekt auf.<br/>                                                   |
| [**Größe ändern**](id3dxprtbuffer--resize.md)                 | Ändert die Anzahl der im Puffer enthaltenen Stichproben.<br/>                                                                                                                             |
| [**Scalebuffer**](id3dxprtbuffer--scalebuffer.md)       | Multipliziert jeden Wert im Puffer mit einem konstanten Wert.<br/>                                                                                                                          |
| [**UnlockBuffer**](id3dxprtbuffer--unlockbuffer.md)     | Beendet die Lebensdauer des ppData-Zeigers, der von [**ID3DXPRTBuffer:: LockBuffer**](id3dxprtbuffer--lockbuffer.md)zurückgegeben wurde.<br/>                                                              |



 

## <a name="remarks"></a>Bemerkungen

Die **ID3DXPRTBuffer** -Schnittstelle wird durch Aufrufen der [**D3DXCreatePRTBuffer**](d3dxcreateprtbuffer.md) -Funktion oder der [**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md) -Funktion abgerufen.

Der LPD3DXPRTBUFFER-Typ wird als Zeiger auf die **ID3DXPRTBuffer** -Schnittstelle definiert.


```
typedef interface ID3DXPRTBuffer ID3DXPRTBuffer;
typedef interface ID3DXPRTBuffer *LPD3DXPRTBUFFER;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Schnittstellen](dx9-graphics-reference-d3dx-interfaces.md)
</dt> <dt>

[**D3DXCreatePRTBuffer**](d3dxcreateprtbuffer.md)
</dt> <dt>

[**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md)
</dt> <dt>

[**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md)
</dt> </dl>

 

 
