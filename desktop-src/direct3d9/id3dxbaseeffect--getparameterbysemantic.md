---
description: Ruft das Handle eines Parameters der obersten Ebene oder eines Strukturmember-Parameters ab, indem seine Semantik mit einer Suche ohne Berücksichtigung der Groß-/Kleinschreibung gesucht wird
ms.assetid: 3de3791a-fe09-4a39-bd6f-0e20a641dd32
title: 'ID3DXBaseEffect:: getparameterbysemantic-Methode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetParameterBySemantic
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: c70d30d68d73d6c4dd33d483747be4293a255693
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355877"
---
# <a name="id3dxbaseeffectgetparameterbysemantic-method"></a>ID3DXBaseEffect:: getparameterbysemantic-Methode

Ruft das Handle eines Parameters der obersten Ebene oder eines Strukturmember-Parameters ab, indem seine Semantik mit einer Suche ohne Berücksichtigung der Groß-/Kleinschreibung gesucht wird

## <a name="syntax"></a>Syntax


```C++
D3DXHANDLE GetParameterBySemantic(
  [in] D3DXHANDLE hParameter,
  [in] LPCSTR     pSemantic
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hparameter* \[ in\]
</dt> <dd>

Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Handle des-Parameters oder **null** für Parameter der obersten Ebene. Weitere Informationen finden Sie unter [Handles (Direct3D 9)](handles.md).

</dd> <dt>

*psemantic* \[ in\]
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Zeichenfolge, die den semantischen Namen enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Gibt das Handle des ersten Parameters zurück, der der angegebenen Semantik entspricht, oder **null** , wenn die Semantik nicht gefunden wurde. Weitere Informationen finden Sie unter [Handles (Direct3D 9)](handles.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> </dl>

 

 
