---
description: Legen Sie die Adjacency-Daten des Gitters fest.
ms.assetid: 67d51ce0-7fe2-484d-9874-f1fa59632d59
title: ID3DX10Mesh::SetAdjacencyData-Methode (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.SetAdjacencyData
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 8e183fb6fad07b92d8bca15654456ca1d31a11839af033222803044f8207a14f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118990380"
---
# <a name="id3dx10meshsetadjacencydata-method"></a>ID3DX10Mesh::SetAdjacencyData-Methode

Legen Sie die Adjacency-Daten des Gitters fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetAdjacencyData(
  [in] const UINT *pAdjacency
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pAdjacency* \[ In\]
</dt> <dd>

Typ: **const [**UINT**](../winprog/windows-data-types.md) \***

Die adjacency-Daten, die festgelegt werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist einer der Unter [Direct3D 10-Rückgabecodes aufgeführten Werte.](d3d10-graphics-reference-returnvalues.md)

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

 

 
