---
title: ID3DX11EffectDepthStencilViewVariable GetDepthStencil-Methode (D3dx11effect.h)
description: Abrufen einer Tiefenschablonenansichtsressource.
ms.assetid: 7d94d98b-7070-41ee-9a9d-fe848f8914f2
keywords:
- GetDepthStencil-Methode Direct3D 11
- GetDepthStencil-Methode Direct3D 11 , ID3DX11EffectDepthStencilViewVariable-Schnittstelle
- ID3DX11EffectDepthStencilViewVariable-Schnittstelle Direct3D 11 , GetDepthStencil-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectDepthStencilViewVariable.GetDepthStencil
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d31b5a947afc9a1b92349b20bc5d075599a16d12abae0ac7d375e8bc0a0de89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989740"
---
# <a name="id3dx11effectdepthstencilviewvariablegetdepthstencil-method"></a>ID3DX11EffectDepthStencilViewVariable::GetDepthStencil-Methode

Abrufen einer Tiefenschablonenansichtsressource.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetDepthStencil(
   ID3D11DepthStencilView **ppResource
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppResource* 
</dt> <dd>

Typ: **[ **ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview)\*\***

Die Adresse eines Zeigers auf eine Tiefenschablonenansichtsschnittstelle. Siehe [**ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview).

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

[ID3DX11EffectDepthStencilViewVariable](id3dx11effectdepthstencilviewvariable.md)
</dt> </dl>

 

 





