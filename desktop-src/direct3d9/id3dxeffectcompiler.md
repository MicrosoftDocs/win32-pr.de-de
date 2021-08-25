---
description: Die ID3DXEffectCompiler-Schnittstelle kompiliert einen Effekt aus einer Funktion oder aus einem Vertex-Shader.
ms.assetid: 2d1dbc63-1eb9-4736-a0b5-7f899c0638be
title: ID3DXEffectCompiler-Schnittstelle (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectCompiler
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c7a16417528d1adbd9ba54f9bd7120057654d14e0ef4bddad829e8f232445069
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119856740"
---
# <a name="id3dxeffectcompiler-interface"></a>ID3DXEffectCompiler-Schnittstelle

Die **ID3DXEffectCompiler-Schnittstelle** kompiliert einen Effekt aus einer Funktion oder einem Vertex-Shader.

## <a name="members"></a>Member

Die **ID3DXEffectCompiler-Schnittstelle** erbt von [**ID3DXBaseEffect.**](id3dxbaseeffect.md) **ID3DXEffectCompiler** verfügt auch über diese Membertypen:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DXEffectCompiler-Schnittstelle** verfügt über diese Methoden.



| Methode                                                      | Beschreibung                                                                                                                                 |
|:------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------|
| [**CompileEffect**](id3dxeffectcompiler--compileeffect.md) | Kompilieren Sie einen Effekt.<br/>                                                                                                               |
| [**CompileShader**](id3dxeffectcompiler--compileshader.md) | Kompiliert einen Shader aus einem Effekt, der eine oder mehrere Funktionen enthält.<br/>                                                            |
| [**GetLiteral**](id3dxeffectcompiler--getliteral.md)       | Ruft einen Literalstatus eines Parameters ab. Ein Literalparameter verfügt über einen Wert, der sich während der Lebensdauer eines Effekts nicht ändert.<br/>      |
| [**SetLiteral**](id3dxeffectcompiler--setliteral.md)       | Umschaltet den Literalstatus eines Parameters. Ein Literalparameter verfügt über einen Wert, der sich während der Lebensdauer eines Effekts nicht ändert.<br/> |



 

## <a name="remarks"></a>Hinweise

Die ID3DXEffectCompiler-Schnittstelle wird durch Aufrufen von [**D3DXCreateEffectCompiler,**](d3dxcreateeffectcompiler.md) [**D3DXCreateEffectCompilerFromFile**](d3dxcreateeffectcompilerfromfile.md)oder [**D3DXCreateEffectCompilerFromResource**](d3dxcreateeffectcompilerfromresource.md)ermittelt.

Der LPD3DXEFFECTCOMPILER-Typ wird als Zeiger auf diese Schnittstelle definiert.


```
typedef interface ID3DXEffectCompiler ID3DXEffectCompiler;
typedef interface ID3DXEffectCompiler *LPD3DXEFFECTCOMPILER;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ID3DXBaseEffect**](id3dxbaseeffect.md)
</dt> <dt>

[Effektschnittstellen](dx9-graphics-reference-effects-interfaces.md)
</dt> <dt>

[**D3DXCreateEffectCompiler**](d3dxcreateeffectcompiler.md)
</dt> <dt>

[**D3DXCreateEffectCompilerFromFile**](d3dxcreateeffectcompilerfromfile.md)
</dt> <dt>

[**D3DXCreateEffectCompilerFromResource**](d3dxcreateeffectcompilerfromresource.md)
</dt> </dl>

 

 




