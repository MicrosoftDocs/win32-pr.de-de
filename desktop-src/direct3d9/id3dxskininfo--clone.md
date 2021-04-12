---
description: Klont ein Skin Info-Objekt.
ms.assetid: 82d0a78a-95f3-4b09-bc1a-b4bc663e0850
title: 'ID3DXSkinInfo:: Clone-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.Clone
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: edd9776b75d027a32b32b58c59fc82daaebfa3ad
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219483"
---
# <a name="id3dxskininfoclone-method"></a>ID3DXSkinInfo:: Clone-Methode

Klont ein Skin Info-Objekt.

## <a name="syntax"></a>Syntax


```C++
HRESULT Clone(
  [in, out] LPD3DXSKININFO *ppSkinInfo
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppskininfo* \[ in, out\]
</dt> <dd>

Typ: **[ **LPD3DXSKININFO**](id3dxskininfo.md)\***

Adresse eines Zeigers auf ein [**ID3DXSkinInfo**](id3dxskininfo.md) -Objekt, das das geklonte Objekt enthält, wenn die Methode erfolgreich ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> </dl>

 

 




