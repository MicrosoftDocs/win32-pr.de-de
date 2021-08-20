---
title: ID3DX11EffectBlendVariable SetBlendState-Methode (D3dx11effect.h)
description: Legt den Überblendungszustand eines Effekts fest.
ms.assetid: 46100721-65a3-46de-aa22-3e7e2fb7b960
keywords:
- SetBlendState-Methode Direct3D 11
- SetBlendState-Methode Direct3D 11, ID3DX11EffectBlendVariable-Schnittstelle
- ID3DX11EffectBlendVariable-Schnittstelle Direct3D 11, SetBlendState-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectBlendVariable.SetBlendState
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87a8f945faaf7f07846ea58b91378bbf2e6c06eeb1c3d0d041a6e0a71e2e9ea7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119046498"
---
# <a name="id3dx11effectblendvariablesetblendstate-method"></a>ID3DX11EffectBlendVariable::SetBlendState-Methode

Legt den Überblendungszustand eines Effekts fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetBlendState(
   UINT             Index,
   ID3D11BlendState *pBlendState
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Index* 
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Indizieren sie in ein Array von Blendzustandsschnittstellen. Wenn nur eine Blendzustandsschnittstelle verfügbar ist, verwenden Sie 0.

</dd> <dt>

*pBlendState* 
</dt> <dd>

Typ: **[ **ID3D11BlendState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11blendstate)\***

Ein Zeiger auf eine [**ID3D11BlendState-Schnittstelle,**](/windows/desktop/api/D3D11/nn-d3d11-id3d11blendstate) die den zu setzenden Blend-Zustand enthält.

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

[ID3DX11EffectBlendVariable](id3dx11effectblendvariable.md)
</dt> </dl>

 

