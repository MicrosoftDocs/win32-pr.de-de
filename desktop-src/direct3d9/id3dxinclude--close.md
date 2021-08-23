---
description: Eine vom Benutzer implementierte Methode zum Schließen einer \# Shader-Includedatei.
ms.assetid: de54ce56-3884-443a-9879-4e7290bcfb8d
title: ID3DXInclude::Close-Methode (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXInclude.Close
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 32df78aedcf4e7e229eec8c9648c82c86f6fea9f4c7176b8780cee67ccf49fcb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987400"
---
# <a name="id3dxincludeclose-method"></a>ID3DXInclude::Close-Methode

Eine vom Benutzer implementierte Methode zum Schließen einer \# Shader-Includedatei.

## <a name="syntax"></a>Syntax


```C++
HRESULT Close(
  [in] LPCVOID pData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pData* \[ In\]
</dt> <dd>

Typ: **[ **LPCVOID**](../winprog/windows-data-types.md)**

Zeiger auf den zurückgegebenen Puffer, der die Include-Direktiven enthält. Dies ist der Zeiger, der vom entsprechenden [**ID3DXInclude::Open-Aufruf zurückgegeben**](id3dxinclude--open.md) wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Die vom Benutzer implementierte Methode sollte S \_ OK zurückgeben. Wenn der Rückruf beim Lesen der Includedatei fehlschlägt, schlägt die API fehl, die den Aufruf des \# Rückrufs verursacht hat. Folgende Werte sind möglich:

-   Der HLSL-Shader kann nicht mit einer der D3DXCompileShader-Funktionen \* \* \* verwendet werden.
-   Der Assemblyshader kann nicht mit einer der D3DXAssembleShader-Funktionen \* \* \* verwendet werden.
-   Die Auswirkung tritt bei einer der Funktionen D3DXCreateEffect \* \* \* oder D3DXCreateEffectCompiler \* \* \* auf.

## <a name="remarks"></a>Hinweise

Wenn [**ID3DXInclude::Open**](id3dxinclude--open.md) erfolgreich war, wird **ID3DXInclude::Close** garantiert aufgerufen, bevor die API, die diese Schnittstelle verwendet, zurückgegeben wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXInclude](id3dxinclude.md)
</dt> <dt>

[**ID3DXInclude::Open**](id3dxinclude--open.md)
</dt> </dl>

 

 
