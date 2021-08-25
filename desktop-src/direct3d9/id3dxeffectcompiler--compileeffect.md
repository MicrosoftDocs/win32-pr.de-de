---
description: Kompilieren sie einen Effekt.
ms.assetid: be6f862a-5091-4a06-a27a-308e81360129
title: ID3DXEffectCompiler::CompileEffect-Methode (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectCompiler.CompileEffect
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: f3769f3f7433aadc55e766d68ecc152a4e26444cf506344f80e3f11a0bca8fcf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951660"
---
# <a name="id3dxeffectcompilercompileeffect-method"></a>ID3DXEffectCompiler::CompileEffect-Methode

Kompilieren sie einen Effekt.

## <a name="syntax"></a>Syntax


```C++
HRESULT CompileEffect(
  [in]          DWORD        Flags,
  [out, retval] LPD3DXBUFFER *ppEffect,
  [out, retval] LPD3DXBUFFER *ppErrorMsgs
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Flags* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Kompilierungsoptionen, die durch verschiedene Flags identifiziert werden. Der Direct3D 10 HLSL-Compiler ist jetzt die Standardeinstellung. Weitere Informationen finden Sie unter [D3DXSHADER-Flags.](d3dxshader-flags.md)

</dd> <dt>

*ppEffect* \[ out, retval\]
</dt> <dd>

Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Puffer, der den kompilierten Effekt enthält. Weitere Informationen zum Zugriff auf den Puffer finden Sie unter [**ID3DXBuffer.**](id3dxbuffer.md)

</dd> <dt>

*ppErrorMsgs* \[ out, retval\]
</dt> <dd>

Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Puffer, der mindestens die erste kompilierungsfehlermeldung enthält, die aufgetreten ist. Dies schließt Compilerfehler und Kompilierungsfehler auf hoher Ebene ein. Weitere Informationen zum Zugriff auf den Puffer finden Sie unter [**ID3DXBuffer.**](id3dxbuffer.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert S \_ OK.

Wenn die Argumente ungültig sind, gibt die Methode D3DERR \_ INVALIDCALL zurück.

Wenn die Methode fehlschlägt, ist der Rückgabewert E \_ FAIL.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXEffectCompiler](id3dxeffectcompiler.md)
</dt> </dl>

 

 
