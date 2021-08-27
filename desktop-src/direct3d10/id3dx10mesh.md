---
description: Anwendungen verwenden die Methoden der ID3DX10Mesh-Schnittstelle, um Gitternetzobjekte zu bearbeiten.
ms.assetid: 1734b8fd-e1a6-4aa4-96a0-8693019a9dac
title: ID3DX10Mesh-Schnittstelle (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 2506191db941eee0a046d52f64aaeeb0f642f11dd35e42d6b49c4b5f5f457d79
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096650"
---
# <a name="id3dx10mesh-interface"></a>ID3DX10Mesh-Schnittstelle

Anwendungen verwenden die Methoden der ID3DX10Mesh-Schnittstelle, um Gitternetzobjekte zu bearbeiten.

## <a name="members"></a>Member

Die **ID3DX10Mesh-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ID3DX10Mesh** verfügt auch über diese Membertypen:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DX10Mesh-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                                   | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                          |
|:-----------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CloneMesh**](id3dx10mesh-clonemesh.md)                                               | Erstellt ein neues Gitternetz und füllt es mit den Daten eines zuvor geladenen Gitters.<br/>                                                                                                                                                                                                                                                |
| [**CommitToDevice**](id3dx10mesh-committodevice.md)                                     | Übertragen Sie alle an einem Gitternetz vorgenommenen Änderungen an das Gerät, damit die Änderungen gerendert werden können. Diese sollte aufgerufen werden, nachdem die Daten eines Gitters geändert und bevor sie gerendert werden. Ein Gitternetz kann nur gerendert werden, wenn es an das Gerät übertragen wird. Siehe Bemerkungen.<br/>                                                                         |
| [**Verwerfen**](id3dx10mesh-discard.md)                                                   | Entfernt Netzdaten von dem Gerät, für das ein Commit auf das Gerät (mit [**ID3DX10Mesh::CommitToDevice) übertragen wurde.**](id3dx10mesh-committodevice.md)<br/>                                                                                                                                                                         |
| [**DrawSubset**](id3dx10mesh-drawsubset.md)                                             | Zeichnet eine Teilmenge eines Gitters.<br/>                                                                                                                                                                                                                                                                                                 |
| [**DrawSubsetInstanced**](id3dx10mesh-drawsubsetinstanced.md)                           | Zeichnen Sie mehrere Instanzen derselben Teilmenge eines Gitters.<br/>                                                                                                                                                                                                                                                                      |
| [**GenerateAdjacencyAndPointReps**](id3dx10mesh-generateadjacencyandpointreps.md)       | Generieren Sie eine Liste von Gitternetzrändern sowie eine Liste von Gesichtern, die die einzelnen Ränder gemeinsam haben.<br/>                                                                                                                                                                                                                                           |
| [**GenerateAttributeBufferFromTable**](id3dx10mesh-generateattributebufferfromtable.md) | Generieren Sie einen Attributpuffer aus den Daten in der Attributtabelle des Gitters. Ein Attributpuffer ist ein weiteres Format zum Speichern der Daten in der Attributtabelle. Sowohl der Attributpuffer als auch die Attributtabelle sind interne Datenstrukturen im Gitternetz.<br/>                                                                  |
| [**GenerateGSAdjacency**](id3dx10mesh-generategsadjacency.md)                           | Fügt dem Indexpuffer des Gitters Adjazienzdaten hinzu. Wenn das Gitternetz an einen Geometrie-Shader gesendet werden soll, der Adjacency-Daten übernimmt, muss der Indexpuffer des Gitters Adjazienzdaten enthalten.<br/>                                                                                                                       |
| [**GetAdjacencyBuffer**](id3dx10mesh-getadjacencybuffer.md)                             | Greifen Sie auf den Adjacency-Puffer des Gitters zu.<br/>                                                                                                                                                                                                                                                                                       |
| [**GetAttributeBuffer**](id3dx10mesh-getattributebuffer.md)                             | Greifen Sie auf den Attributpuffer des Gitters zu.<br/>                                                                                                                                                                                                                                                                                       |
| [**GetAttributeTable**](id3dx10mesh-getattributetable.md)                               | Ruft entweder eine Attributtabelle für ein Gitternetz oder die Anzahl von Einträgen ab, die in einer Attributtabelle für ein Gitternetz gespeichert sind.<br/>                                                                                                                                                                                                         |
| [**GetDeviceIndexBuffer**](id3dx10mesh-getdeviceindexbuffer.md)                         | Greifen Sie mit [**ID3DX10Mesh::CommitToDevice**](id3dx10mesh-committodevice.md)auf den Indexpuffer des Gitters zu, nachdem ein Commit auf das Gerät übertragen wurde. Dies ist ein anderer Wert als [**ID3DX10Mesh::GetIndexBuffer,**](id3dx10mesh-getindexbuffer.md)der den Indexpuffer zurückgibt, bevor er auf das Gerät übertragen wurde.<br/>     |
| [**GetDeviceVertexBuffer**](id3dx10mesh-getdevicevertexbuffer.md)                       | Greifen Sie mit [**ID3DX10Mesh::CommitToDevice**](id3dx10mesh-committodevice.md)auf den Scheitelpunktpuffer des Gitters zu, nachdem er auf das Gerät übertragen wurde. Dies ist ein anderer Wert als [**ID3DX10Mesh::GetVertexBuffer,**](id3dx10mesh-getvertexbuffer.md)der den Scheitelpunktpuffer zurückgibt, bevor er auf das Gerät übertragen wurde.<br/> |
| [**GetFaceCount**](id3dx10mesh-getfacecount.md)                                         | Ruft die Anzahl der Gesichter im Gitternetz ab.<br/>                                                                                                                                                                                                                                                                                |
| [**GetFlags**](id3dx10mesh-getflags.md)                                                 | Greifen Sie auf die Erstellungsflags des Gitters zu.<br/>                                                                                                                                                                                                                                                                                         |
| [**GetIndexBuffer**](id3dx10mesh-getindexbuffer.md)                                     | Ruft die Daten in einem Indexpuffer ab.<br/>                                                                                                                                                                                                                                                                                    |
| [**GetPointRepBuffer**](id3dx10mesh-getpointrepbuffer.md)                               | Hier erhalten Sie den Punkt-Rep-Puffer des Gitters.<br/>                                                                                                                                                                                                                                                                                          |
| [**GetVertexBuffer**](id3dx10mesh-getvertexbuffer.md)                                   | Ruft den Scheitelpunktpuffer ab, der dem Gitternetz zugeordnet ist.<br/>                                                                                                                                                                                                                                                                     |
| [**GetVertexBufferCount**](id3dx10mesh-getvertexbuffercount.md)                         | Gibt die Anzahl der Scheitelpunktpuffer im Gitternetz an.<br/>                                                                                                                                                                                                                                                                             |
| [**GetVertexCount**](id3dx10mesh-getvertexcount.md)                                     | Gibt die Anzahl der Scheitelzeichen im Gitternetz an. Ein Gitternetz kann mehrere Scheitelpunktpuffer enthalten (d. h., ein Scheitelpunktpuffer kann alle Positionsdaten enthalten, ein anderes kann alle Texturkoordinatendaten usw.) enthalten, aber jeder Scheitelpunktpuffer enthält die gleiche Anzahl von Elementen.<br/>                                                   |
| [**GetVertexDescription**](id3dx10mesh-getvertexdescription.md)                         | Greifen Sie auf die Scheitelpunktbeschreibung zu, die [**an D3DX10CreateMesh übergeben wird.**](d3d10-d3dx10createmesh.md) Die Scheitelpunktbeschreibung beschreibt das Layout der Scheitelpunktpuffer des Gitters.<br/>                                                                                                                                                   |
| [**Schneiden**](id3dx10mesh-intersect.md)                                               | Bestimmt, ob sich ein Strahl mit diesem Netz überschneidet.<br/>                                                                                                                                                                                                                                                                            |
| [**IntersectSubset**](id3dx10mesh-intersectsubset.md)                                   | Bestimmt, ob sich ein Strahl mit einer Teilmenge dieses Gitters überschneidet.<br/>                                                                                                                                                                                                                                                                |
| [**Optimieren**](id3dx10mesh-optimize.md)                                                 | Generiert ein neues Gitternetz mit neu angeordneten Gesichtern und Scheitelungen, um die Zeichnungsleistung zu optimieren.<br/>                                                                                                                                                                                                                                   |
| [**SetAdjacencyData**](id3dx10mesh-setadjacencydata.md)                                 | Legen Sie die Adjacency-Daten des Gitters fest.<br/>                                                                                                                                                                                                                                                                                            |
| [**SetAttributeData**](id3dx10mesh-setattributedata.md)                                 | Legen Sie die Attributdaten des Gitters fest.<br/>                                                                                                                                                                                                                                                                                            |
| [**SetAttributeTable**](id3dx10mesh-setattributetable.md)                               | Legt die Attributtabelle für ein Gitternetz und die Anzahl der in der Tabelle gespeicherten Einträge fest.<br/>                                                                                                                                                                                                                                        |
| [**SetIndexData**](id3dx10mesh-setindexdata.md)                                         | Legen Sie die Indexdaten des Gitters fest.<br/>                                                                                                                                                                                                                                                                                                |
| [**SetPointRepData**](id3dx10mesh-setpointrepdata.md)                                   | Legen Sie die Point Rep-Daten für das Gitternetz fest.<br/>                                                                                                                                                                                                                                                                                      |
| [**SetVertexData**](id3dx10mesh-setvertexdata.md)                                       | Legen Sie Scheitelpunktdaten in einen der Scheitelpunktpuffer des Gitters fest.<br/>                                                                                                                                                                                                                                                                    |



 

## <a name="remarks"></a>Hinweise

Rufen Sie zum Abrufen der ID3DX10Mesh-Schnittstelle [**D3DX10CreateMesh auf.**](d3d10-d3dx10createmesh.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Schnittstellen](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
