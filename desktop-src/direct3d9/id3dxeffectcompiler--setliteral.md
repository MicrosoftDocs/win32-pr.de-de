---
description: Schaltet den literalstatus eines Parameters um. Ein literalparameter weist einen Wert auf, der sich während der Lebensdauer eines Effekts nicht ändert.
ms.assetid: 09ebf666-8a50-4604-abef-aed0d92a6d49
title: 'ID3DXEffectCompiler:: setliteralmethode (D3DX9Shader. h)'
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
ms.openlocfilehash: 5a64426381876458b601b741050a01e5f35d084c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354356"
---
# <a name="id3dxeffectcompilersetliteral-method"></a>ID3DXEffectCompiler:: setliterale-Methode

Schaltet den literalstatus eines Parameters um. Ein literalparameter weist einen Wert auf, der sich während der Lebensdauer eines Effekts nicht ändert.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetLiteral(
  [in] D3DXHANDLE hParameter,
  [in] BOOL       Literal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hparameter* \[ in\]
</dt> <dd>

Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Eindeutiger Bezeichner für einen Parameter. Weitere Informationen finden Sie unter [Handles (Direct3D 9)](handles.md).

</dd> <dt>

*Literale* \[ in\]
</dt> <dd>

Typ: **[ **bool**](../winprog/windows-data-types.md)**

Legen Sie diese Einstellung auf " **true** " fest, um **den-Parameter als** Literalwert festzulegen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.

## <a name="remarks"></a>Bemerkungen

Diese Methoden ändern nur, ob der Parameter ein Literalwert ist oder nicht. Um den Wert eines Parameters zu ändern, verwenden Sie eine Methode wie [**ID3DXBaseEffect:: SetBool**](id3dxbaseeffect--setbool.md) oder [**ID3DXBaseEffect:: SetValue**](id3dxbaseeffect--setvalue.md).

Diese Funktion muss vor der Kompilierung des Effekts aufgerufen werden. Im folgenden finden Sie ein Beispiel dafür, wie Sie diese Funktion verwenden können:


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
| Header<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXEffectCompiler](id3dxeffectcompiler.md)
</dt> <dt>

[Verwendungen und Literale (Direct3D 9)](usages-and-literals.md)
</dt> <dt>

[**ID3DXEffectCompiler:: getliteral**](id3dxeffectcompiler--getliteral.md)
</dt> </dl>

 

 
