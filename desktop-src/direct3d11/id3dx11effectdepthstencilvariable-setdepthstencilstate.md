---
title: ID3DX11EffectDepthStencilVariable SetDepthStencilState-Methode (D3dx11effect.h)
description: Legt den Tiefen schablonenzustand fest.
ms.assetid: 4ece246f-4466-4790-8f38-450b67fff7c6
keywords:
- SetDepthStencilState-Methode Direct3D 11
- SetDepthStencilState-Methode Direct3D 11, ID3DX11EffectDepthStencilVariable-Schnittstelle
- ID3DX11EffectDepthStencilVariable-Schnittstelle Direct3D 11 , SetDepthStencilState-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectDepthStencilVariable.SetDepthStencilState
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d974a3016da96721a70de1e38d5b985402db9c7bd2e6d42495143fdd468295f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989812"
---
# <a name="id3dx11effectdepthstencilvariablesetdepthstencilstate-method"></a>ID3DX11EffectDepthStencilVariable::SetDepthStencilState-Methode

Legt den Tiefen schablonenzustand fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetDepthStencilState(
   UINT                    Index,
   ID3D11DepthStencilState *pDepthStencilState
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Index* 
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Indizieren Sie in ein Array von Tiefen-Schablonenschnittstellen. Wenn es nur eine Tiefen-Schablonenschnittstelle gibt, verwenden Sie 0.

</dd> <dt>

*pDepthStencilState* 
</dt> <dd>

Typ: **[ **ID3D11DepthStencilState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilstate)\***

Zeiger auf eine [**ID3D11DepthStencilState-Schnittstelle,**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilstate) die den neuen Tiefen-Schablonenzustand enthält.

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



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DX11EffectDepthStencilVariable](id3dx11effectdepthstencilvariable.md)
</dt> </dl>

 

