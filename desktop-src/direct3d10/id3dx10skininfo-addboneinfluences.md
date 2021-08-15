---
description: Ermöglichen Sie es einem vorhandenen Gitter, eine Gruppe von Scheitelpunkte zu beeinflussen und zu definieren, wie viel Einfluss die Ziese auf die einzelnen Scheitelpunkte hat.
ms.assetid: 37ba97a8-ba40-4700-b8b8-fa7cc9118307
title: ID3DX10SkinInfo::AddBoneInfluences-Methode (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.AddBoneInfluences
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 7f640481c664c51614a45ff10250a4c40d769a27d793868c4bec316c2cab9ded
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117914346"
---
# <a name="id3dx10skininfoaddboneinfluences-method"></a>ID3DX10SkinInfo::AddBoneInfluences-Methode

Ermöglichen Sie es einem vorhandenen Gitter, eine Gruppe von Scheitelpunkte zu beeinflussen und zu definieren, wie viel Einfluss die Ziese auf die einzelnen Scheitelpunkte hat.

## <a name="syntax"></a>Syntax


```C++
HRESULT AddBoneInfluences(
  [in] UINT  BoneIndex,
  [in] UINT  InfluenceCount,
  [in] UINT  *pIndices,
  [in] float *pWeights
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Index* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Ein Index, der einen vorhandenen Zeichner angibt. Muss zwischen 0 und dem von [**ID3DX10SkinInfo::GetNumBones zurückgegebenen Wert liegen.**](id3dx10skininfo-getnumbones.md)

</dd> <dt>

*InfluenceCount* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Anzahl der Scheitelpunkt, die dem Einfluss des Gitters hinzugefügt werden.

</dd> <dt>

*pIndices* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)\***

Zeiger auf ein Array von Scheitelpunktindizes. Jedes Member dieses Arrays verfügt über einen entsprechenden Member in pWeights, damit pIndices \[ i \] pWeights \[ i \] entspricht. Der entsprechende Wert in pWeights i bestimmt, wie viel EinflussIndex auf den von \[ pIndices i indizierten Scheitelpunkt \] \[ \] hat. Die Größe des pIndices-Arrays muss größer oder gleich InfluenceCount sein.

</dd> <dt>

*pWeights* \[ In\]
</dt> <dd>

Typ: **\* float**

Zeiger auf ein Array von Gewichtungen. Jedes Member dieses Arrays verfügt über ein entsprechendes Member in pIndices, damit pWeights \[ i \] pIndices \[ i \] entspricht. Jeder Wert in "pWeights" liegt zwischen 0 und 1 und definiert den Einfluss, den die Zie auf jeden Scheitelpunkt hat. Die Größe von pWeights muss größer oder gleich InfluenceCount sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert S \_ OK. Wenn bei der Methode ein Fehler auftritt, kann der Rückgabewert E \_ INVALIDARG oder E \_ OUTOFMEMORY sein.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DX10SkinInfo](id3dx10skininfo.md)
</dt> <dt>

[D3DX-Schnittstellen](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
