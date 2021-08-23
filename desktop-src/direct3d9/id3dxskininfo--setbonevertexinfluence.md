---
description: Legt einen Einflusswert eines Würfes auf einen einzelnen Scheitelpunkt fest.
ms.assetid: 9283866f-3dfe-467d-a74f-77e89c2778c4
title: ID3DXSkinInfo::SetBoneVertexInfluence-Methode (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.SetBoneVertexInfluence
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 950c72ed89c9204fb2369f175effd381548cb1913e9a2949666f6a0f4ea9aad9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119674690"
---
# <a name="id3dxskininfosetbonevertexinfluence-method"></a>ID3DXSkinInfo::SetBoneVertexInfluence-Methode

Legt einen Einflusswert eines Würfes auf einen einzelnen Scheitelpunkt fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetBoneVertexInfluence(
  [in] DWORD boneNum,
  [in] DWORD influenceNum,
  [in] FLOAT weight
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*enumerationNum* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Index des Verzeichnisses. Muss zwischen 0 (0) und der Anzahl der Nummern (1) sein.

</dd> <dt>

*influenceNum* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Index des Einflussarrays des angegebenen Verzeichnisses.

</dd> <dt>

*Gewichtung* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Der Mischungsfaktor des angegebenen Einflussfaktors.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> <dt>

[**ID3DXSkinInfo::GetBoneVertexInfluence**](id3dxskininfo--getbonevertexinfluence.md)
</dt> <dt>

[**ID3DXSkinInfo::FindBoneVertexInfluenceIndex**](id3dxskininfo--findbonevertexinfluenceindex.md)
</dt> <dt>

[**ID3DXSkinInfo::GetBoneInfluence**](id3dxskininfo--getboneinfluence.md)
</dt> </dl>

 

 
