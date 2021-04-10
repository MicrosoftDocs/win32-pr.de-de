---
description: Eine Liste der Scheitel Punkte, die von einem bestimmten Knochen beeinflusst werden, und eine Liste der Auswirkungen von Bone auf jeden Scheitelpunkt erhalten.
ms.assetid: d1dea694-874d-4f21-87a8-f6b013617544
title: 'ID3DX10SkinInfo:: getboneingefluences-Methode (d3dx10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.GetBoneInfluences
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 9aead6b1dd381011a922c5bfbc1874976a78417c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219708"
---
# <a name="id3dx10skininfogetboneinfluences-method"></a>ID3DX10SkinInfo:: getboneingefluences-Methode

Eine Liste der Scheitel Punkte, die von einem bestimmten Knochen beeinflusst werden, und eine Liste der Auswirkungen von Bone auf jeden Scheitelpunkt erhalten.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetBoneInfluences(
  [in]      UINT  BoneIndex,
  [in]      UINT  Offset,
  [in]      UINT  Count,
  [in, out] UINT  *pDestIndices,
  [in, out] float *pDestWeights
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Boneingedex* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Ein Index, der einen vorhandenen Knochen Wert angibt. Muss zwischen 0 und dem von [**ID3DX10SkinInfo:: getnumbones**](id3dx10skininfo-getnumbones.md)zurückgegebenen Wert liegen.

</dd> <dt>

*Offset* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Ein Offset vom oberen Rand der Liste der von ihm beeinflussten Scheitel Punkte. Dieser Wert muss zwischen 0 und dem von [**ID3DX10SkinInfo:: getboneinfluscecount**](id3dx10skininfo-getboneinfluencecount.md)zurückgegebenen Wert liegen.

</dd> <dt>

*Anzahl* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Die Anzahl der Indizes und Gewichtungen, die abgerufen werden sollen. Muss zwischen 0 und dem von ID3DX10SkinInfo:: getboneinfluscecount zurückgegebenen Wert liegen.

</dd> <dt>

*pdestindices* \[ in, out\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)\***

Eine Liste von Indizes in den Scheitelpunkt Puffer, die jeweils einen Vertex darstellen, der durch den Knochen beeinflusst wird. Diese Werte entsprechen den Werten in "pdestgewichtungen", sodass "pdestindices \[ i" \] pdestgewichtungen \[ i entspricht \] .

</dd> <dt>

*pdestgewichtungen* \[ in, out\]
</dt> <dd>

Typ: **float \***

Eine Liste der Auswirkungen, die der Knochen auf jedem Scheitelpunkt hat. Diese Werte entsprechen den Werten in pdestindices, sodass pdestgewichtungen \[ ich \] pdestindices \[ i \] . f verwende.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert lauten: E \_ invalidArg oder e \_ oudef Memory.

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

 

 
