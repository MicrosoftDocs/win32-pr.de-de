---
description: 'ID3DX10Mesh::GenerateAdjaencyAndPointReps-Methode: Generieren Sie eine Liste von Gitternetzkanten sowie eine Liste von Gesichtern, die die einzelnen Kanten gemeinsam nutzen.'
ms.assetid: 3932e2b1-031d-4962-ad90-6e9da8cf2e0e
title: ID3DX10Mesh::GenerateAdjaencyAndPointReps-Methode (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GenerateAdjacencyAndPointReps
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 55198648be8952f975313dad3019063917eddf4d38f0a7d636039d5802f08e00
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119566940"
---
# <a name="id3dx10meshgenerateadjacencyandpointreps-method"></a>ID3DX10Mesh::GenerateAdjaencyAndPointReps-Methode

Generieren Sie eine Liste von Gitternetzrändern sowie eine Liste von Gesichtern, die die einzelnen Kanten gemeinsam nutzen.

## <a name="syntax"></a>Syntax


```C++
HRESULT GenerateAdjacencyAndPointReps(
  [in] FLOAT Epsilon
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Epsilon* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Gibt an, dass Scheitelpunkte, die sich in der Position um weniger als epsilon unterscheiden, als zufällig behandelt werden sollen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist einer der In [Direct3D 10-Rückgabecodes aufgeführten](d3d10-graphics-reference-returnvalues.md)Werte.

## <a name="remarks"></a>Hinweise

Nachdem eine Anwendung Adjazenzinformationen für ein Gitternetz generiert hat, können die Gitternetzdaten optimiert werden, um eine bessere Zeichnungsleistung zu erzielen.

Die Reihenfolge der Einträge im Adjazenzpuffer wird durch die Reihenfolge der Scheitelpunktindizes im Indexpuffer bestimmt. Das angrenzende Dreieck 0 entspricht immer dem Rand zwischen den Indizes der Ecken 0 und 1. Das angrenzende Dreieck 1 entspricht immer dem Rand zwischen den Indizes der Ecken 1 und 2, während das angrenzende Dreieck 2 dem Rand zwischen den Indizes der Ecken 2 und 0 entspricht.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[D3DX-Schnittstellen](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
