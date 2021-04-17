---
description: Legt die Scheitelpunkt Deklaration fest.
ms.assetid: cbb802ac-f0ba-41e6-8c67-a787982f975f
title: 'ID3DXSkinInfo:: setdeclaration-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.SetDeclaration
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 821801647ca1aee3deabe69d911bd1cab5f7eb4f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354047"
---
# <a name="id3dxskininfosetdeclaration-method"></a>ID3DXSkinInfo:: setdeclaration-Methode

Legt die Scheitelpunkt Deklaration fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetDeclaration(
  [in] const D3DVERTEXELEMENT9 *pDeclaration
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pdeclaration* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***

Zeiger auf ein Array von [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) -Elementen.

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
</dt> <dt>

[**ID3DXSkinInfo:: getDeclaration**](id3dxskininfo--getdeclaration.md)
</dt> </dl>

 

 




