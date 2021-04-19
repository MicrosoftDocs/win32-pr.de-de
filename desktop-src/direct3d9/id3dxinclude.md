---
description: ID3DXInclude ist eine vom Benutzer implementierte Schnittstelle, um Rückrufe für \# Includedirektiven während der shaderkompilierung bereitzustellen.
ms.assetid: 8e0bfff1-8d6d-4381-b9fd-f5f64f854712
title: ID3DXInclude-Schnittstelle (D3DX9Shader. h)
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
ms.openlocfilehash: d4b0a34eb5b4c3ab20a57a5089de1d6d1ebbdf51
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106369331"
---
# <a name="id3dxinclude-interface"></a>ID3DXInclude-Schnittstelle

ID3DXInclude ist eine vom Benutzer implementierte Schnittstelle, um Rückrufe für \# Includedirektiven während der shaderkompilierung bereitzustellen. Jede der Methoden in dieser Schnittstelle muss vom Benutzer implementiert werden, der dann als Rückrufe für die Anwendung verwendet wird, wenn einer der folgenden Punkte zutrifft:

-   Ein HLSL-Shader, der eine include-Datei enthält, \# wird durch Aufrufen einer der D3DXCompileShader- \* \* \* Funktionen kompiliert.
-   Ein assemblyshader \# wird durch Aufrufen einer der D3DXAssembleShader-Funktionen zusammengestellt \* \* \* .
-   Ein Effekt, der einen Include-Wert enthält, \# wird durch den Aufruf einer der D3DXCreateEffect- \* \* \* oder D3DXCreateEffectCompiler- \* \* \* Funktionen kompiliert.

## <a name="members"></a>Member

Die **ID3DXInclude** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **ID3DXInclude** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DXInclude** -Schnittstelle verfügt über diese Methoden.



| Methode                               | BESCHREIBUNG                                                                                           |
|:-------------------------------------|:------------------------------------------------------------------------------------------------------|
| [**Schließen**](id3dxinclude--close.md) | Eine vom Benutzer implementierte Methode zum Schließen einer Shader- \# Includedatei.<br/>                             |
| [**Eren**](id3dxinclude--open.md)   | Eine vom Benutzer implementierte Methode zum Öffnen und Lesen des Inhalts einer-Shader- \# Includedatei.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Ein Benutzer erstellt eine ID3DXInclude-Schnittstelle, indem er eine Klasse implementiert, die von dieser Schnittstelle abgeleitet wird, und alle Schnittstellen Methoden implementiert.

Der LPD3DXINCLUDE-Typ wird als Zeiger auf diese Schnittstelle definiert.


```
typedef interface ID3DXInclude ID3DXInclude;
typedef interface ID3DXInclude *LPD3DXINCLUDE;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Effekt Schnittstellen](dx9-graphics-reference-effects-interfaces.md)
</dt> </dl>

 

 
