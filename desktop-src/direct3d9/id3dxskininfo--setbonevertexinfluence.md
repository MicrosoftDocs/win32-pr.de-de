---
description: Legt einen Einfluss Wert eines Knotens in einem einzelnen Scheitelpunkt fest.
ms.assetid: 9283866f-3dfe-467d-a74f-77e89c2778c4
title: 'ID3DXSkinInfo:: setbonevertexinfluence-Methode (D3DX9Mesh. h)'
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
ms.openlocfilehash: db84cdf9a1647bc5302c421e52d50f812e74596e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106365068"
---
# <a name="id3dxskininfosetbonevertexinfluence-method"></a>ID3DXSkinInfo:: setbonevertexinfluence-Methode

Legt einen Einfluss Wert eines Knotens in einem einzelnen Scheitelpunkt fest.

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

*bonumum* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Der Index des-Knochens. Muss zwischen 0 und der Anzahl der Knochen liegen.

</dd> <dt>

*Einflussfaktoren* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Index des Einfluss Arrays des angegebenen Knochen.

</dd> <dt>

*Gewichtung* \[ in\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

Der Blend-Faktor des angegebenen Knochen Einflusses.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> <dt>

[**ID3DXSkinInfo:: getbonevertexinfluence**](id3dxskininfo--getbonevertexinfluence.md)
</dt> <dt>

[**ID3DXSkinInfo:: findbonevertexinfluendceindex**](id3dxskininfo--findbonevertexinfluenceindex.md)
</dt> <dt>

[**ID3DXSkinInfo:: getboneingefluence**](id3dxskininfo--getboneinfluence.md)
</dt> </dl>

 

 
