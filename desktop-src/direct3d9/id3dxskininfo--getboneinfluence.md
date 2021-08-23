---
description: Ruft die Scheitelungen und Gewichtungen ab, die von einem -Gitter beeinflusst werden.
ms.assetid: 84cb064b-b6b2-402d-81cc-8c02de6f8b52
title: ID3DXSkinInfo::GetBoneInfluence-Methode (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.GetBoneInfluence
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8f49afb4175559bb5338c01c0ebb22fb89801aef5e7cafa62386e25c095ea139
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847305"
---
# <a name="id3dxskininfogetboneinfluence-method"></a>ID3DXSkinInfo::GetBoneInfluence-Methode

Ruft die Scheitelungen und Gewichtungen ab, die von einem -Gitter beeinflusst werden.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetBoneInfluence(
  [in]      DWORD Bone,
  [in, out] DWORD *vertices,
  [in, out] FLOAT *weights
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Besen* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Nummer des 500-00-

</dd> <dt>

*Scheiteltices* \[ in, out\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***

Erhalten Sie das Array von Scheitelpunkt, das von einem Gitter beeinflusst wird.

</dd> <dt>

*Gewichtungen* \[ in, out\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Hier erhalten Sie das Array von Gewichtungen, die von einem 2000-2016-2016 beeinflusst werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert D3D \_ OK. Wenn bei der Methode ein Fehler auftritt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.

## <a name="remarks"></a>Hinweise

Verwenden [**Sie ID3DXSkinInfo::GetNumBoneInfluences,**](id3dxskininfo--getnumboneinfluences.md) um herauszufinden, wie viele Scheitelpunkt die Flüsse beeinflussen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> <dt>

[**ID3DXSkinInfo::SetBoneInfluence**](id3dxskininfo--setboneinfluence.md)
</dt> </dl>

 

 
