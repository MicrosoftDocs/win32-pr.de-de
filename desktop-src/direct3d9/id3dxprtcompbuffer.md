---
description: Die ID3DXPRTCompBuffer-Schnittstelle speichert eine komprimierte Version eines ID3DXPRTBuffer-Puffers für die Verwendung mit der Principal Component Analysis (PCA).
ms.assetid: 97f8576c-24d5-4f60-923b-4d8d94382fe9
title: ID3DXPRTCompBuffer-Schnittstelle (D3DX9Mesh. h)
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
ms.openlocfilehash: 323ed6f2bbe9ce4caf495a00330c1b1e0e83e158
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106365128"
---
# <a name="id3dxprtcompbuffer-interface"></a>ID3DXPRTCompBuffer-Schnittstelle

Die **ID3DXPRTCompBuffer** -Schnittstelle speichert eine komprimierte Version eines [**ID3DXPRTBuffer**](id3dxprtbuffer.md) -Puffers für die Verwendung mit der Principal Component Analysis (PCA).

## <a name="members"></a>Member

Die **ID3DXPRTCompBuffer** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **ID3DXPRTCompBuffer** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DXPRTCompBuffer** -Schnittstelle verfügt über diese Methoden.



| Methode                                                             | BESCHREIBUNG                                                                                                                                                                                                                        |
|:-------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Extractbasis**](id3dxprtcompbuffer--extractbasis.md)           | Extrahiert den Mittelwert und die Hauptkomponentenanalyse (PCA) für einen bestimmten Cluster aus einem **ID3DXPRTCompBuffer** -komprimierten Datenpuffer.<br/>                                                                       |
| [**Extractclusterids**](id3dxprtcompbuffer--extractclusterids.md) | Extrahiert die Cluster-IDs pro Beispiel aus einem komprimierten **ID3DXPRTCompBuffer** -Datenpuffer.<br/>                                                                                                                              |
| [**Extractpca**](id3dxprtcompbuffer--extractpca.md)               | Extrahiert die pro-Beispiel-PCA-Projektions Koeffizienten (Principal Component Analysis) aus einem komprimierten **ID3DXPRTCompBuffer** -Datenpuffer.<br/>                                                                               |
| [**Extracttexture**](id3dxprtcompbuffer--extracttexture.md)       | Extrahiert die pro-Beispiel-PCA-Projektions Koeffizienten (Principal Component Analysis) aus einem komprimierten **ID3DXPRTCompBuffer** -Datenpuffer und fügt die Daten einem [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) -Objekt hinzu.<br/> |
| [**Extracttomesh**](id3dxprtcompbuffer--extracttomesh.md)         | Extrahiert die pro-Beispiel-PCA-Projektions Koeffizienten (Principal Component Analysis) aus einem komprimierten **ID3DXPRTCompBuffer** -Datenpuffer und fügt die Daten einem [**ID3DXMesh**](id3dxmesh.md) -Objekt hinzu.<br/>                 |
| [**GetHeight**](id3dxprtcompbuffer--getheight.md)                 | Ruft die Höhe der Textur in Pixel ab.<br/>                                                                                                                                                                         |
| [**Getnumchannels**](id3dxprtcompbuffer--getnumchannels.md)       | Ruft die Anzahl der Farbkanäle ab, die im Arbeitsspeicher zum Speichern von Beispielen verwendet werden.<br/>                                                                                                                                                 |
| [**Getnumclusters**](id3dxprtcompbuffer--getnumclusters.md)       | Ruft die Anzahl der Cluster ab, die für die Komprimierung verwendet werden sollen.<br/>                                                                                                                                                                |
| [**Getnumcoeffs**](id3dxprtcompbuffer--getnumcoeffs.md)           | Ruft die Anzahl der skalare pro Farbkanal ab, die im Arbeitsspeicher zum Speichern von Beispielen verwendet werden.<br/>                                                                                                                                      |
| [**Getnumpca**](id3dxprtcompbuffer--getnumpca.md)                 | Ruft die Anzahl der in jedem Cluster zu verwendenden PCA-Vektoren (Principal Component Analysis) ab.<br/>                                                                                                                        |
| [**Getnumsamples**](id3dxprtcompbuffer--getnumsamples.md)         | Ruft die Anzahl der abtasteten Scheitel Punkte (oder Texels) ab.<br/>                                                                                                                                                                   |
| [**GetWidth**](id3dxprtcompbuffer--getwidth.md)                   | Ruft die Breite der Textur in Pixel ab.<br/>                                                                                                                                                                          |
| [**IsTexture**](id3dxprtcompbuffer--istexture.md)                 | Gibt an, ob der Puffer eine Textur enthält.<br/>                                                                                                                                                                        |
| [**Normalizedata**](id3dxprtcompbuffer--normalizedata.md)         | Normalisiert alle PCA-Gewichtungen (Principal Component Analysis), sodass Sie zwischen-1 und 1 liegen. Basis Vektoren werden geändert, um diese Normalisierung widerzuspiegeln.<br/>                                                                  |



 

## <a name="remarks"></a>Bemerkungen

Die **ID3DXPRTCompBuffer** -Schnittstelle wird durch Aufrufen der [**D3DXCreatePRTCompBuffer**](d3dxcreateprtcompbuffer.md) -Funktion abgerufen.

Der LPD3DXPRTCOMPBUFFER-Typ wird als Zeiger auf die **ID3DXPRTCompBuffer** -Schnittstelle definiert.


```
typedef interface ID3DXPRTCompBuffer ID3DXPRTCompBuffer;
typedef interface ID3DXPRTCompBuffer *LPD3DXPRTCOMPBUFFER;
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

[**D3DXCreatePRTCompBuffer**](d3dxcreateprtcompbuffer.md)
</dt> <dt>

[**ID3DXPRTBuffer**](id3dxprtbuffer.md)
</dt> </dl>

 

 
