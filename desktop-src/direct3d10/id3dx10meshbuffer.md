---
description: Ein Gitternetzpuffer ist ein Puffer, der Daten zu einem Gitternetz enthält.
ms.assetid: a9fdfa22-531d-4da0-89f0-8766c2635e20
title: ID3DX10MeshBuffer-Schnittstelle (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10MeshBuffer
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: a2aeabcd6dd3cc711636d0e275f76ab48537953671559e244cf341e270783fb8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118540154"
---
# <a name="id3dx10meshbuffer-interface"></a>ID3DX10MeshBuffer-Schnittstelle

Ein Gitternetzpuffer ist ein Puffer, der Daten zu einem Gitternetz enthält. Sie kann einen von fünf verschiedenen Datentypen enthalten: Scheitelpunktdaten, Indexdaten, Adjacency-Daten, Attributdaten oder Punkt-Rep-Daten. Die -Struktur wird für den Zugriff auf diese fünf Datenteile über die folgenden fünf APIs verwendet: [**ID3DX10Mesh::GetVertexBuffer,**](id3dx10mesh-getvertexbuffer.md) [**ID3DX10Mesh::GetIndexBuffer,**](id3dx10mesh-getindexbuffer.md) [**ID3DX10Mesh::GetAdjacencyBuffer,**](id3dx10mesh-getadjacencybuffer.md) [**ID3DX10Mesh::GetAttributeBuffer**](id3dx10mesh-getattributebuffer.md)oder [**ID3DX10Mesh::GetPointRepBuffer**](id3dx10mesh-getpointrepbuffer.md).

## <a name="members"></a>Member

Die **ID3DX10MeshBuffer-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ID3DX10MeshBuffer verfügt** auch über diese Membertypen:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DX10MeshBuffer-Schnittstelle** verfügt über diese Methoden.



| Methode                                       | BESCHREIBUNG                                                                |
|:---------------------------------------------|:---------------------------------------------------------------------------|
| [**GetSize**](id3dx10meshbuffer-getsize.md) | Gibt die Größe des Gitternetzpuffers in Bytes an.<br/>                      |
| [**Zuordnung**](id3dx10meshbuffer-map.md)         | Sie erhalten einen Zeiger auf den Gitternetzpufferspeicher, um dessen Inhalt zu ändern.<br/> |
| [**Unmap**](id3dx10meshbuffer-unmap.md)     | Entzuordnung eines Puffers.<br/>                                                 |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[D3DX-Schnittstellen](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
