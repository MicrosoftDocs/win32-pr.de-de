---
description: Ruft die maximalen Gesichtseinflüsse in einem Dreiecksgitternetz mit dem angegebenen Indexpuffer ab.
ms.assetid: 72dc2440-87df-461e-80d0-9ad9b1e4d8ee
title: ID3DXSkinInfo::GetMaxFaceInfluences-Methode (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.GetMaxFaceInfluences
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 84e949c0b6140b4be0f55c47c0f24b3e3b2843009c5c0cd039c76caefa0667a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118800669"
---
# <a name="id3dxskininfogetmaxfaceinfluences-method"></a>ID3DXSkinInfo::GetMaxFaceInfluences-Methode

Ruft die maximalen Gesichtseinflüsse in einem Dreiecksgitternetz mit dem angegebenen Indexpuffer ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetMaxFaceInfluences(
  [in] LPDIRECT3DINDEXBUFFER9 pIB,
  [in] DWORD                  NumFaces,
  [in] DWORD                  *maxFaceInfluences
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pIB* \[ In\]
</dt> <dd>

Typ: **[ **LPDIRECT3DINDEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)**

Zeiger auf den Indexpuffer, der die Meshindexdaten enthält.

</dd> <dt>

*NumFaces* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Anzahl der Gesichter im Gitternetz.

</dd> <dt>

*maxFaceInfluences* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***

Zeiger auf die maximalen Gesichtseinflüsse.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> </dl>

 

 
