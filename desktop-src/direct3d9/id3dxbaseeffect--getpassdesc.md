---
description: Ruft eine Pass Beschreibung ab.
ms.assetid: 44c65a82-bcf4-49f5-9312-8320e133bb2f
title: 'ID3DXBaseEffect:: getpassdesc-Methode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetPassDesc
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 15a997470fddf5056b7191fcc3226ad210724041
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106363185"
---
# <a name="id3dxbaseeffectgetpassdesc-method"></a>ID3DXBaseEffect:: getpassdesc-Methode

Ruft eine Pass Beschreibung ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetPassDesc(
  [in]  D3DXHANDLE    hPass,
  [out] D3DXPASS_DESC *pDesc
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hpass* \[ in\]
</dt> <dd>

Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Pass-handle. Weitere Informationen finden Sie unter [Handles (Direct3D 9)](handles.md).

</dd> <dt>

*PDE SC* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **D3DXPASS \_ DESC**](d3dxpass-desc.md)\***

Gibt eine Beschreibung des angegebenen Pass zurück. Weitere Informationen finden Sie unter [**D3DXPASS \_**](d3dxpass-desc.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Wenn ein Effekt mit [D3DXFX \_ Not \_ cloneable](d3dxfx.md)erstellt wird, gibt diese Methode **null** -Zeiger (in [**D3DXPASS \_ DESC**](d3dxpass-desc.md)) an die Shader-Funktionen zurück.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> </dl>

 

 




