---
description: Ruft eine Textur ab.
ms.assetid: e009ccc2-4491-4976-9460-7478b2bd34c2
title: 'ID3DXBaseEffect:: GetTexture-Methode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetTexture
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 25ef71df1f9dcd84bbe6726fd3a13f9ec09eff17
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103761943"
---
# <a name="id3dxbaseeffectgettexture-method"></a>ID3DXBaseEffect:: GetTexture-Methode

Ruft eine Textur ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetTexture(
  [in]  D3DXHANDLE             hParameter,
  [out] LPDIRECT3DBASETEXTURE9 *ppTexture
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hparameter* \[ in\]
</dt> <dd>

Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Eindeutiger Bezeichner. Weitere Informationen finden Sie unter [Handles (Direct3D 9)](handles.md).

</dd> <dt>

*pptexture* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)\***

Gibt ein Textur Objekt zurück. Siehe [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> <dt>

[**SetTexture**](id3dxbaseeffect--settexture.md)
</dt> </dl>

 

 
