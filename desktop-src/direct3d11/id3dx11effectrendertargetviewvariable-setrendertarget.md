---
title: ID3DX11EffectRenderTargetViewVariable SetRenderTarget-Methode (D3dx11effect.h)
description: Legen Sie ein Renderziel fest.
ms.assetid: caac7190-4f58-4a8e-9764-b6120ac14856
keywords:
- SetRenderTarget-Methode Direct3D 11
- SetRenderTarget-Methode Direct3D 11 , ID3DX11EffectRenderTargetViewVariable-Schnittstelle
- ID3DX11EffectRenderTargetViewVariable-Schnittstelle Direct3D 11, SetRenderTarget-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectRenderTargetViewVariable.SetRenderTarget
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69bd36ddab704ab7ac78d78e7e7cf0c2262794df76730bc6f9019662c292abbc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045848"
---
# <a name="id3dx11effectrendertargetviewvariablesetrendertarget-method"></a>ID3DX11EffectRenderTargetViewVariable::SetRenderTarget-Methode

Legen Sie ein Renderziel fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetRenderTarget(
   ID3D11RenderTargetView *pResource
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pResource* 
</dt> <dd>

Typ: **[ **ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview)\***

Ein Zeiger auf eine Schnittstelle für render-target-view. Siehe [**ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview).

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

 

 





