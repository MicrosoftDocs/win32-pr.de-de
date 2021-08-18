---
title: D3D11Reflect-Funktion
description: Ruft einen Zeiger auf eine Reflektionsschnittstelle ab.
ms.assetid: 855097c7-988b-4ab6-90c5-e5dd0bc9e1e0
keywords:
- D3D11Reflect-Funktion HLSL
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
ms.openlocfilehash: 44b980d955dcd37197c8d8ed05a6602025d1e21731ca6d22302b76cc2f2e53da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986880"
---
# <a name="d3d11reflect-function"></a>D3D11Reflect-Funktion

Ruft einen Zeiger auf eine Reflektionsschnittstelle ab.

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

*pSrcData* \[ In\]
</dt> <dd>

Typ: **[ **LPCVOID**](/windows/desktop/WinProg/windows-data-types)**

Ein Zeiger auf Quelldaten als kompilierten HLSL-Code.

</dd> <dt>

*SrcDataSize* \[ In\]
</dt> <dd>

Typ: **[ **SIZE \_ T**](/windows/desktop/WinProg/windows-data-types)**

Länge von *pSrcData.*

</dd> <dt>

*ppReflector* \[ out\]
</dt> <dd>

Typ: **[ **ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection)\*\***

Die Adresse eines Zeigers auf die [**ID3D11ShaderReflection-Schnittstelle.**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](/windows/desktop/WinProg/windows-data-types)**

Gibt einen der Rückgabecodes zurück, die im Thema [Direct3D 11 Return Codes beschrieben sind.](/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues)

## <a name="remarks"></a>Hinweise

Die **Inlinecompilerfunktion D3D11Reflect** ist ein Wrapper für die [**D3DReflect-Compilerfunktion.**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreflect) **D3D11Reflect kann** nur eine [**ID3D11ShaderReflection-Schnittstelle**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection) aus einem Shader abrufen. **D3DReflect** kann eine **ID3D11ShaderReflection-Schnittstelle** oder eine Direct3D 10- oder Direct3D 10.1-Reflektionsschnittstelle abrufen, z. B. [**ID3D10ShaderReflection**](/windows/desktop/api/d3d10shader/nn-d3d10shader-id3d10shaderreflection).

Shadercode enthält Metadaten, die mithilfe der Reflektions-APIs überprüft werden können.

Der folgende Code zeigt, wie sie eine [**ID3D11ShaderReflection-Schnittstelle**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection) aus einem Shader abruft.


```C++
pd3dDevice->CreatePixelShader( pPixelShaderBuffer->GetBufferPointer(),
                               pPixelShaderBuffer->GetBufferSize(), g_pPSClassLinkage, &g_pPixelShader );

ID3D11ShaderReflection* pReflector = NULL; 
D3D11Reflect( pPixelShaderBuffer->GetBufferPointer(), pPixelShaderBuffer->GetBufferSize(), 
            &pReflector);
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DCompiler.inl</dt> </dl>     |
| Bibliothek<br/> | <dl> <dt>D3dcompiler \_ 47.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3dcompiler \_47.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Funktionen](dx-graphics-d3dcompiler-reference-functions.md)
</dt> </dl>

 

