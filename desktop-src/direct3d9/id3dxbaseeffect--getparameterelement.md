---
description: Das Handle eines Array Element-Parameters erhalten.
ms.assetid: fe8edbc5-dc1d-4386-8149-489541d55bde
title: 'ID3DXBaseEffect:: getparameterelement-Methode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetParameterElement
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 5130ccf57634f9b1a569a1dd70833fe2014e1a74
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355876"
---
# <a name="id3dxbaseeffectgetparameterelement-method"></a>ID3DXBaseEffect:: getparameterelement-Methode

Das Handle eines Array Element-Parameters erhalten.

## <a name="syntax"></a>Syntax


```C++
D3DXHANDLE GetParameterElement(
  [in] D3DXHANDLE hParameter,
  [in] UINT       ElementIndex
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hparameter* \[ in\]
</dt> <dd>

Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Handle des Arrays. Weitere Informationen finden Sie unter [Handles (Direct3D 9)](handles.md).

</dd> <dt>

*Element Index* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Array Element Index.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Gibt das Handle des angegebenen Parameters zurück, oder **null** , wenn hparameter oder Elementindex ungültig ist. Weitere Informationen finden Sie unter [Handles (Direct3D 9)](handles.md).

## <a name="remarks"></a>Bemerkungen

Diese Methode wird verwendet, um ein Element eines Parameters zu erhalten, bei dem es sich um ein Array handelt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> </dl>

 

 
