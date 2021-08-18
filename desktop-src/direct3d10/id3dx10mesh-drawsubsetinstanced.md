---
description: Zeichnen mehrerer Instanzen derselben Teilmenge eines Gitternetzes.
ms.assetid: 2a17ecdb-c6f3-401c-b7ed-8a42fe159de0
title: ID3DX10Mesh::D rawSubsetInstanced-Methode (D3DX10.h)
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
ms.openlocfilehash: 41da932b5f9445df83c0783b7788b8a7079af2acb74643ea37111d8482e8e208
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118990430"
---
# <a name="id3dx10meshdrawsubsetinstanced-method"></a>ID3DX10Mesh::D rawSubsetInstanced-Methode

Zeichnen mehrerer Instanzen derselben Teilmenge eines Gitternetzes.

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

*AttribId* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Gibt an, welche Teilmenge des Gitternetzes gezeichnet werden soll. Dieser Wert wird verwendet, um Gesichter in einem Gitternetz als zu einer oder mehreren Attributgruppen gehörend zu unterscheiden. Siehe Bemerkungen.

</dd> <dt>

*InstanceCount* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Anzahl der zu rendernden Instanzen.

</dd> <dt>

*StartInstanceLocation* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Welche Instanz aus in jedem Puffer abgerufen werden soll, der als Instanzdaten markiert ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist einer der In [Direct3D 10-Rückgabecodes aufgeführten](d3d10-graphics-reference-returnvalues.md)Werte.

## <a name="remarks"></a>Hinweise

Ein Gitternetz enthält eine Attributtabelle. Die Attributtabelle kann ein Gitternetz in Teilmengen unterteilen, wobei jede Teilmenge mit einer Attribut-ID identifiziert wird. Beispielsweise kann ein Gitternetz mit 200 Gesichtern, unterteilt in drei Teilmengen, eine Attributtabelle aufweisen, die wie folgt aussieht:



| Subset     | Gesichtserkennung           |
|------------|-----------------|
| AttribID 0 | Gesichter 0 ~ 50    |
| AttribID 1 | Gesichter 51 ~ 125  |
| AttribID 2 | Gesichter 126 ~ 200 |



 

Die Instanziierung kann die Leistung erweitern, indem dieselbe Geometrie wiederverwendet wird, um mehrere Objekte in einer Szene zu zeichnen. Ein Beispiel für die Instanziierung ist das Zeichnen desselben Objekts mit unterschiedlichen Positionen und Farben. Für die Indizierung sind mehrere Scheitelpunktpuffer erforderlich: mindestens einer für Daten pro Scheitelpunkt und ein zweiter Puffer für Daten pro Instanz.

Zeichnungsinstanzen mit DrawSubsetInstanced ähneln sehr dem Prozess, der mit [**ID3D10Device::D rawIndexedInstanced**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-drawindexedinstanced) verwendet wird, der im [Instanziierungsbeispiel](https://msdn.microsoft.com/library/Ee418269(v=VS.85).aspx)beschrieben ist. Der Hauptunterschied bei der Verwendung von DrawSubsetInstanced besteht darin, dass Scheitelpunkt- und Indexpuffer aus dem [**ID3DX10Mesh-Schnittstellenobjekt**](id3dx10mesh.md) extrahiert werden müssen, bevor die Instanziierungsdaten kombiniert werden können.

Der folgende Code veranschaulicht das Extrahieren der Scheitelpunkt- und Indexpuffer aus dem Gittermodellobjekt.


```
      ID3D10Buffer* vertexBuffer;
      pDeviceObj->pMesh->GetDeviceVertexBuffer(0, &vertexBuffer);
      ID3D10Buffer* indexBuffer;
      pDeviceObj->pMesh->GetDeviceIndexBuffer(&indexBuffer);
      
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[D3DX-Schnittstellen](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
