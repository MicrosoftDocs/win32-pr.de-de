---
description: Ruft das Handle eines Parameters der obersten Ebene oder eines Struktur-Memberparameters ab, indem nach dessen Namen gesucht wird.
ms.assetid: fb03685e-e512-4293-80d7-6c2c0fc9ebfd
title: ID3DXBaseEffect::GetParameterByName-Methode (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetParameterByName
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 30a1e585cbbbaee4891e3e7dc2cd4e3d3c871fd33fe36daa51c9137c26bfdc7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119848680"
---
# <a name="id3dxbaseeffectgetparameterbyname-method"></a>ID3DXBaseEffect::GetParameterByName-Methode

Ruft das Handle eines Parameters der obersten Ebene oder eines Struktur-Memberparameters ab, indem nach dessen Namen gesucht wird.

## <a name="syntax"></a>Syntax


```C++
D3DXHANDLE GetParameterByName(
  [in] D3DXHANDLE hParameter,
  [in] LPCSTR     pName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hParameter* \[ In\]
</dt> <dd>

Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Handle des Parameters oder **NULL für** Parameter der obersten Ebene. Siehe [Handles (Direct3D 9).](handles.md)

</dd> <dt>

*pName* \[ In\]
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Eine Zeichenfolge, die den Parameternamen enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Gibt das Handle des angegebenen Parameters oder **NULL zurück,** wenn der Index ungültig war. Siehe [Handles (Direct3D 9).](handles.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> </dl>

 

 
