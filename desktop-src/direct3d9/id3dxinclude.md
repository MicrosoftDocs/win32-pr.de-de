---
description: ID3DXInclude ist eine vom Benutzer implementierte Schnittstelle zum Bereitstellen von Rückrufen für Include-Direktiven \# während der Shaderkompilierung.
ms.assetid: 8e0bfff1-8d6d-4381-b9fd-f5f64f854712
title: ID3DXInclude-Schnittstelle (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXInclude
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: e48ab32894ad1bf4c2f992ab4fff5953b3d98de4afd5e044de0119e056ee8133
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118295180"
---
# <a name="id3dxinclude-interface"></a>ID3DXInclude-Schnittstelle

ID3DXInclude ist eine vom Benutzer implementierte Schnittstelle zum Bereitstellen von Rückrufen für Include-Direktiven \# während der Shaderkompilierung. Jede der Methoden in dieser Schnittstelle muss vom Benutzer implementiert werden, der dann als Rückrufe für die Anwendung verwendet wird, wenn eine der folgenden Bedingungen eintritt:

-   Ein HLSL-Shader, der ein Include enthält, wird durch Aufrufen einer der \# D3DXCompileShader-Funktionen \* \* \* kompiliert.
-   Ein Assemblyshader-Include wird durch Aufrufen einer \# der D3DXAssembleShader-Funktionen \* \* \* zusammengestellt.
-   Ein Effekt, der ein Include enthält, wird durch Aufrufen einer der \# D3DXCreateEffect- oder \* \* \* D3DXCreateEffectCompiler-Funktionen \* \* \* kompiliert.

## <a name="members"></a>Member

Die **ID3DXInclude-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ID3DXInclude** verfügt auch über die folgenden Membertypen:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DXInclude-Schnittstelle** verfügt über diese Methoden.



| Methode                               | Beschreibung                                                                                           |
|:-------------------------------------|:------------------------------------------------------------------------------------------------------|
| [**Schließen**](id3dxinclude--close.md) | Eine vom Benutzer implementierte Methode zum Schließen einer \# Shader-Includedatei.<br/>                             |
| [**Öffnen**](id3dxinclude--open.md)   | Eine vom Benutzer implementierte Methode zum Öffnen und Lesen des Inhalts einer \# Shader-Includedatei.<br/> |



 

## <a name="remarks"></a>Hinweise

Ein Benutzer erstellt eine ID3DXInclude-Schnittstelle, indem er eine Klasse implementiert, die von dieser Schnittstelle ableitung, und alle Schnittstellenmethoden implementiert.

Der LPD3DXINCLUDE-Typ wird als Zeiger auf diese Schnittstelle definiert.


```
typedef interface ID3DXInclude ID3DXInclude;
typedef interface ID3DXInclude *LPD3DXINCLUDE;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Effektschnittstellen](dx9-graphics-reference-effects-interfaces.md)
</dt> </dl>

 

 
