---
description: Eine vom Benutzer implementierte Methode zum Öffnen und Lesen des Inhalts einer \# Shader-Includedatei.
ms.assetid: ad0105f7-042d-4e96-ad4a-1ece08e519af
title: ID3DXInclude::Open-Methode (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXInclude.Open
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: e50b4774f6ed62b1e8a6e6cb85b5732efd878302563958e25e6b9017f9acc58d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987390"
---
# <a name="id3dxincludeopen-method"></a>ID3DXInclude::Open-Methode

Eine vom Benutzer implementierte Methode zum Öffnen und Lesen des Inhalts einer \# Shader-Includedatei.

## <a name="syntax"></a>Syntax


```C++
HRESULT Open(
  [in]  D3DXINCLUDE_TYPE IncludeType,
  [in]  LPCSTR           pFileName,
  [in]  LPCVOID          pParentData,
  [out] LPCVOID          *ppData,
  [out] UINT             *pBytes
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*IncludeType* \[ In\]
</dt> <dd>

Typ: **[ **D3DXINCLUDE \_ TYPE**](./d3dxinclude-type.md)**

Der Speicherort der \# Includedatei. Siehe [**D3DXINCLUDE \_ TYPE**](./d3dxinclude-type.md).

</dd> <dt>

*pFileName* \[ In\]
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Name der \# Includedatei.

</dd> <dt>

*pParentData* \[ In\]
</dt> <dd>

Typ: **[ **LPCVOID**](../winprog/windows-data-types.md)**

Zeiger auf den Container, der die \# Includedatei enthält. Der Compiler kann NULL in *pParentData übergeben.* Weitere Informationen finden Sie im Abschnitt "Suchen nach Includedateien" unter [Kompilieren eines Effekts (Direct3D 11).](../direct3d11/d3d11-graphics-programming-guide-effects-compile.md)

</dd> <dt>

*ppData* \[ out\]
</dt> <dd>

Typ: **[ **LPCVOID**](../winprog/windows-data-types.md)\***

Zeiger auf den zurückgegebenen Puffer, der die Include-Direktiven enthält. Dieser Zeiger bleibt gültig, bis [**ID3DXInclude::Close**](id3dxinclude--close.md) aufgerufen wird.

</dd> <dt>

*pBytes* \[ out\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)\***

Anzahl der in ppData zurückgegebenen Bytes.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Die vom Benutzer implementierte Methode sollte S \_ OK zurückgeben. Wenn der Rückruf beim Lesen der Includedatei fehlschlägt, schlägt die API fehl, die den Aufruf des \# Rückrufs verursacht hat. Folgende Werte sind möglich:

-   Der HLSL-Shader kann nicht mit einer der D3DXCompileShader-Funktionen \* \* \* verwendet werden.
-   Der Assemblyshader kann nicht mit einer der D3DXAssembleShader-Funktionen \* \* \* verwendet werden.
-   Die Auswirkung tritt bei einer der Funktionen D3DXCreateEffect \* \* \* oder D3DXCreateEffectCompiler \* \* \* auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXInclude](id3dxinclude.md)
</dt> <dt>

[**ID3DXInclude::Close**](id3dxinclude--close.md)
</dt> </dl>

 

 
