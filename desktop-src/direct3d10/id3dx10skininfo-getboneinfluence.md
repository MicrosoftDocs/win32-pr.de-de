---
description: Gibt die Menge der Auswirkung an, die ein bestimmter Knochen über einem bestimmten Scheitelpunkt hat.
ms.assetid: 0586fdfd-e5b1-4699-b489-c54a0f305ee4
title: 'ID3DX10SkinInfo:: getboneingefluence-Methode (d3dx10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.GetBoneInfluence
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: b2f7e6b75e9c0f9f08463b6dacf9d7c9d72f4f28
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106351973"
---
# <a name="id3dx10skininfogetboneinfluence-method"></a>ID3DX10SkinInfo:: getboneingefluence-Methode

Gibt die Menge der Auswirkung an, die ein bestimmter Knochen über einem bestimmten Scheitelpunkt hat.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetBoneInfluence(
  [in] UINT  BoneIndex,
  [in] UINT  InfluenceIndex,
  [in] float *pWeight
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Boneingedex* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Ein Index, der einen vorhandenen Knochen Wert angibt. Muss zwischen 0 und dem von [**ID3DX10SkinInfo:: getnumbones**](id3dx10skininfo-getnumbones.md)zurückgegebenen Wert liegen.

</dd> <dt>

*Einflussfaktor ceindex* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Ein Index in der Liste der in der Liste der von ihm Einfluss enden Scheitel Punkte.

</dd> <dt>

*pweight* \[ in\]
</dt> <dd>

Typ: **float \***

Die Menge der Auswirkung zwischen 0 und 1, die der Knochen über dem Scheitelpunkt hat.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert E \_ invalidArg lauten.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie ID3DX10SkinInfo:: getboneinfluencecount, um herauszufinden, wie viele Scheitel Punkte der Knochen Einfluss hat.

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

 

 
