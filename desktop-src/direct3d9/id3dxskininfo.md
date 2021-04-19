---
description: Anwendungen verwenden die Methoden der ID3DXSkinInfo-Schnittstelle, um die für die Animation von Vertex-Daten verwendete Ober Matrizen zu bearbeiten. Diese Schnittstelle ist nicht mehr strikt an ID3DXMesh gebunden und kann verwendet werden, um einen beliebigen Satz von Scheitelpunkt Daten zu Skin.
ms.assetid: 4ccf88b0-2cc7-4e91-a0f2-fb8eea66a3ce
title: ID3DXSkinInfo-Schnittstelle (D3DX9Mesh. h)
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
ms.openlocfilehash: afb93a0513bef7de1b0815b8b1f50179e2cba41d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106365301"
---
# <a name="id3dxskininfo-interface"></a>ID3DXSkinInfo-Schnittstelle

Anwendungen verwenden die Methoden der ID3DXSkinInfo-Schnittstelle, um die für die Animation von Vertex-Daten verwendete Ober Matrizen zu bearbeiten. Diese Schnittstelle ist nicht mehr strikt an [**ID3DXMesh**](id3dxmesh.md) gebunden und kann verwendet werden, um einen beliebigen Satz von Scheitelpunkt Daten zu Skin.

## <a name="members"></a>Member

Die **ID3DXSkinInfo** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **ID3DXSkinInfo** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DXSkinInfo** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                              | BESCHREIBUNG                                                                                                                                                                                    |
|:------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Klon**](id3dxskininfo--clone.md)                                               | Klont ein Skin Info-Objekt.<br/>                                                                                                                                                          |
| [**Convertumblendedmesh**](id3dxskininfo--converttoblendedmesh.md)                 | Nimmt ein Mesh an und gibt ein neues Mesh mit pro-vertexblend-Gewichtungen und einer Tabelle mit einer Kombination aus der Tabelle zurück In der Tabelle ist beschrieben, welche Knochen welche Teilmengen des Netzes beeinflussen.<br/>                   |
| [**Convertinindexedblendedmesh**](id3dxskininfo--converttoindexedblendedmesh.md)   | Nimmt ein Mesh an und gibt ein neues Mesh mit pro-Vertex-Blend-Gewichtungen,-Indizes und einer Bone-Kombinations Tabelle zurück. In der Tabelle wird beschrieben, welche Knochen Paletten welche Teilmengen des Netzes beeinflussen.<br/> |
| [**Findbonevertexinfluendceindex**](id3dxskininfo--findbonevertexinfluenceindex.md) | Ruft den Index des Knochen Einflusses ab, der sich auf einen einzelnen Scheitelpunkt auswirkt.<br/>                                                                                                                |
| [**Getboneingefluence**](id3dxskininfo--getboneinfluence.md)                         | Ruft die Scheitel Punkte und Gewichtungen ab, die ein Knochen beeinflusst.<br/>                                                                                                                               |
| [**Getbonename**](id3dxskininfo--getbonename.md)                                   | Ruft den Feldnamen aus dem-MarkerIndex ab.<br/>                                                                                                                                            |
| [**Getboneoffsetmatrix**](id3dxskininfo--getboneoffsetmatrix.md)                   | Ruft die markveroffsetmatrix ab.<br/>                                                                                                                                                        |
| [**Getbonevertexinfluence**](id3dxskininfo--getbonevertexinfluence.md)             | Ruft den Blend Faktor und den Scheitelpunkt ab, der von einem angegebenen Knochen Einfluss betroffen ist.<br/>                                                                                                       |
| [**GetDeclaration**](id3dxskininfo--getdeclaration.md)                             | Ruft die Vertex-Deklaration ab.<br/>                                                                                                                                                        |
| [**Getf VF**](id3dxskininfo--getfvf.md)                                             | Ruft den Scheitelpunkt Wert fester Funktion ab.<br/>                                                                                                                                               |
| [**Getmaxfakeingefluences**](id3dxskininfo--getmaxfaceinfluences.md)                 | Ruft die maximalen Gesichts Einflüsse in einem Dreiecks Mesh mit dem angegebenen Index Puffer ab.<br/>                                                                                                |
| [**Getmaxvertexeinflüsse**](id3dxskininfo--getmaxvertexinfluences.md)             | Ruft die maximale Anzahl von Einflüssen für einen Scheitelpunkt im Mesh ab.<br/>                                                                                                                   |
| [**Getminboneingefluence**](id3dxskininfo--getminboneinfluence.md)                   | Ruft den minimalen Knochen Einfluss ab. Werte, die kleiner als dieser Wert sind, werden ignoriert.<br/>                                                                                                    |
| [**Getnumboneingefluences**](id3dxskininfo--getnumboneinfluences.md)                 | Ruft die Anzahl der Einflüsse für einen Knochen ab.<br/>                                                                                                                                           |
| [**Getnumbones**](id3dxskininfo--getnumbones.md)                                   | Ruft die Anzahl der Knochen ab.<br/>                                                                                                                                                           |
| [**Umwandlungs**](id3dxskininfo--remap.md)                                               | Aktualisiert die Informationen zu den Informationen zu den Daten, die nach dem erneuten ordnen der Scheitel Punkte entsprechen Diese Methode sollte aufgerufen werden, wenn der Ziel Vertex-Puffer extern neu angeordnet wurde.<br/>              |
| [**Setboneingefluence**](id3dxskininfo--setboneinfluence.md)                         | Legt den Wert für den Einfluss für einen Knochen Wert fest.<br/>                                                                                                                                                |
| [**Setbonename**](id3dxskininfo--setbonename.md)                                   | Legt den Namen des Knochens fest.<br/>                                                                                                                                                                 |
| [**Setboneoffsetmatrix**](id3dxskininfo--setboneoffsetmatrix.md)                   | Legt die markveroffsetmatrix fest.<br/>                                                                                                                                                        |
| [**Setbonevertexinfluence**](id3dxskininfo--setbonevertexinfluence.md)             | Legt einen Einfluss Wert eines Knotens in einem einzelnen Scheitelpunkt fest.<br/>                                                                                                                               |
| [**Setdeclaration**](id3dxskininfo--setdeclaration.md)                             | Legt die Scheitelpunkt Deklaration fest.<br/>                                                                                                                                                        |
| [**Setf-VF**](id3dxskininfo--setfvf.md)                                             | Legt den Typ des flexiblen Vertex-Formats (FVF) fest.<br/>                                                                                                                                         |
| [**Setminboneingefluence**](id3dxskininfo--setminboneinfluence.md)                   | Legt den minimalen Knochen Einfluss fest. Werte, die kleiner als dieser Wert sind, werden ignoriert.<br/>                                                                                                    |
| [**Updateskinnedmesh**](id3dxskininfo--updateskinnedmesh.md)                       | Wendet das softwareskinning auf die Ziel Vertices basierend auf den aktuellen Matrizen an.<br/>                                                                                                     |



 

## <a name="remarks"></a>Bemerkungen

Erstellen Sie eine **ID3DXSkinInfo** -Schnittstelle mit [**D3DXCreateSkinInfo**](d3dxcreateskininfo.md), [**D3DXCreateSkinInfoFromBlendedMesh**](d3dxcreateskininfofromblendedmesh.md)oder [**D3DXCreateSkinInfoFVF**](d3dxcreateskininfofvf.md).

Der LPD3DXSKININFO-Typ wird als Zeiger auf die **ID3DXSkinInfo** -Schnittstelle definiert.


```
typedef struct ID3DXSkinInfo *LPD3DXSKININFO;
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

 

 
