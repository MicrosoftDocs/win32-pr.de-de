---
description: Ein Gitter Puffer ist ein Puffer, der Daten zu einem Mesh enthält.
ms.assetid: a9fdfa22-531d-4da0-89f0-8766c2635e20
title: ID3DX10MeshBuffer-Schnittstelle (d3dx10. h)
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
ms.openlocfilehash: 42076393c3be5443688ec4db954131935b62f696
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106366644"
---
# <a name="id3dx10meshbuffer-interface"></a>ID3DX10MeshBuffer-Schnittstelle

Ein Gitter Puffer ist ein Puffer, der Daten zu einem Mesh enthält. Sie kann einen von fünf verschiedenen Datentypen enthalten: Vertex-Daten, Indexdaten, Daten der Daten, Attributdaten oder Punkt-Rep-Daten. Die-Struktur wird für den Zugriff auf diese fünf Datenelemente über die folgenden fünf APIs verwendet: [**ID3DX10Mesh:: getvertexbuffer**](id3dx10mesh-getvertexbuffer.md), [**ID3DX10Mesh:: getindexbuffer**](id3dx10mesh-getindexbuffer.md), [**ID3DX10Mesh:: gettribuencybuffer**](id3dx10mesh-getadjacencybuffer.md), [**ID3DX10Mesh:: getattributebuffer**](id3dx10mesh-getattributebuffer.md)oder [**ID3DX10Mesh:: getpointrepbuffer**](id3dx10mesh-getpointrepbuffer.md).

## <a name="members"></a>Member

Die **ID3DX10MeshBuffer** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **ID3DX10MeshBuffer** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DX10MeshBuffer** -Schnittstelle verfügt über diese Methoden.



| Methode                                       | BESCHREIBUNG                                                                |
|:---------------------------------------------|:---------------------------------------------------------------------------|
| [**GetSize**](id3dx10meshbuffer-getsize.md) | Gibt die Größe des Gitter Puffers in Bytes an.<br/>                      |
| [**Bilden**](id3dx10meshbuffer-map.md)         | Einen Zeiger auf den Arbeitsspeicher des Mesh-Puffers, um seinen Inhalt zu ändern.<br/> |
| [**Unmap**](id3dx10meshbuffer-unmap.md)     | Aufheben der Zuordnung eines Puffers.<br/>                                                 |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx10. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3dx10. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Schnittstellen](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
