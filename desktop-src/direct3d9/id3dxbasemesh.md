---
description: Anwendungen verwenden die Methoden der ID3DXBaseMesh-Schnittstelle, um Mesh-und Progressive Mesh-Objekte zu bearbeiten und abzufragen.
ms.assetid: ec4ccd77-e370-470c-9325-3d794a8f7f16
title: ID3DXBaseMesh-Schnittstelle (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 58029639852b30f5de357bb2643583615c45485c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355027"
---
# <a name="id3dxbasemesh-interface"></a>ID3DXBaseMesh-Schnittstelle

Anwendungen verwenden die Methoden der **ID3DXBaseMesh** -Schnittstelle, um Mesh-und Progressive Mesh-Objekte zu bearbeiten und abzufragen.

## <a name="members"></a>Member

Die **ID3DXBaseMesh** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **ID3DXBaseMesh** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DXBaseMesh** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                            | BESCHREIBUNG                                                                                                                                                                                                           |
|:----------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Clonemesh**](id3dxbasemesh--clonemesh.md)                                     | Klont ein Mesh mit einem Deklarator.<br/>                                                                                                                                                                          |
| [**Clonemeshf VF**](id3dxbasemesh--clonemeshfvf.md)                               | Klont ein Mesh mit einem flexiblen Scheitelpunkt Formatierungs Code (FVF).<br/>                                                                                                                                                   |
| [**Convertadjackocytopointreps**](id3dxbasemesh--convertadjacencytopointreps.md) | Konvertiert Gitter Informations Informationen in ein Array von Punkt Vertretern.<br/>                                                                                                                                  |
| [**Convertpointrepstoannäherency**](id3dxbasemesh--convertpointrepstoadjacency.md) | Konvertiert Punkt repräsentative Daten in Gitter Informations Informationen.<br/>                                                                                                                                          |
| [**DrawSubset**](id3dxbasemesh--drawsubset.md)                                   | Zeichnet eine Teilmenge eines Mesh.<br/>                                                                                                                                                                                  |
| [**Generateency**](id3dxbasemesh--generateadjacency.md)                     | Generieren Sie eine Liste mit Gitter Kanten sowie eine Liste der Flächen, die die einzelnen Kanten gemeinsam verwenden.<br/>                                                                                                                            |
| [**GetAttributeTable**](id3dxbasemesh--getattributetable.md)                     | Ruft entweder eine Attribut Tabelle für ein Mesh oder die Anzahl der in einer Attribut Tabelle gespeicherten Einträge für ein Mesh ab.<br/>                                                                                          |
| [**GetDeclaration**](id3dxbasemesh--getdeclaration.md)                           | Ruft eine Deklaration ab, die die Scheitel Punkte im Mesh beschreibt.<br/>                                                                                                                                               |
| [**GetDevice**](id3dxbasemesh--getdevice.md)                                     | Ruft das dem Mesh zugeordnete Gerät ab.<br/>                                                                                                                                                             |
| [**Getf VF**](id3dxbasemesh--getfvf.md)                                           | Ruft den Scheitelpunkt Wert fester Funktion ab.<br/>                                                                                                                                                                      |
| [**Getindexbuffer**](id3dxbasemesh--getindexbuffer.md)                           | Ruft die Daten in einem Index Puffer ab.<br/>                                                                                                                                                                     |
| [**Getnumbytespervertex**](id3dxbasemesh--getnumbytespervertex.md)               | Ruft die Anzahl der Bytes pro Scheitelpunkt ab.<br/>                                                                                                                                                                       |
| [**Getnumgesichter**](id3dxbasemesh--getnumfaces.md)                                 | Ruft die Anzahl der Gesichter im Mesh ab.<br/>                                                                                                                                                                 |
| [**Getnumvertices**](id3dxbasemesh--getnumvertices.md)                           | Ruft die Anzahl der Scheitel Punkte im Mesh ab.<br/>                                                                                                                                                              |
| [**GetOptions**](id3dxbasemesh--getoptions.md)                                   | Ruft die Gitter Optionen ab, die für dieses Mesh zum Zeitpunkt der Erstellung aktiviert sind.<br/>                                                                                                                                         |
| [**Getvertexbuffer**](id3dxbasemesh--getvertexbuffer.md)                         | Ruft den dem Mesh zugeordneten Vertex-Puffer ab.<br/>                                                                                                                                                      |
| [**LockIndexBuffer**](id3dxbasemesh--lockindexbuffer.md)                         | Sperrt einen Index Puffer und erhält einen Zeiger auf den Speicher des Index Puffers.<br/>                                                                                                                                    |
| [**Lockvertexbuffer**](id3dxbasemesh--lockvertexbuffer.md)                       | Sperrt einen Scheitelpunkt Puffer und erhält einen Zeiger auf den Vertex-Pufferspeicher.<br/>                                                                                                                                   |
| [**Unlockindexbuffer**](id3dxbasemesh--unlockindexbuffer.md)                     | Entsperrt einen Index Puffer.<br/>                                                                                                                                                                                   |
| [**Unlockvertexbuffer**](id3dxbasemesh--unlockvertexbuffer.md)                   | Entsperrt einen Scheitelpunkt Puffer.<br/>                                                                                                                                                                                   |
| [**Updatesemantics**](id3dxbasemesh--updatesemantics.md)                         | Mit dieser Methode kann der Benutzer die Mesh-Deklaration ändern, ohne das Datenlayout des Vertexpuffers zu ändern. Der-Rückruf ist nur gültig, wenn die alten und neuen Deklarations Formate die gleiche Scheitelpunkt Größe aufweisen.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Ein Mesh ist ein Objekt, das aus einem Satz von polygonalen Flächen besteht. Ein Mesh definiert einen Satz von Scheitel Punkten und eine Gruppe von Gesichtern (die Flächen werden in Bezug auf die Scheitel Punkte und die normale des Netzes definiert).

Der LPD3DXBASEMESH-Typ wird als Zeiger auf die **ID3DXBaseMesh** -Schnittstelle definiert.


```
typedef struct ID3DXBaseMesh *LPD3DXBASEMESH;
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

 

 
