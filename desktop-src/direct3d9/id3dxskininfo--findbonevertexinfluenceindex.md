---
description: Ruft den Index des Knochen Einflusses ab, der sich auf einen einzelnen Scheitelpunkt auswirkt.
ms.assetid: vs|directx_sdk|~\id3dxskininfo__findbonevertexinfluenceindex.htm
title: 'ID3DXSkinInfo:: findbonevertexinfluendceindex-Methode (D3DX9Mesh. h)'
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
ms.openlocfilehash: 05a86e98e5001092700fdec12f2a7afc33ddf082
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106366433"
---
# <a name="id3dxskininfofindbonevertexinfluenceindex-method"></a>ID3DXSkinInfo:: findbonevertexinfluendceindex-Methode

Ruft den Index des Knochen Einflusses ab, der sich auf einen einzelnen Scheitelpunkt auswirkt.

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

*bonumum* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Der Index des-Knochens. Muss zwischen 0 und der Anzahl der Knochen liegen.

</dd> <dt>

*vertexnum* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Der Index des Scheitel Punkts, für den der Knochen Einfluss gefunden werden soll. Muss zwischen 0 und der Anzahl der Scheitel Punkte im Mesh liegen.

</dd> <dt>

*pinfluendceindex* \[ in, out\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***

Zeiger auf den Index des Knochen Einflusses, der vertexnum beeinflusst.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK. Wenn der angegebene Knochen den angegebenen Scheitelpunkt nicht beeinflusst, \_ wird "false" zurückgegeben. Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.

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

[**ID3DXSkinInfo:: setbonevertexinfluence**](id3dxskininfo--setbonevertexinfluence.md)
</dt> <dt>

[**ID3DXSkinInfo:: getboneingefluence**](id3dxskininfo--getboneinfluence.md)
</dt> </dl>

 

 
