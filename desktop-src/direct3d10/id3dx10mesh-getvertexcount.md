---
description: Die Anzahl der Scheitel Punkte im Mesh.
ms.assetid: fea8a3b5-ca10-4066-b2ca-6579829d31b6
title: 'ID3DX10Mesh:: getvertexcount-Methode (d3dx10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetVertexCount
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 189be6ff6872cfb85c2f336c29dedef2e435382e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355035"
---
# <a name="id3dx10meshgetvertexcount-method"></a>ID3DX10Mesh:: getvertexcount-Methode

Die Anzahl der Scheitel Punkte im Mesh. Ein Mesh kann mehrere Scheitelpunkt Puffer enthalten (d. h., ein Vertex-Puffer enthält möglicherweise alle Positionsdaten, eine andere enthält möglicherweise alle Texturkoordinaten Daten usw.), aber jeder Scheitelpunkt Puffer enthält die gleiche Anzahl von Elementen.

## <a name="syntax"></a>Syntax


```C++
UINT GetVertexCount();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Die Anzahl der Scheitel Punkte im Mesh.

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

 

 
