---
title: ID3DX11EffectConstantBuffer settexturebuffer-Methode (D3dx11effect. h)
description: Legen Sie einen Textur Puffer fest.
ms.assetid: b8c327e4-52ff-498e-81e9-187e58bbe5d2
keywords:
- Settexturebuffer-Methode Direct3D 11
- Settexturebuffer-Methode Direct3D 11, ID3DX11EffectConstantBuffer-Schnittstelle
- ID3DX11EffectConstantBuffer-Schnittstelle Direct3D 11, settexturebuffer-Methode
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
ms.openlocfilehash: 736ec4c5f0125dfc37925d67875cf97c5441117c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982161"
---
# <a name="id3dx11effectconstantbuffersettexturebuffer-method"></a>ID3DX11EffectConstantBuffer:: settexturebuffer-Methode

Legen Sie einen Textur Puffer fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetTextureBuffer(
   ID3D11ShaderResourceView *pTextureBuffer
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ptexturebuffer* 
</dt> <dd>

Typ: **[ **ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\***

Ein Zeiger auf eine Shader-Resource-View-Schnittstelle für den Zugriff auf einen Textur Puffer.

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

 

 





