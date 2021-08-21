---
title: ID3DX11EffectShaderVariable GetDomainShader-Methode (D3dx11effect.h)
description: Abrufen eines Domänen-Shaders.
ms.assetid: fd95a4f0-7df3-4098-843f-0a1e22209603
keywords:
- GetDomainShader-Methode Direct3D 11
- GetDomainShader-Methode Direct3D 11 , ID3DX11EffectShaderVariable-Schnittstelle
- ID3DX11EffectShaderVariable-Schnittstelle Direct3D 11 , GetDomainShader-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderVariable.GetDomainShader
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e66bb99f170e6b638587d7da5a8d3cc57a34d3cab6bb04968b049d39dcb09c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118533296"
---
# <a name="id3dx11effectshadervariablegetdomainshader-method"></a>ID3DX11EffectShaderVariable::GetDomainShader-Methode

Abrufen eines Domänen-Shaders.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetDomainShader(
   UINT               ShaderIndex,
   ID3D11DomainShader **ppPS
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ShaderIndex* 
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Index des Domänen-Shaders.

</dd> <dt>

*Öpp* 
</dt> <dd>

Typ: **[ **ID3D11DomainShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11domainshader)\*\***

Zeiger auf einen [**ID3D11DomainShader-Zeiger,**](/windows/win32/api/d3d11/nn-d3d11-id3d11domainshader) der bei der Rückgabe auf den Domänenshader festgelegt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Gibt einen der folgenden [Direct3D 11-Rückgabecodes zurück.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Hinweise

> [!Note]  
> Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte zur Verfügung. Sie müssen die Effects 11-Quelle verwenden, um ihre Effekte-Typ-Anwendung zu erstellen. Weitere Informationen zur Verwendung der Quelle Effects 11 finden Sie unter [Unterschiede zwischen Effekten 10 und Effekten 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Bibliothek<br/> | <dl> <dt>N/A (Eine Effects 11-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DX11EffectShaderVariable](id3dx11effectshadervariable.md)
</dt> </dl>

 

