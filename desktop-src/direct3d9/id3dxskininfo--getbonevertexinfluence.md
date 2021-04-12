---
description: Ruft den Blend Faktor und den Scheitelpunkt ab, der von einem angegebenen Knochen Einfluss betroffen ist.
ms.assetid: bbed4766-e571-4a9e-b7e3-047052470cbe
title: 'ID3DXSkinInfo:: getbonevertexinfluence-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.GetBoneVertexInfluence
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6e3cb7c530ed72a65f9a3e8de6b0735b1a7ae5e4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354076"
---
# <a name="id3dxskininfogetbonevertexinfluence-method"></a>ID3DXSkinInfo:: getbonevertexinfluence-Methode

Ruft den Blend Faktor und den Scheitelpunkt ab, der von einem angegebenen Knochen Einfluss betroffen ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetBoneVertexInfluence(
  [in]      DWORD boneNum,
  [in]      DWORD influenceNum,
  [in, out] FLOAT *pWeight,
  [in, out] DWORD *pVertexNum
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

*pweight* \[ in, out\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)\***

Zeiger auf den Blend-Faktor, der durch Einflussfaktoren beeinflusst wird.

</dd> <dt>

*pvertexnum* \[ in, out\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***

Zeiger auf den Scheitelpunkt, der durch Einflussfaktoren beeinflusst wird.

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

[**ID3DXSkinInfo:: setbonevertexinfluence**](id3dxskininfo--setbonevertexinfluence.md)
</dt> <dt>

[**ID3DXSkinInfo:: findbonevertexinfluendceindex**](id3dxskininfo--findbonevertexinfluenceindex.md)
</dt> <dt>

[**ID3DXSkinInfo:: getboneingefluence**](id3dxskininfo--getboneinfluence.md)
</dt> </dl>

 

 
