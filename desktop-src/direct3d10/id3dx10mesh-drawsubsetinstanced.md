---
description: Zeichnen Sie mehrere Instanzen derselben Teilmenge eines Mesh.
ms.assetid: 2a17ecdb-c6f3-401c-b7ed-8a42fe159de0
title: ID3DX10Mesh::D rawsubsegtinstanzierte-Methode (d3dx10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.DrawSubsetInstanced
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 314f85d896be629254def560e55ce6a05bfe1fbd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353385"
---
# <a name="id3dx10meshdrawsubsetinstanced-method"></a>ID3DX10Mesh::D rawsubsegtinstanzierte-Methode

Zeichnen Sie mehrere Instanzen derselben Teilmenge eines Mesh.

## <a name="syntax"></a>Syntax


```C++
HRESULT DrawSubsetInstanced(
  [in] UINT AttribId,
  [in] UINT InstanceCount,
  [in] UINT StartInstanceLocation
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Atungbid* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Gibt an, welche Teilmenge des Mesh gezeichnet werden soll. Dieser Wert wird verwendet, um Gesichter in einem Mesh als zu einer oder mehreren Attribut Gruppen gehörenden zu unterscheiden. Siehe Bemerkungen.

</dd> <dt>

*InstanceCount* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Anzahl der zu Rendering enden Instanzen.

</dd> <dt>

*Startinstancelokation* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Die Instanz, aus der in jedem als Instanzdaten markierten Puffer abgerufen werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist einer der Werte, die in [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)aufgelistet sind.

## <a name="remarks"></a>Bemerkungen

Ein Mesh enthält eine Attribut Tabelle. In der Attribut Tabelle kann ein Mesh in Teilmengen aufgeteilt werden, wobei jede Teilmenge mit einer Attribut-ID identifiziert wird. Beispielsweise kann ein Mesh mit 200-Gesichtern, das in drei Teilmengen unterteilt ist, eine Attribut Tabelle aufweisen, die wie folgt aussieht:



|            |                 |
|------------|-----------------|
| Atungbid 0 | Gesichter 0 ~ 50    |
| Atungbid 1 | Gesichter 51 ~ 125  |
| Atungbid 2 | Gesichter 126 ~ 200 |



 

Durch die Instanziierung kann die Leistung durch Wiederverwendung derselben Geometrie erweitert werden, um mehrere Objekte in einer Szene zu zeichnen. Ein Beispiel für eine Instanziierung könnte darin bestehen, das gleiche Objekt mit unterschiedlichen Positionen und Farben zu zeichnen. Die Indizierung erfordert mehrere Vertex-Puffer: mindestens eine für pro-Vertex-Daten und einen zweiten Puffer für Instanzdaten.

Das Zeichnen von Instanzen mit drawsubmentinstancing ähnelt dem Prozess, der mit [**ID3D10Device verwendet wird::D rawindexedinstancing**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-drawindexedinstanced) , der unter [Instancing Sample (instanziierungsbeispiel](https://msdn.microsoft.com/library/Ee418269(v=VS.85).aspx)) beschrieben wird. Der Hauptunterschied bei der Verwendung von drawsubsetinstancing besteht darin, dass Vertex-und Index Puffer aus dem [**ID3DX10Mesh-Schnittstellen**](id3dx10mesh.md) Objekt extrahiert werden müssen, bevor die Instanziierungsdaten kombiniert werden können.

Der folgende Code veranschaulicht das Extrahieren der Scheitelpunkt-und Index Puffer aus dem Mesh-Objekt.


```
      ID3D10Buffer* vertexBuffer;
      pDeviceObj->pMesh->GetDeviceVertexBuffer(0, &vertexBuffer);
      ID3D10Buffer* indexBuffer;
      pDeviceObj->pMesh->GetDeviceIndexBuffer(&indexBuffer);
      
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx10. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3dx10. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[D3DX-Schnittstellen](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
