---
description: Anwendungen verwenden die Methoden der ID3DXMesh-Schnittstelle zum Bearbeiten von Mesh-Objekten.
ms.assetid: f571fe0b-3f0c-43c9-809c-d1e14f85b720
title: ID3DXMesh-Schnittstelle (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9c2a677edba4bad5e908b6dd69aa21a467b2a245
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355716"
---
# <a name="id3dxmesh-interface"></a>ID3DXMesh-Schnittstelle

Anwendungen verwenden die Methoden der ID3DXMesh-Schnittstelle zum Bearbeiten von Mesh-Objekten.

## <a name="members"></a>Member

Die **ID3DXMesh** -Schnittstelle erbt von [**ID3DXBaseMesh**](id3dxbasemesh.md). **ID3DXMesh** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DXMesh** -Schnittstelle verfügt über diese Methoden.



| Methode                                                            | BESCHREIBUNG                                                                                                                            |
|:------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------|
| [**LockAttributeBuffer**](id3dxmesh--lockattributebuffer.md)     | Sperrt den Gitter Puffer, der die Daten des Mesh-Attributs enthält, und gibt einen Zeiger darauf zurück.<br/>                                   |
| [**Optimieren**](id3dxmesh--optimize.md)                           | Generiert ein neues Mesh mit neu bestellten Gesichtern und Scheitel Punkten, um die Zeichnungs Leistung zu optimieren.<br/>                                     |
| [**Optimizanplace**](id3dxmesh--optimizeinplace.md)             | Generiert ein Mesh mit neu bestellten Gesichtern und Scheitel Punkten, um die Zeichnungs Leistung zu optimieren. Diese Methode ordnet das vorhandene Mesh neu an.<br/> |
| [**""-Tributetable "**](id3dxmesh--setattributetable.md)         | Legt die Attribut Tabelle für ein Mesh und die Anzahl der in der Tabelle gespeicherten Einträge fest.<br/>                                          |
| [**UnlockAttributeBuffer**](id3dxmesh--unlockattributebuffer.md) | Entsperrt einen Attribut Puffer.<br/>                                                                                                |



 

## <a name="remarks"></a>Bemerkungen

Rufen Sie zum Abrufen der **ID3DXMesh** -Schnittstelle entweder die [**D3DXCreateMesh**](d3dxcreatemesh.md) -oder die [**D3DXCreateMeshFVF**](d3dxcreatemeshfvf.md) -Funktion auf.

Diese Schnittstelle erbt zusätzliche Funktionen von der [**ID3DXBaseMesh**](id3dxbasemesh.md) -Schnittstelle.

Der LPD3DXMESH-Typ wird als Zeiger auf die **ID3DXMesh** -Schnittstelle definiert.


```
typedef struct ID3DXMesh *LPD3DXMESH;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ID3DXBaseMesh**](id3dxbasemesh.md)
</dt> <dt>

[D3DX-Schnittstellen](dx9-graphics-reference-d3dx-interfaces.md)
</dt> <dt>

[Mesh-Funktionen](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 




