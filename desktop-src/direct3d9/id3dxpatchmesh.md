---
description: Diese Schnittstelle kapselt die patchmesh-Funktionalität.
ms.assetid: c70c0fe0-b695-4ad9-b0c6-7854cf8f7593
title: ID3DXPatchMesh-Schnittstelle (D3DX9Mesh. h)
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
ms.openlocfilehash: f1f13e6abe3a164e8027ddcb6bb33e9f0ca618fb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355207"
---
# <a name="id3dxpatchmesh-interface"></a>ID3DXPatchMesh-Schnittstelle

Diese Schnittstelle kapselt die patchmesh-Funktionalität.

## <a name="members"></a>Member

Die **ID3DXPatchMesh** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **ID3DXPatchMesh** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DXPatchMesh** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                           | BESCHREIBUNG                                                                                     |
|:---------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [**Clonemesh**](id3dxpatchmesh--clonemesh.md)                                   | Erstellt ein neues patchmesh mit der angegebenen Scheitelpunkt Deklaration.<br/>                      |
| [**Generateency**](id3dxpatchmesh--generateadjacency.md)                   | Generiert eine Liste der Gitter Kanten und der Patches, die die einzelnen Kanten gemeinsam verwenden.<br/>                  |
| [**Getcontrolverticesperpatch**](id3dxpatchmesh--getcontrolverticesperpatch.md) | Ruft die Anzahl der Steuerelement Vertices pro Patch ab.<br/>                                       |
| [**GetDeclaration**](id3dxpatchmesh--getdeclaration.md)                         | Ruft die Vertex-Deklaration ab.<br/>                                                         |
| [**GetDevice**](id3dxpatchmesh--getdevice.md)                                   | Ruft das Gerät ab, das das Mesh erstellt hat.<br/>                                               |
| [**Getverdräneparam**](id3dxpatchmesh--getdisplaceparam.md)                     | Ruft Mesh-Geometrie-Verschiebungs Parameter ab.<br/>                                          |
| [**Getindexbuffer**](id3dxpatchmesh--getindexbuffer.md)                         | Ruft den Mesh-Index Puffer ab.<br/>                                                          |
| [**Getnumpatches**](id3dxpatchmesh--getnumpatches.md)                           | Ruft die Anzahl der Patches im Mesh ab.<br/>                                              |
| [**Getnumvertices**](id3dxpatchmesh--getnumvertices.md)                         | Ruft die Anzahl der Scheitel Punkte im Mesh ab.<br/>                                             |
| [**GetOptions**](id3dxpatchmesh--getoptions.md)                                 | Ruft den Typ des Patches ab.<br/>                                                              |
| [**Getpatchinfo**](id3dxpatchmesh--getpatchinfo.md)                             | Ruft die Attribute des Patches ab.<br/>                                                    |
| [**Gettesssize**](id3dxpatchmesh--gettesssize.md)                               | Ruft die Größe des Mosaik Netzes ab, wenn eine Mosaik Ebene angegeben ist.<br/>                   |
| [**Getvertexbuffer**](id3dxpatchmesh--getvertexbuffer.md)                       | Ruft den mesvertexpuffer ab.<br/>                                                         |
| [**LockAttributeBuffer**](id3dxpatchmesh--lockattributebuffer.md)               | Sperrt den Attribut Puffer.<br/>                                                          |
| [**LockIndexBuffer**](id3dxpatchmesh--lockindexbuffer.md)                       | Sperren Sie den Index Puffer.<br/>                                                               |
| [**Lockvertexbuffer**](id3dxpatchmesh--lockvertexbuffer.md)                     | Sperren Sie den Scheitelpunkt Puffer.<br/>                                                              |
| [**Optimieren**](id3dxpatchmesh--optimize.md)                                     | Optimiert das patchemesh für effizientes Mosaik.<br/>                                 |
| [**Setverdräneparam**](id3dxpatchmesh--setdisplaceparam.md)                     | Legt Mesh-Geometrie-Verschiebungs Parameter fest.<br/>                                          |
| [**& Nbsp;**](id3dxpatchmesh--tessellate.md)                                 | Führt ein einheitliches Mosaik basierend auf der Mosaik Ebene aus.<br/>                       |
| [**Tbitellateadaptive**](id3dxpatchmesh--tessellateadaptive.md)                 | Führt ein adaptives Mosaik basierend auf dem z-basierten adaptiven Mosaik Kriterium aus.<br/> |
| [**UnlockAttributeBuffer**](id3dxpatchmesh--unlockattributebuffer.md)           | Entsperren Sie den Attribut Puffer.<br/>                                                         |
| [**Unlockindexbuffer**](id3dxpatchmesh--unlockindexbuffer.md)                   | Entsperren Sie den Index Puffer.<br/>                                                             |
| [**Unlockvertexbuffer**](id3dxpatchmesh--unlockvertexbuffer.md)                 | Entsperren Sie den Vertex-Puffer.<br/>                                                            |



 

## <a name="remarks"></a>Bemerkungen

Ein patchmesh ist ein Mesh, das aus einer Reihe von Patches besteht.

Rufen Sie zum Abrufen der **ID3DXPatchMesh** -Schnittstelle die [**D3DXCreatePatchMesh**](d3dxcreatepatchmesh.md) -Funktion auf.

Der LPD3DXPATCHMESH-Typ wird wie folgt als Zeiger auf die **ID3DXPatchMesh** -Schnittstelle definiert:


```
typedef struct ID3DXPatchMesh *LPD3DXPATCHMESH;
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

[Mesh-Funktionen](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
