---
description: Anwendungen verwenden die Methoden der ID3DX10Mesh-Schnittstelle zum Bearbeiten von Mesh-Objekten.
ms.assetid: 1734b8fd-e1a6-4aa4-96a0-8693019a9dac
title: ID3DX10Mesh-Schnittstelle (d3dx10. h)
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
ms.openlocfilehash: 2ddf0876928f85debded1645b9a22de790917017
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106371953"
---
# <a name="id3dx10mesh-interface"></a>ID3DX10Mesh-Schnittstelle

Anwendungen verwenden die Methoden der ID3DX10Mesh-Schnittstelle zum Bearbeiten von Mesh-Objekten.

## <a name="members"></a>Member

Die **ID3DX10Mesh** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **ID3DX10Mesh** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DX10Mesh** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                                   | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                          |
|:-----------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Clonemesh**](id3dx10mesh-clonemesh.md)                                               | Erstellt ein neues Mesh und füllt es mit den Daten eines zuvor geladenen Mesh.<br/>                                                                                                                                                                                                                                                |
| [**Commitgeräte**](id3dx10mesh-committodevice.md)                                     | Commit für alle an einem Mesh vorgenommenen Änderungen auf dem Gerät durchgeführt, sodass die Änderungen gerendert werden können. Dies sollte aufgerufen werden, nachdem die Daten eines Netzes geändert wurden und bevor es gerendert wird. Ein Mesh kann nur dann gerendert werden, wenn es auf dem Gerät ausgeführt wird. Siehe Bemerkungen.<br/>                                                                         |
| [**Verwerfen**](id3dx10mesh-discard.md)                                                   | Entfernt Mesh-Daten von dem Gerät, für das ein Commit an das Gerät ausgeführt wurde (mit [**ID3DX10Mesh:: commitcomdevice**](id3dx10mesh-committodevice.md)).<br/>                                                                                                                                                                         |
| [**DrawSubset**](id3dx10mesh-drawsubset.md)                                             | Zeichnet eine Teilmenge eines Mesh.<br/>                                                                                                                                                                                                                                                                                                 |
| [**Drawsub-tinstangeleitet**](id3dx10mesh-drawsubsetinstanced.md)                           | Zeichnen Sie mehrere Instanzen derselben Teilmenge eines Mesh.<br/>                                                                                                                                                                                                                                                                      |
| [**Generateanandarcyandpointreps**](id3dx10mesh-generateadjacencyandpointreps.md)       | Generieren Sie eine Liste mit Gitter Kanten sowie eine Liste der Flächen, die die einzelnen Kanten gemeinsam verwenden.<br/>                                                                                                                                                                                                                                           |
| [**Generateattributebufferfromtable**](id3dx10mesh-generateattributebufferfromtable.md) | Generieren Sie einen Attribut Puffer aus den Daten in der-Attribut Tabelle des Mesh. Ein Attribut Puffer ist ein anderes Format zum Speichern der Daten in der Attribut Tabelle. Der Attribut Puffer und die Attribut Tabelle sind interne Datenstrukturen im Mesh.<br/>                                                                  |
| [**Generategsadjacency**](id3dx10mesh-generategsadjacency.md)                           | Fügt dem Index Puffer des Netzes Informationen hinzu. Wenn das Mesh an einen Geometry-Shader gesendet werden soll, der die Daten aufnimmt, ist es erforderlich, dass der Index Puffer des Netzes Informationen zu den Daten enthält.<br/>                                                                                                                       |
| [**Getannäherendcybuffer**](id3dx10mesh-getadjacencybuffer.md)                             | Greifen Sie auf den zutreffungspuffer des Mesh zu.<br/>                                                                                                                                                                                                                                                                                       |
| [**Getattributebuffer**](id3dx10mesh-getattributebuffer.md)                             | Greifen Sie auf den-Attribut Puffer des Mesh zu.<br/>                                                                                                                                                                                                                                                                                       |
| [**GetAttributeTable**](id3dx10mesh-getattributetable.md)                               | Ruft entweder eine Attribut Tabelle für ein Mesh oder die Anzahl der in einer Attribut Tabelle gespeicherten Einträge für ein Mesh ab.<br/>                                                                                                                                                                                                         |
| [**Getbeviceingedexbuffer**](id3dx10mesh-getdeviceindexbuffer.md)                         | Greifen Sie auf den Index Puffer des Mesh zu, nachdem er mit [**ID3DX10Mesh:: committedevice**](id3dx10mesh-committodevice.md)an das Gerät übertragen wurde. Dies unterscheidet sich von [**ID3DX10Mesh:: getindexbuffer**](id3dx10mesh-getindexbuffer.md), das den Index Puffer zurückgibt, bevor er an das Gerät übertragen wurde.<br/>     |
| [**Getdebug-texbuffer**](id3dx10mesh-getdevicevertexbuffer.md)                       | Greifen Sie auf den Vertex-Puffer des Mesh zu, nachdem er mit [**ID3DX10Mesh:: committedevice**](id3dx10mesh-committodevice.md)an das Gerät übertragen wurde. Dies unterscheidet sich von [**ID3DX10Mesh:: getvertexbuffer**](id3dx10mesh-getvertexbuffer.md), das den Vertex-Puffer zurückgibt, bevor er an das Gerät übertragen wurde.<br/> |
| [**Getfacecount**](id3dx10mesh-getfacecount.md)                                         | Ruft die Anzahl der Gesichter im Mesh ab.<br/>                                                                                                                                                                                                                                                                                |
| [**GetFlags**](id3dx10mesh-getflags.md)                                                 | Greifen Sie auf die erstellungsflags des Netzes zu.<br/>                                                                                                                                                                                                                                                                                         |
| [**Getindexbuffer**](id3dx10mesh-getindexbuffer.md)                                     | Ruft die Daten in einem Index Puffer ab.<br/>                                                                                                                                                                                                                                                                                    |
| [**Getpointrepbuffer**](id3dx10mesh-getpointrepbuffer.md)                               | Gibt den Punkt Rep-Puffer des Netzes an.<br/>                                                                                                                                                                                                                                                                                          |
| [**Getvertexbuffer**](id3dx10mesh-getvertexbuffer.md)                                   | Ruft den dem Mesh zugeordneten Vertex-Puffer ab.<br/>                                                                                                                                                                                                                                                                     |
| [**Getvertexbuffercount**](id3dx10mesh-getvertexbuffercount.md)                         | Die Anzahl der Vertex-Puffer im Mesh.<br/>                                                                                                                                                                                                                                                                             |
| [**Getvertexcount**](id3dx10mesh-getvertexcount.md)                                     | Die Anzahl der Scheitel Punkte im Mesh. Ein Mesh kann mehrere Scheitelpunkt Puffer enthalten (d. h., ein Vertex-Puffer enthält möglicherweise alle Positionsdaten, eine andere enthält möglicherweise alle Texturkoordinaten Daten usw.), aber jeder Scheitelpunkt Puffer enthält die gleiche Anzahl von Elementen.<br/>                                                   |
| [**Getvertexdescription**](id3dx10mesh-getvertexdescription.md)                         | Zugreifen auf die vertexbeschreibung, die an [**D3DX10CreateMesh**](d3d10-d3dx10createmesh.md)übermittelt wurde. In der Scheitelpunkt Beschreibung wird das Layout der Vertex-Puffer des Netzes beschrieben.<br/>                                                                                                                                                   |
| [**Intersect**](id3dx10mesh-intersect.md)                                               | Bestimmt, ob sich ein Strahl mit diesem Mesh schneidet.<br/>                                                                                                                                                                                                                                                                            |
| [**Intersectsubset**](id3dx10mesh-intersectsubset.md)                                   | Bestimmt, ob sich ein Strahl mit einer Teilmenge dieses Netzes schneidet.<br/>                                                                                                                                                                                                                                                                |
| [**Optimieren**](id3dx10mesh-optimize.md)                                                 | Generiert ein neues Mesh mit neu bestellten Gesichtern und Scheitel Punkten, um die Zeichnungs Leistung zu optimieren.<br/>                                                                                                                                                                                                                                   |
| [**"".**](id3dx10mesh-setadjacencydata.md)                                 | Legen Sie die Daten des Mesh fest.<br/>                                                                                                                                                                                                                                                                                            |
| [**"" "".**](id3dx10mesh-setattributedata.md)                                 | Legen Sie die Attributdaten des Mesh fest.<br/>                                                                                                                                                                                                                                                                                            |
| [**""-Tributetable "**](id3dx10mesh-setattributetable.md)                               | Legt die Attribut Tabelle für ein Mesh und die Anzahl der in der Tabelle gespeicherten Einträge fest.<br/>                                                                                                                                                                                                                                        |
| [**Setindexdata**](id3dx10mesh-setindexdata.md)                                         | Legen Sie die Indexdaten des Netzes fest.<br/>                                                                                                                                                                                                                                                                                                |
| [**Setpointrepdata**](id3dx10mesh-setpointrepdata.md)                                   | Legen Sie die Punkt-Rep-Daten für das Mesh fest.<br/>                                                                                                                                                                                                                                                                                      |
| [**Setvertexdata**](id3dx10mesh-setvertexdata.md)                                       | Legen Sie Scheitelpunkt Daten auf einen der Vertex-Puffer des Netzes fest.<br/>                                                                                                                                                                                                                                                                    |



 

## <a name="remarks"></a>Bemerkungen

Rufen Sie zum Abrufen der ID3DX10Mesh-Schnittstelle [**D3DX10CreateMesh**](d3d10-d3dx10createmesh.md)auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx10. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3dx10. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Schnittstellen](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
