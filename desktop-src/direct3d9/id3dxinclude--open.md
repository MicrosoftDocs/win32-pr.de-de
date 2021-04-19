---
description: Eine vom Benutzer implementierte Methode zum Öffnen und Lesen des Inhalts einer-Shader- \# Includedatei.
ms.assetid: ad0105f7-042d-4e96-ad4a-1ece08e519af
title: 'ID3DXInclude:: Open-Methode (D3DX9Shader. h)'
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
ms.openlocfilehash: 313b3f4845f9a46f758a40b6b315cc5b5eeecb29
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355231"
---
# <a name="id3dxincludeopen-method"></a>ID3DXInclude:: Open-Methode

Eine vom Benutzer implementierte Methode zum Öffnen und Lesen des Inhalts einer-Shader- \# Includedatei.

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

*IncludeType* \[ in\]
</dt> <dd>

Type: **[ **D3DXINCLUDE- \_ Typ**](./d3dxinclude-type.md)**

Der Speicherort der \# Includedatei. Siehe [**D3DXINCLUDE \_ Type**](./d3dxinclude-type.md).

</dd> <dt>

*pfilename* \[ in\]
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Der Name der \# Includedatei.

</dd> <dt>

*pparser-Daten* \[ in\]
</dt> <dd>

Geben Sie Folgendes ein: **[ **lpcvoid**](../winprog/windows-data-types.md)**

Zeiger auf den Container, der die \# Includedatei enthält. Der Compiler kann NULL in *pparameentdata* übergeben. Weitere Informationen finden Sie im Abschnitt "Suchen nach Includedateien" unter [Kompilieren eines Effekts (Direct3D 11)](../direct3d11/d3d11-graphics-programming-guide-effects-compile.md).

</dd> <dt>

*ppData* \[ vorgenommen\]
</dt> <dd>

Geben Sie Folgendes ein: **[ **lpcvoid**](../winprog/windows-data-types.md)\***

Ein Zeiger auf den zurückgegebenen Puffer, der die include-Direktiven enthält. Dieser Zeiger bleibt gültig, bis [**ID3DXInclude:: Close**](id3dxinclude--close.md) aufgerufen wird.

</dd> <dt>

*Pbytes* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)\***

Anzahl der in ppData zurückgegebenen Bytes.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Die vom Benutzer implementierte Methode sollte S \_ OK zurückgeben. Wenn beim Lesen der Includedatei der Rückruf fehlschlägt \# , schlägt die API fehl, die den Aufruf des Rückrufs bewirkt hat. Folgende Werte sind möglich:

-   Der HLSL-Shader erzeugt eine der D3DXCompileShader- \* \* \* Funktionen nicht.
-   Der assemblyshader führt einen der D3DXAssembleShader- \* \* \* Funktionen aus.
-   Der Effekt führt nicht zu einer der D3DXCreateEffect- \* \* \* oder D3DXCreateEffectCompiler- \* \* \* Funktionen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXInclude](id3dxinclude.md)
</dt> <dt>

[**ID3DXInclude:: Close**](id3dxinclude--close.md)
</dt> </dl>

 

 
