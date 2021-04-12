---
title: D3D11Reflect-Funktion
description: Ruft einen Zeiger auf eine reflektionseschnittstelle ab.
ms.assetid: 855097c7-988b-4ab6-90c5-e5dd0bc9e1e0
keywords:
- D3D11Reflect-Funktion (HLSL)
topic_type:
- apiref
api_name:
- D3D11Reflect
api_location:
- D3dcompiler_47.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e54a1f388ebb122398ad33c3a8d942496fa55393
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104132397"
---
# <a name="d3d11reflect-function"></a>D3D11Reflect-Funktion

Ruft einen Zeiger auf eine reflektionseschnittstelle ab.

## <a name="syntax"></a>Syntax

``` syntax
HRESULT D3D11Reflect(
  in  LPCVOID pSrcData,
  in  SIZE_T SrcDataSize,
  out ID3D11ShaderReflection ppReflector
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*pSrcData* \[ in\]
</dt> <dd>

Geben Sie Folgendes ein: **[ **lpcvoid**](/windows/desktop/WinProg/windows-data-types)**

Ein Zeiger auf Quelldaten als kompilierter HLSL-Code.

</dd> <dt>

*Srcdatasize* \[ in\]
</dt> <dd>

Typ: **[ **Größe \_ T**](/windows/desktop/WinProg/windows-data-types)**

Länge von *pSrcData*.

</dd> <dt>

*ppreflector* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection)\*\***

Die Adresse eines Zeigers auf die [**ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection) -Schnittstelle.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](/windows/desktop/WinProg/windows-data-types)**

Gibt einen der Rückgabecodes zurück, die im Thema [Direct3D 11 Return Codes](/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues)beschrieben werden.

## <a name="remarks"></a>Bemerkungen

Die Inline- **D3D11Reflect** -Compilerfunktion ist ein Wrapper für die [**D3DReflect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreflect) -Compilerfunktion. **D3D11Reflect** kann nur eine [**ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection) -Schnittstelle aus einem Shader abrufen. **D3DReflect** kann eine **ID3D11ShaderReflection** -Schnittstelle oder eine Direct3D 10-oder Direct3D 10,1 Reflection-Schnittstelle abrufen, z. b. [**ID3D10ShaderReflection**](/windows/desktop/api/d3d10shader/nn-d3d10shader-id3d10shaderreflection).

Shader-Code enthält Metadaten, die mithilfe der reflektionsapis überprüft werden können.

Der folgende Code zeigt, wie eine [**ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection) -Schnittstelle aus einem Shader abgerufen wird.


```C++
pd3dDevice->CreatePixelShader( pPixelShaderBuffer->GetBufferPointer(),
                               pPixelShaderBuffer->GetBufferSize(), g_pPSClassLinkage, &g_pPixelShader );

ID3D11ShaderReflection* pReflector = NULL; 
D3D11Reflect( pPixelShaderBuffer->GetBufferPointer(), pPixelShaderBuffer->GetBufferSize(), 
            &pReflector);
```



## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DCompiler. INL</dt> </dl>     |
| Bibliothek<br/> | <dl> <dt>D3dcompiler \_ 47. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3dcompiler \_47.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Funktionen](dx-graphics-d3dcompiler-reference-functions.md)
</dt> </dl>

 

