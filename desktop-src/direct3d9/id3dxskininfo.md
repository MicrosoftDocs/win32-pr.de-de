---
description: Anwendungen verwenden die Methoden der ID3DXSkinInfo-Schnittstelle, um Matrizen zu bearbeiten, die zum Skinn von Scheitelpunktdaten für Animationen verwendet werden. Diese Schnittstelle ist nicht mehr streng an ID3DXMesh gebunden und kann zum Skinn beliebiger Scheitelpunktdaten verwendet werden.
ms.assetid: 4ccf88b0-2cc7-4e91-a0f2-fb8eea66a3ce
title: ID3DXSkinInfo-Schnittstelle (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0d7bfeddb5cb34bb9b5d0372f424c40248f06e55fa7263e1e884e71fb82dafcb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119727760"
---
# <a name="id3dxskininfo-interface"></a>ID3DXSkinInfo-Schnittstelle

Anwendungen verwenden die Methoden der ID3DXSkinInfo-Schnittstelle, um Matrizen zu bearbeiten, die zum Skinn von Scheitelpunktdaten für Animationen verwendet werden. Diese Schnittstelle ist nicht mehr streng an [**ID3DXMesh**](id3dxmesh.md) gebunden und kann zum Skinn beliebiger Scheitelpunktdaten verwendet werden.

## <a name="members"></a>Member

Die **ID3DXSkinInfo-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ID3DXSkinInfo** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DXSkinInfo-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                              | Beschreibung                                                                                                                                                                                    |
|:------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Klon**](id3dxskininfo--clone.md)                                               | Klont ein Skininformationsobjekt.<br/>                                                                                                                                                          |
| [**ConvertToBlendedMesh**](id3dxskininfo--converttoblendedmesh.md)                 | Nimmt ein Gitternetz und gibt ein neues Gitternetz mit Mischungsgewichtungen pro Scheitelpunkt und einer Kombinationstabelle zurück. In der Tabelle wird beschrieben, welche Ausschnitte sich auf die Teilmengen des Gitternetzes auswirken.<br/>                   |
| [**ConvertToIndexedBlendedMesh**](id3dxskininfo--converttoindexedblendedmesh.md)   | Nimmt ein Gitternetz und gibt ein neues Gitternetz mit Mischungsgewichtungen, Indizes und einer Kombinationstabelle pro Scheitelpunkt zurück. In der Tabelle wird beschrieben, welche Paletten sich auf die Teilmengen des Gitternetzes auswirken.<br/> |
| [**FindBoneVertexInfluenceIndex**](id3dxskininfo--findbonevertexinfluenceindex.md) | Ruft den Index des Einflusses ab, der sich auf einen einzelnen Scheitelpunkt auswirkt.<br/>                                                                                                                |
| [**GetBoneInfluence**](id3dxskininfo--getboneinfluence.md)                         | Ruft die Scheitelpunkte und Gewichtungen ab, die ein Gitter beeinflusst.<br/>                                                                                                                               |
| [**GetBoneName**](id3dxskininfo--getbonename.md)                                   | Ruft den Namen des Verzeichnisses aus dem Index ab.<br/>                                                                                                                                            |
| [**GetBoneOffsetMatrix**](id3dxskininfo--getboneoffsetmatrix.md)                   | Ruft die Offsetmatrix des Offsets ab.<br/>                                                                                                                                                        |
| [**GetBoneVertexInfluence**](id3dxskininfo--getbonevertexinfluence.md)             | Ruft den Mischungsfaktor und den Scheitelpunkt ab, die von einem angegebenen Einflussfaktor betroffen sind.<br/>                                                                                                       |
| [**GetDeclaration**](id3dxskininfo--getdeclaration.md)                             | Ruft die Scheitelpunktdeklaration ab.<br/>                                                                                                                                                        |
| [**GetFVF**](id3dxskininfo--getfvf.md)                                             | Ruft den vertex-Wert der festen Funktion ab.<br/>                                                                                                                                               |
| [**GetMaxFaceInfluences**](id3dxskininfo--getmaxfaceinfluences.md)                 | Ruft die maximalen Gesichtseinflüsse in einem Dreiecksgitternetz mit dem angegebenen Indexpuffer ab.<br/>                                                                                                |
| [**GetMaxVertexInfluences**](id3dxskininfo--getmaxvertexinfluences.md)             | Ruft die maximale Anzahl von Einflussfaktoren für jeden Scheitelpunkt im Netz ab.<br/>                                                                                                                   |
| [**GetMinBoneInfluence**](id3dxskininfo--getminboneinfluence.md)                   | Ruft den minimalen Einfluss des Einflusses ab. Einflusswerte, die kleiner als diese sind, werden ignoriert.<br/>                                                                                                    |
| [**GetNumBoneInfluences**](id3dxskininfo--getnumboneinfluences.md)                 | Ruft die Anzahl der Einflussfaktoren für einen Ochsen ab.<br/>                                                                                                                                           |
| [**GetNumBones**](id3dxskininfo--getnumbones.md)                                   | Ruft die Anzahl der Brüche ab.<br/>                                                                                                                                                           |
| [**Remap**](id3dxskininfo--remap.md)                                               | Updates beeinflussen Informationen, um Scheitelpunkte abzugleichen, nachdem sie neu angeordnet wurden. Diese Methode sollte aufgerufen werden, wenn der Zielvertexpuffer extern neu angeordnet wurde.<br/>              |
| [**SetBoneInfluence**](id3dxskininfo--setboneinfluence.md)                         | Legt den Einflusswert für einen Fluss fest.<br/>                                                                                                                                                |
| [**SetBoneName**](id3dxskininfo--setbonename.md)                                   | Legt den Namen der Bezeichnung fest.<br/>                                                                                                                                                                 |
| [**SetBoneOffsetMatrix**](id3dxskininfo--setboneoffsetmatrix.md)                   | Legt die Offsetmatrix des Offsets fest.<br/>                                                                                                                                                        |
| [**SetBoneVertexInfluence**](id3dxskininfo--setbonevertexinfluence.md)             | Legt einen Einflusswert eines Würfes auf einen einzelnen Scheitelpunkt fest.<br/>                                                                                                                               |
| [**SetDeclaration**](id3dxskininfo--setdeclaration.md)                             | Legt die Scheitelpunktdeklaration fest.<br/>                                                                                                                                                        |
| [**SetFVF**](id3dxskininfo--setfvf.md)                                             | Legt den FVF-Typ (Flexible Vertex Format) fest.<br/>                                                                                                                                         |
| [**SetMinBoneInfluence**](id3dxskininfo--setminboneinfluence.md)                   | Legt den minimalen Einfluss des Einflusses fest. Einflusswerte, die kleiner als diese sind, werden ignoriert.<br/>                                                                                                    |
| [**UpdateSkinnedMesh**](id3dxskininfo--updateskinnedmesh.md)                       | Wendet das Softwareskinning auf die Zielvertices basierend auf den aktuellen Matrizen an.<br/>                                                                                                     |



 

## <a name="remarks"></a>Hinweise

Erstellen Sie eine **ID3DXSkinInfo-Schnittstelle** mit [**D3DXCreateSkinInfo,**](d3dxcreateskininfo.md) [**D3DXCreateSkinInfoFromBlendedMesh**](d3dxcreateskininfofromblendedmesh.md)oder [**D3DXCreateSkinInfoFVF**](d3dxcreateskininfofvf.md).

Der LPD3DXSKININFO-Typ wird als Zeiger auf die **ID3DXSkinInfo-Schnittstelle** definiert.


```
typedef struct ID3DXSkinInfo *LPD3DXSKININFO;
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

 

 
