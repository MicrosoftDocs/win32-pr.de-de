---
title: ID3DX11EffectRenderTargetViewVariable GetRenderTarget-Methode (D3dx11effect.h)
description: Abrufen eines Renderziels.
ms.assetid: 96984d0a-b8f4-444a-9683-3c37d8274d75
keywords:
- GetRenderTarget-Methode Direct3D 11
- GetRenderTarget-Methode Direct3D 11 , ID3DX11EffectRenderTargetViewVariable-Schnittstelle
- ID3DX11EffectRenderTargetViewVariable-Schnittstelle Direct3D 11 , GetRenderTarget-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectRenderTargetViewVariable.GetRenderTarget
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 035ea8f82ece3ca030099eb949f2fb08229c0a9c9b068f45237403b86cf92955
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045868"
---
# <a name="id3dx11effectrendertargetviewvariablegetrendertarget-method"></a>ID3DX11EffectRenderTargetViewVariable::GetRenderTarget-Methode

Abrufen eines Renderziels.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetRenderTarget(
   ID3D11RenderTargetView **ppResource
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppResource* 
</dt> <dd>

Typ: **[ **ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview)\*\***

Die Adresse eines Zeigers auf eine Schnittstelle für render-target-view. Siehe [**ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview).

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

[ID3DX11EffectRenderTargetViewVariable](id3dx11effectrendertargetviewvariable.md)
</dt> </dl>

 

 





