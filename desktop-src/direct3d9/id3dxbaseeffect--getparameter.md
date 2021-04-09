---
description: Ruft das Handle eines Parameters der obersten Ebene oder eines Strukturmember-Parameters ab.
ms.assetid: 940f1bfd-ce62-4c86-88cc-787e62cf6a93
title: 'ID3DXBaseEffect:: GetParameter-Methode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetParameter
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b7c96c371b36b8dcfc2e3e64a95798347ca3a6ea
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104050936"
---
# <a name="id3dxbaseeffectgetparameter-method"></a>ID3DXBaseEffect:: GetParameter-Methode

Ruft das Handle eines Parameters der obersten Ebene oder eines Strukturmember-Parameters ab.

## <a name="syntax"></a>Syntax


```C++
D3DXHANDLE GetParameter(
  [in] D3DXHANDLE hParameter,
  [in] UINT       Index
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hparameter* \[ in\]
</dt> <dd>

Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Handle des-Parameters oder **null** für Parameter der obersten Ebene. Weitere Informationen finden Sie unter [Handles (Direct3D 9)](handles.md).

</dd> <dt>

*Index* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Parameterindex.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Gibt das Handle des angegebenen Parameters oder **null** zurück, wenn der Index ungültig ist. Weitere Informationen finden Sie unter [Handles (Direct3D 9)](handles.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> </dl>

 

 
