---
description: Legt den Typ des flexiblen Vertex-Formats (FVF) fest.
ms.assetid: e581dcd4-7e17-4c36-aac9-c2942924cf51
title: 'ID3DXSkinInfo:: setf VF-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.SetFVF
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 010385597442ba1546c20122f6551fca0cfcf81c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106370394"
---
# <a name="id3dxskininfosetfvf-method"></a>ID3DXSkinInfo:: setf VF-Methode

Legt den Typ des flexiblen Vertex-Formats (FVF) fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetFVF(
  [in] DWORD FVF
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*F-VF* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Flexibles Vertex-Format. Siehe [D3DFVF](d3dfvf.md).

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

 

 
