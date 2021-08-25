---
description: Diese Schnittstelle kapselt patch mesh-Funktionen.
ms.assetid: c70c0fe0-b695-4ad9-b0c6-7854cf8f7593
title: ID3DXPatchMesh-Schnittstelle (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 44899ccee6f13aa25b01e284df5a892196d657610c3f89d546fc0b646eeaa069
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119856280"
---
# <a name="id3dxpatchmesh-interface"></a>ID3DXPatchMesh-Schnittstelle

Diese Schnittstelle kapselt patch mesh-Funktionen.

## <a name="members"></a>Member

Die **ID3DXPatchMesh-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ID3DXPatchMesh** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DXPatchMesh-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                           | Beschreibung                                                                                     |
|:---------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [**CloneMesh**](id3dxpatchmesh--clonemesh.md)                                   | Erstellt ein neues Patchnetz mit der angegebenen Scheitelpunktdeklaration.<br/>                      |
| [**GenerateAdencyency**](id3dxpatchmesh--generateadjacency.md)                   | Generieren Sie eine Liste der Gitternetzränder und der Patches, die die einzelnen Kanten gemeinsam nutzen.<br/>                  |
| [**GetControlVerticesPerPatch**](id3dxpatchmesh--getcontrolverticesperpatch.md) | Ruft die Anzahl der Steuerpunkte pro Patch ab.<br/>                                       |
| [**GetDeclaration**](id3dxpatchmesh--getdeclaration.md)                         | Ruft die Scheitelpunktdeklaration ab.<br/>                                                         |
| [**GetDevice**](id3dxpatchmesh--getdevice.md)                                   | Ruft das Gerät ab, das das Gitternetz erstellt hat.<br/>                                               |
| [**GetDisplaceParam**](id3dxpatchmesh--getdisplaceparam.md)                     | Ruft Gittergeometrie-Verschiebungsparameter ab.<br/>                                          |
| [**GetIndexBuffer**](id3dxpatchmesh--getindexbuffer.md)                         | Ruft den Meshindexpuffer ab.<br/>                                                          |
| [**GetNumPatches**](id3dxpatchmesh--getnumpatches.md)                           | Ruft die Anzahl der Patches im Gitternetz ab.<br/>                                              |
| [**GetNumVertices**](id3dxpatchmesh--getnumvertices.md)                         | Ruft die Anzahl der Scheitelpunkte im Gitternetz ab.<br/>                                             |
| [**GetOptions**](id3dxpatchmesh--getoptions.md)                                 | Ruft den Typ des Patches ab.<br/>                                                              |
| [**GetPatchInfo**](id3dxpatchmesh--getpatchinfo.md)                             | Ruft die Attribute des Patches ab.<br/>                                                    |
| [**GetTessSize**](id3dxpatchmesh--gettesssize.md)                               | Ruft die Größe des Mosaikgitters ab, wenn ein Mosaikgrad angegeben ist.<br/>                   |
| [**GetVertexBuffer**](id3dxpatchmesh--getvertexbuffer.md)                       | Ruft den Vertexpuffer für das Gitternetz ab.<br/>                                                         |
| [**LockAttributeBuffer**](id3dxpatchmesh--lockattributebuffer.md)               | Sperrt den Attributpuffer.<br/>                                                          |
| [**LockIndexBuffer**](id3dxpatchmesh--lockindexbuffer.md)                       | Sperren Sie den Indexpuffer.<br/>                                                               |
| [**LockVertexBuffer**](id3dxpatchmesh--lockvertexbuffer.md)                     | Sperren Sie den Scheitelpunktpuffer.<br/>                                                              |
| [**Optimieren**](id3dxpatchmesh--optimize.md)                                     | Optimiert das Patchnetz für eine effiziente Mosaikierung.<br/>                                 |
| [**SetDisplaceParam**](id3dxpatchmesh--setdisplaceparam.md)                     | Legt Gittergeometrieverschiebungsparameter fest.<br/>                                          |
| [**Mosaik**](id3dxpatchmesh--tessellate.md)                                 | Führt ein einheitliches Mosaik basierend auf der Mosaikebene aus.<br/>                       |
| [**TessellateAdaptive**](id3dxpatchmesh--tessellateadaptive.md)                 | Führt ein adaptives Mosaik basierend auf dem z-basierten Kriterium für das adaptive Mosaik aus.<br/> |
| [**UnlockAttributeBuffer**](id3dxpatchmesh--unlockattributebuffer.md)           | Entsperren Sie den Attributpuffer.<br/>                                                         |
| [**UnlockIndexBuffer**](id3dxpatchmesh--unlockindexbuffer.md)                   | Entsperren Sie den Indexpuffer.<br/>                                                             |
| [**UnlockVertexBuffer**](id3dxpatchmesh--unlockvertexbuffer.md)                 | Entsperren Sie den Scheitelpunktpuffer.<br/>                                                            |



 

## <a name="remarks"></a>Hinweise

Ein Patchnetz ist ein Gitternetz, das aus einer Reihe von Patches besteht.

Rufen Sie die **D3DXCreatePatchMesh-Funktion** auf, um die [**ID3DXPatchMesh-Schnittstelle**](d3dxcreatepatchmesh.md) abzurufen.

Der LPD3DXPATCHMESH-Typ wird wie folgt als Zeiger auf die **ID3DXPatchMesh-Schnittstelle** definiert:


```
typedef struct ID3DXPatchMesh *LPD3DXPATCHMESH;
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

[Meshfunktionen](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
