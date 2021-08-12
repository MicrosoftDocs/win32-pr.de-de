---
description: Schaltet den Literalstatus eines Parameters um. Ein Literalparameter hat einen Wert, der sich während der Lebensdauer eines Effekts nicht ändert.
ms.assetid: 09ebf666-8a50-4604-abef-aed0d92a6d49
title: ID3DXEffectCompiler::SetLiteral-Methode (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectCompiler.SetLiteral
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 5d28ee64c1d1e52b4005c1a81ef4690c539a09e06eb7a8378a246184cf4d2fd8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118295831"
---
# <a name="id3dxeffectcompilersetliteral-method"></a>ID3DXEffectCompiler::SetLiteral-Methode

Schaltet den Literalstatus eines Parameters um. Ein Literalparameter hat einen Wert, der sich während der Lebensdauer eines Effekts nicht ändert.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetLiteral(
  [in] D3DXHANDLE hParameter,
  [in] BOOL       Literal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hParameter* \[ In\]
</dt> <dd>

Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Eindeutiger Bezeichner für einen Parameter. Siehe [Handles (Direct3D 9)](handles.md).

</dd> <dt>

*Literal* \[ In\]
</dt> <dd>

Typ: **[ **BOOL**](../winprog/windows-data-types.md)**

Legen Sie diese Einstellung auf **TRUE** fest, um den Parameter als Literal festzulegen, und **FALSE,** wenn der Parameter den Wert während der Shaderlebensdauer ändern kann.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.

## <a name="remarks"></a>Hinweise

Diese Methode ändert nur, ob der Parameter ein Literal ist oder nicht. Um den Wert eines Parameters zu ändern, verwenden Sie eine Methode wie [**ID3DXBaseEffect::SetBool**](id3dxbaseeffect--setbool.md) oder [**ID3DXBaseEffect::SetValue.**](id3dxbaseeffect--setvalue.md)

Diese Funktion muss aufgerufen werden, bevor der Effekt kompiliert wird. Hier sehen Sie ein Beispiel für die Verwendung dieser Funktion:


```
    LPD3DXEFFECTCOMPILER pEffectCompiler;
    char errors[1000];
    HRESULT hr;
    
    hr = D3DXCreateEffectCompilerFromFile("shader.fx",
                                          NULL, NULL, 0,
                                          &pEffectCompiler, 
                                          &errors);
    
    //In the fx file, literalInt is declared as an int.
    //By calling this function, the compiler will treat
    //it as a literal (i.e. #define)
    hr = pEffectCompiler->SetLiteral("literalInt", TRUE);
    
    //create ten different variations of the same effect
    LPD3DXBUFFER pEffects[10];
    LPD3DXBUFFER pErrors;
    for(int i = 0; i < 10; ++i)
    {
        hr = pEffectCompiler->SetInt("literalInt", i);
    
        hr = pEffectCompiler->CompileEffect(0, &pEffects[i], &pErrors);
    }
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXEffectCompiler](id3dxeffectcompiler.md)
</dt> <dt>

[Verwendungen und Literale (Direct3D 9)](usages-and-literals.md)
</dt> <dt>

[**ID3DXEffectCompiler::GetLiteral**](id3dxeffectcompiler--getliteral.md)
</dt> </dl>

 

 
