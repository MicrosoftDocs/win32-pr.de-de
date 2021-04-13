---
description: Die ID3DXEffectCompiler-Schnittstelle kompiliert einen Effekt aus einer Funktion oder einem Scheitelpunkt-Shader.
ms.assetid: 2d1dbc63-1eb9-4736-a0b5-7f899c0638be
title: ID3DXEffectCompiler-Schnittstelle (D3DX9Effect. h)
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
ms.openlocfilehash: d69cbcd6c14bb3a874a382f46fe5aee6619b8168
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354346"
---
# <a name="id3dxeffectcompiler-interface"></a>ID3DXEffectCompiler-Schnittstelle

Die **ID3DXEffectCompiler** -Schnittstelle kompiliert einen Effekt aus einer Funktion oder einem Scheitelpunkt-Shader.

## <a name="members"></a>Member

Die **ID3DXEffectCompiler** -Schnittstelle erbt von [**ID3DXBaseEffect**](id3dxbaseeffect.md). **ID3DXEffectCompiler** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DXEffectCompiler** -Schnittstelle verfügt über diese Methoden.



| Methode                                                      | BESCHREIBUNG                                                                                                                                 |
|:------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------|
| [**Compileeffect**](id3dxeffectcompiler--compileeffect.md) | Kompilieren eines Effekts.<br/>                                                                                                               |
| [**Compileshader**](id3dxeffectcompiler--compileshader.md) | Kompiliert einen Shader aus einem Effekt, der eine oder mehrere Funktionen enthält.<br/>                                                            |
| [**Getliteral**](id3dxeffectcompiler--getliteral.md)       | Ruft den literalstatus eines Parameters ab. Ein literalparameter weist einen Wert auf, der sich während der Lebensdauer eines Effekts nicht ändert.<br/>      |
| [**Setliterale**](id3dxeffectcompiler--setliteral.md)       | Schaltet den literalstatus eines Parameters um. Ein literalparameter weist einen Wert auf, der sich während der Lebensdauer eines Effekts nicht ändert.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Die ID3DXEffectCompiler-Schnittstelle wird durch Aufrufen von [**D3DXCreateEffectCompiler**](d3dxcreateeffectcompiler.md), [**D3DXCreateEffectCompilerFromFile**](d3dxcreateeffectcompilerfromfile.md)oder [**D3DXCreateEffectCompilerFromResource**](d3dxcreateeffectcompilerfromresource.md)abgerufen.

Der LPD3DXEFFECTCOMPILER-Typ wird als Zeiger auf diese Schnittstelle definiert.


```
typedef interface ID3DXEffectCompiler ID3DXEffectCompiler;
typedef interface ID3DXEffectCompiler *LPD3DXEFFECTCOMPILER;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ID3DXBaseEffect**](id3dxbaseeffect.md)
</dt> <dt>

[Effekt Schnittstellen](dx9-graphics-reference-effects-interfaces.md)
</dt> <dt>

[**D3DXCreateEffectCompiler**](d3dxcreateeffectcompiler.md)
</dt> <dt>

[**D3DXCreateEffectCompilerFromFile**](d3dxcreateeffectcompilerfromfile.md)
</dt> <dt>

[**D3DXCreateEffectCompilerFromResource**](d3dxcreateeffectcompilerfromresource.md)
</dt> </dl>

 

 




