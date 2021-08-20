---
description: Begrenzen Sie die Anzahl von Zieten, die einen Scheitelpunkt beeinflussen können, und/oder begrenzen Sie den Einfluss, den ein Fluss auf einen Scheitelpunkt haben kann.
ms.assetid: 75c4d2eb-0a43-494d-9642-4c08aa814794
title: ID3DX10SkinInfo::Compact-Methode (D3DX10.h)
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
ms.openlocfilehash: 3aab3534ea55d2f6675ef1e65b03d19f4c516562b242e284ee2865f98bc03f18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119046908"
---
# <a name="id3dx10skininfocompact-method"></a>ID3DX10SkinInfo::Compact-Methode

Begrenzen Sie die Anzahl von Zieten, die einen Scheitelpunkt beeinflussen können, und/oder begrenzen Sie den Einfluss, den ein Fluss auf einen Scheitelpunkt haben kann.

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

*MaxPerVertexInfluences* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Die maximale Anzahl von Zieten, die einen bestimmten Scheitelpunkt beeinflussen können. Dieser Wert wird ignoriert, wenn er größer als der von [**ID3DX10SkinInfo::GetMaxBoneInfluences zurückgegebene**](id3dx10skininfo-getmaxboneinfluences.md)Wert ist.

</dd> <dt>

*ScaleMode* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Ein Flag, das beschreibt, wie die verbleibenden Gewichtungen auf einem bestimmten Scheitelpunkt skaliert werden, nachdem einige von MinWeight abgeschnitten wurden. Wenn D3DX10 \_ SKININFO \_ NO SCALING angegeben \_ ist, werden die Gewichtungen überhaupt nicht skaliert. Wenn D3DX10 \_ SKININFO \_ SCALE TO \_ \_ 1 angegeben ist, werden die Gewichtungen, die größer als MinWeight sind, so hochskaliert, dass sie bis zu 1,0 addiert werden. Wenn D3DX10 \_ SKININFO \_ SCALE TO TOTAL \_ angegeben \_ ist, werden die Gewichtungen, die größer als MinWeight sind, hochskaliert, sodass sie zur ursprünglichen Summe addiert werden.

</dd> <dt>

*MinWeight* \[ In\]
</dt> <dd>

Typ: **float**

Der Mindestprozentsatz des Einflusses bzw. der Gewichtung, den ein beliebiger Zähler auf einem Scheitelpunkt haben kann. Dieser Wert muss zwischen 0 und 1 sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert E \_ OUTOFMEMORY oder E \_ INVALIDARG sein.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DX10SkinInfo](id3dx10skininfo.md)
</dt> <dt>

[D3DX-Schnittstellen](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
