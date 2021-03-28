---
title: ID3DX11EffectConstantBuffer gettexturebuffer-Methode (D3dx11effect. h)
description: Einen Textur Puffer erhalten.
ms.assetid: 8d09e67c-358e-49ee-8ca4-e1f548b52c3a
keywords:
- Gettexturebuffer-Methode Direct3D 11
- Gettexturebuffer-Methode Direct3D 11, ID3DX11EffectConstantBuffer-Schnittstelle
- ID3DX11EffectConstantBuffer-Schnittstelle Direct3D 11, gettexturebuffer-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectConstantBuffer.GetTextureBuffer
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d03000338c725e71096e57715a49a70b4347b358
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982477"
---
# <a name="id3dx11effectconstantbuffergettexturebuffer-method"></a>ID3DX11EffectConstantBuffer:: gettexturebuffer-Methode

Einen Textur Puffer erhalten.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetTextureBuffer(
   ID3D11ShaderResourceView **ppTextureBuffer
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pptexturebuffer* 
</dt> <dd>

Typ: **[ **ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\*\***

Die Adresse eines Zeigers auf eine Shader-Resource-View-Schnittstelle für den Zugriff auf einen Textur Puffer. Siehe [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Gibt einen der folgenden [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)zurück.

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit. Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen. Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Bibliothek<br/> | <dl> <dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DX11EffectConstantBuffer](id3dx11effectconstantbuffer.md)
</dt> </dl>

 

 





