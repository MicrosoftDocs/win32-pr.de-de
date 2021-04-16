---
description: Generieren Sie eine Liste mit Gitter Kanten sowie eine Liste der Flächen, die die einzelnen Kanten gemeinsam verwenden.
ms.assetid: 3932e2b1-031d-4962-ad90-6e9da8cf2e0e
title: 'ID3DX10Mesh:: generateaccessumcyandpointreps-Methode (d3dx10. h)'
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
ms.openlocfilehash: c46cf83931c95116132798ca971f9d4e61da2af8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104530992"
---
# <a name="id3dx10meshgenerateadjacencyandpointreps-method"></a>ID3DX10Mesh:: generateaccessumcyandpointreps-Methode

Generieren Sie eine Liste mit Gitter Kanten sowie eine Liste der Flächen, die die einzelnen Kanten gemeinsam verwenden.

## <a name="syntax"></a>Syntax


```C++
HRESULT GenerateAdjacencyAndPointReps(
  [in] FLOAT Epsilon
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Epsilon* \[ in\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

Gibt an, dass Scheitel Punkte, die sich an einer Position um weniger als Epsilon unterscheiden, als Coincident behandelt werden sollen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist einer der Werte, die in [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)aufgelistet sind.

## <a name="remarks"></a>Bemerkungen

Nachdem eine Anwendung Informationen zu einem Mesh generiert hat, können die Mesh-Daten optimiert werden, um die Leistung zu verbessern.

Die Reihenfolge der Einträge im Anfügungs Puffer wird durch die Reihenfolge der Scheitelpunkt Indizes im Index Puffer bestimmt. Das angrenzende Dreieck 0 entspricht immer dem Rand zwischen den Indizes der Ecken 0 und 1. Das angrenzende Dreieck 1 entspricht immer dem Rand zwischen den Indizes der Ecken 1 und 2, während das angrenzende Dreieck 2 dem Rand zwischen den Indizes der Ecken 2 und 0 entspricht.

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

 

 
