---
description: Ruft den Index des Einflusses ab, der sich auf einen einzelnen Scheitelpunkt auswirkt.
ms.assetid: vs|directx_sdk|~\id3dxskininfo__findbonevertexinfluenceindex.htm
title: ID3DXSkinInfo::FindBoneVertexInfluenceIndex-Methode (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.FindBoneVertexInfluenceIndex
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9d9035f6c791708dc0b7d84ffd69380f801f4ecce8525c03bb1ac00a3902a1d8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119727790"
---
# <a name="id3dxskininfofindbonevertexinfluenceindex-method"></a>ID3DXSkinInfo::FindBoneVertexInfluenceIndex-Methode

Ruft den Index des Einflusses ab, der sich auf einen einzelnen Scheitelpunkt auswirkt.

## <a name="syntax"></a>Syntax


```C++
HRESULT FindBoneVertexInfluenceIndex(
  [in]      DWORD boneNum,
  [in]      DWORD vertexNum,
  [in, out] DWORD *pInfluenceIndex
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*enumerationNum* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Index des Verzeichnisses. Muss zwischen 0 (0) und der Anzahl der Nummern (1) sein.

</dd> <dt>

*vertexNum* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Index des Scheitelpunkts, für den der Einfluss des Würfes gefunden werden soll. Muss zwischen 0 und der Anzahl der Scheitelpunkte im Netz sein.

</dd> <dt>

*pInfluenceIndex* \[ in, out\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***

Zeiger auf den Index des Einflusses, der sich auf vertexNum auswirkt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert S \_ OK. Wenn der angegebene Zähler den angegebenen Scheitelpunkt nicht beeinflusst, wird S \_ FALSE zurückgegeben. Wenn die Methode fehlschlägt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> <dt>

[**ID3DXSkinInfo::GetBoneVertexInfluence**](id3dxskininfo--getbonevertexinfluence.md)
</dt> <dt>

[**ID3DXSkinInfo::SetBoneVertexInfluence**](id3dxskininfo--setbonevertexinfluence.md)
</dt> <dt>

[**ID3DXSkinInfo::GetBoneInfluence**](id3dxskininfo--getboneinfluence.md)
</dt> </dl>

 

 
