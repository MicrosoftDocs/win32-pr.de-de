---
description: Ruft das Handle eines Parameters der obersten Ebene oder eines Strukturmemberparameters ab, indem seine Semantik mit einer Suche ohne Beachtung der Groß-/Kleinschreibung gesucht wird.
ms.assetid: 3de3791a-fe09-4a39-bd6f-0e20a641dd32
title: ID3DXBaseEffect::GetParameterBySemantic-Methode (D3DX9Shader.h)
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
ms.openlocfilehash: fa00ef4585462f068e95fcefca8332acd46930efaf1bb1c108a471511ab63eb4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119791010"
---
# <a name="id3dxbaseeffectgetparameterbysemantic-method"></a>ID3DXBaseEffect::GetParameterBySemantic-Methode

Ruft das Handle eines Parameters der obersten Ebene oder eines Strukturmemberparameters ab, indem seine Semantik mit einer Suche ohne Beachtung der Groß-/Kleinschreibung gesucht wird.

## <a name="syntax"></a>Syntax


```C++
D3DXHANDLE GetParameterBySemantic(
  [in] D3DXHANDLE hParameter,
  [in] LPCSTR     pSemantic
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hParameter* \[ In\]
</dt> <dd>

Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Handle des Parameters oder **NULL** für Parameter der obersten Ebene. Siehe [Handles (Direct3D 9)](handles.md).

</dd> <dt>

*pSemantic* \[ In\]
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Zeichenfolge, die den semantischen Namen enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Gibt das Handle des ersten Parameters zurück, der mit der angegebenen Semantik übereinstimmt, oder **NULL,** wenn die Semantik nicht gefunden wurde. Siehe [Handles (Direct3D 9)](handles.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> </dl>

 

 
