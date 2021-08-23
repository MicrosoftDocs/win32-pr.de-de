---
title: ID3DX11EffectConstantBuffer SetTextureBuffer-Methode (D3dx11effect.h)
description: Legen Sie einen Texturpuffer fest.
ms.assetid: b8c327e4-52ff-498e-81e9-187e58bbe5d2
keywords:
- SetTextureBuffer-Methode Direct3D 11
- SetTextureBuffer-Methode Direct3D 11, ID3DX11EffectConstantBuffer-Schnittstelle
- ID3DX11EffectConstantBuffer-Schnittstelle Direct3D 11 , SetTextureBuffer-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectConstantBuffer.SetTextureBuffer
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2d71b104d51b8310f2922c25e940cd559e2d47dca695cbe844e7526eb8235fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119046369"
---
# <a name="id3dx11effectconstantbuffersettexturebuffer-method"></a>ID3DX11EffectConstantBuffer::SetTextureBuffer-Methode

Legen Sie einen Texturpuffer fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetTextureBuffer(
   ID3D11ShaderResourceView *pTextureBuffer
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pTextureBuffer* 
</dt> <dd>

Typ: **[ **ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\***

Ein Zeiger auf eine Shader-Ressourcenansicht-Schnittstelle für den Zugriff auf einen Texturpuffer.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Gibt einen der folgenden [Direct3D 11-Rückgabecodes zurück.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Hinweise

> [!Note]  
> Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit. Sie müssen die Quelle Effects 11 verwenden, um Ihre Effekttypanwendung zu erstellen. Weitere Informationen zur Verwendung der Quelle Effects 11 finden Sie unter [Unterschiede zwischen Effekten 10 und Effekten 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Bibliothek<br/> | <dl> <dt>Nicht verfügbar (eine Effects 11-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DX11EffectConstantBuffer](id3dx11effectconstantbuffer.md)
</dt> </dl>

 

 





