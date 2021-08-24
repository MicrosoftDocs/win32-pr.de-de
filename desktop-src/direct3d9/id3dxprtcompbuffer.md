---
description: Die ID3DXPRTCompBuffer-Schnittstelle speichert eine komprimierte Version eines ID3DXPRTBuffer-Puffers zur Verwendung mit der Prinzipalkomponentenanalyse (Principal Component Analysis, PCA).
ms.assetid: 97f8576c-24d5-4f60-923b-4d8d94382fe9
title: ID3DXPRTCompBuffer-Schnittstelle (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTCompBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a84f1bc7b25af0c900f5587ba0d1dd948cac39bc52f706ff389c0ca9d053ec0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119985610"
---
# <a name="id3dxprtcompbuffer-interface"></a>ID3DXPRTCompBuffer-Schnittstelle

Die **ID3DXPRTCompBuffer-Schnittstelle** speichert eine komprimierte Version eines [**ID3DXPRTBuffer-Puffers**](id3dxprtbuffer.md) zur Verwendung mit der Prinzipalkomponentenanalyse (Principal Component Analysis, PCA).

## <a name="members"></a>Member

Die **ID3DXPRTCompBuffer-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ID3DXPRTCompBuffer** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DXPRTCompBuffer-Schnittstelle** verfügt über diese Methoden.



| Methode                                                             | BESCHREIBUNG                                                                                                                                                                                                                        |
|:-------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ExtractBasis**](id3dxprtcompbuffer--extractbasis.md)           | Extrahiert die Basisvektoren der Mittleren und Prinzipalkomponentenanalyse (PCA) für einen bestimmten Cluster aus einem komprimierten **ID3DXPRTCompBuffer-Datenpuffer.**<br/>                                                                       |
| [**ExtractClusterIDs**](id3dxprtcompbuffer--extractclusterids.md) | Extrahiert die pro Beispiel verwendeten Cluster-IDs aus einem komprimierten **ID3DXPRTCompBuffer-Datenpuffer.**<br/>                                                                                                                              |
| [**ExtractPCA**](id3dxprtcompbuffer--extractpca.md)               | Extrahiert die Pro-Sample-Projektionskoeffizienten für die Prinzipalkomponentenanalyse (Principal Component Analysis, PCA) aus einem komprimierten **ID3DXPRTCompBuffer-Datenpuffer.**<br/>                                                                               |
| [**ExtractTexture**](id3dxprtcompbuffer--extracttexture.md)       | Extrahiert die Pro-Sample-Projektionskoeffizienten für die Prinzipalkomponentenanalyse (Principal Component Analysis, PCA) aus einem komprimierten **ID3DXPRTCompBuffer-Datenpuffer** und fügt die Daten einem [**IDirect3DTexture9-Objekt**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) hinzu.<br/> |
| [**ExtractToMesh**](id3dxprtcompbuffer--extracttomesh.md)         | Extrahiert die Pro-Sample-Projektionskoeffizienten für die Prinzipalkomponentenanalyse (Principal Component Analysis, PCA) aus einem komprimierten **ID3DXPRTCompBuffer-Datenpuffer** und fügt die Daten einem [**ID3DXMesh-Objekt**](id3dxmesh.md) hinzu.<br/>                 |
| [**Font.getheight**](id3dxprtcompbuffer--getheight.md)                 | Ruft die Höhe der Textur in Pixel ab.<br/>                                                                                                                                                                         |
| [**GetNumChannels**](id3dxprtcompbuffer--getnumchannels.md)       | Ruft die Anzahl der Farbkanäle ab, die im Arbeitsspeicher zum Speichern von Beispielen verwendet werden.<br/>                                                                                                                                                 |
| [**GetNumClusters**](id3dxprtcompbuffer--getnumclusters.md)       | Ruft die Anzahl der Cluster ab, die für die Komprimierung verwendet werden sollen.<br/>                                                                                                                                                                |
| [**GetNumCoeffs**](id3dxprtcompbuffer--getnumcoeffs.md)           | Ruft die Anzahl von Skalaren pro Farbkanal ab, die im Arbeitsspeicher zum Speichern von Stichproben verwendet werden.<br/>                                                                                                                                      |
| [**GetNumPCA**](id3dxprtcompbuffer--getnumpca.md)                 | Ruft die Anzahl der Basisvektoren für die Prinzipalkomponentenanalyse (Principal Component Analysis, PCA) ab, die in jedem Cluster verwendet werden sollen.<br/>                                                                                                                        |
| [**GetNumSamples**](id3dxprtcompbuffer--getnumsamples.md)         | Ruft die Anzahl der Scheitelpunkte (oder Texel) ab, die als Stichprobe entnommen wurden.<br/>                                                                                                                                                                   |
| [**GetWidth**](id3dxprtcompbuffer--getwidth.md)                   | Ruft die Breite der Textur in Pixel ab.<br/>                                                                                                                                                                          |
| [**IsTexture**](id3dxprtcompbuffer--istexture.md)                 | Gibt an, ob der Puffer eine Textur enthält.<br/>                                                                                                                                                                        |
| [**NormalizeData**](id3dxprtcompbuffer--normalizedata.md)         | Normalisiert alle Gewichtungen der Hauptkomponentenanalyse (Principal Component Analysis, PCA), sodass sie zwischen -1 und 1 liegen. Basisvektoren werden geändert, um diese Normalisierung widerzuspiegeln.<br/>                                                                  |



 

## <a name="remarks"></a>Hinweise

Die **ID3DXPRTCompBuffer-Schnittstelle** wird durch Aufrufen der [**D3DXCreatePRTCompBuffer-Funktion**](d3dxcreateprtcompbuffer.md) abgerufen.

Der LPD3DXPRTCOMPBUFFER-Typ wird als Zeiger auf die **ID3DXPRTCompBuffer-Schnittstelle** definiert.


```
typedef interface ID3DXPRTCompBuffer ID3DXPRTCompBuffer;
typedef interface ID3DXPRTCompBuffer *LPD3DXPRTCOMPBUFFER;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Schnittstellen](dx9-graphics-reference-d3dx-interfaces.md)
</dt> <dt>

[**D3DXCreatePRTCompBuffer**](d3dxcreateprtcompbuffer.md)
</dt> <dt>

[**ID3DXPRTBuffer**](id3dxprtbuffer.md)
</dt> </dl>

 

 
