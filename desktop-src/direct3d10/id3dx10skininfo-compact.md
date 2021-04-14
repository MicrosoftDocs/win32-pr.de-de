---
description: Begrenzen Sie die Anzahl der Knochen, die einen Scheitelpunkt beeinflussen können, und/oder schränken Sie die Menge der Auswirkungen ein, die ein Knochen auf einen Scheitelpunkt aufweisen kann.
ms.assetid: 75c4d2eb-0a43-494d-9642-4c08aa814794
title: 'ID3DX10SkinInfo:: Compact-Methode (d3dx10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.Compact
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 379343688a1fd2ffe5ebd968dc984fa09faada7d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394090"
---
# <a name="id3dx10skininfocompact-method"></a>ID3DX10SkinInfo:: Compact-Methode

Begrenzen Sie die Anzahl der Knochen, die einen Scheitelpunkt beeinflussen können, und/oder schränken Sie die Menge der Auswirkungen ein, die ein Knochen auf einen Scheitelpunkt aufweisen kann.

## <a name="syntax"></a>Syntax


```C++
HRESULT Compact(
  [in] UINT  MaxPerVertexInfluences,
  [in] UINT  ScaleMode,
  [in] float MinWeight
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Maxpervertexeinflüsse* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Die maximale Anzahl von Knochen, die einen bestimmten Scheitelpunkt beeinflussen können. Dieser Wert wird ignoriert, wenn er größer ist als der Wert, der von [**ID3DX10SkinInfo:: getmaxbonein fluences**](id3dx10skininfo-getmaxboneinfluences.md)zurückgegeben wurde.

</dd> <dt>

*Skalemode* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Ein Flag, das beschreibt, wie die verbleibenden Gewichtungen auf einem bestimmten Scheitelpunkt skaliert werden, nachdem einige von minweight abgeschnitten wurden. Wenn d3dx10 \_ skininfo \_ keine \_ Skalierung angegeben ist, werden die Gewichtungen überhaupt nicht skaliert. Wenn d3dx10 \_ skininfo \_ \_ auf \_ 1 festgelegt ist, werden die Gewichtungen größer als minweight zentral hochskaliert, sodass Sie bis zu 1,0 addieren. Wenn d3dx10 \_ skininfo \_ Scale \_ to \_ Total angegeben wird, werden die Gewichtungen größer als minweight zentral hochskaliert, sodass Sie den ursprünglichen Gesamtwert hinzufügen.

</dd> <dt>

*Minweight* \[ in\]
</dt> <dd>

Typ: **float**

Der minimale Prozentsatz der Auswirkung (oder Gewichtung), den alle Knochen für einen beliebigen Scheitelpunkt aufweisen können. Dieser Wert muss zwischen 0 und 1 liegen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert lauten: e \_ outo-Memory oder e \_ invalidArg.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx10. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3dx10. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DX10SkinInfo](id3dx10skininfo.md)
</dt> <dt>

[D3DX-Schnittstellen](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
