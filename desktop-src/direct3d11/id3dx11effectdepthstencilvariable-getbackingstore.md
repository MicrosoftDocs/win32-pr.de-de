---
title: ID3DX11EffectDepthStencilVariable GetBackingStore-Methode (D3dx11effect.h)
description: Sie erhalten einen Zeiger auf eine Variable, die den Tiefen-Schablonenzustand enthält.
ms.assetid: 6aeed5ac-f0ee-4e8c-b87b-022f58c9094c
keywords:
- GetBackingStore-Methode Direct3D 11
- GetBackingStore-Methode Direct3D 11, ID3DX11EffectDepthStencilVariable-Schnittstelle
- ID3DX11EffectDepthStencilVariable-Schnittstelle Direct3D 11 , GetBackingStore-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectDepthStencilVariable.GetBackingStore
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfe2387b6cc071e9146176e6cf8b84da1870c0671572f184fea7e6cbadef03d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989840"
---
# <a name="id3dx11effectdepthstencilvariablegetbackingstore-method"></a>ID3DX11EffectDepthStencilVariable::GetBackingStore-Methode

Sie erhalten einen Zeiger auf eine Variable, die den Tiefen-Schablonenzustand enthält.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetBackingStore(
   UINT                     Index,
   D3D11_DEPTH_STENCIL_DESC *pDepthStencilDesc
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Index* 
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Indizieren Sie in ein Array von Beschreibungen des Tiefen-Schablonenzustands. Wenn es nur eine Tiefen-Schablonenvariable gibt, verwenden Sie 0.

</dd> <dt>

*pDepthStencilDesc* 
</dt> <dd>

Typ: **[ **D3D11 \_ DEPTH \_ STENCIL \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc)\***

Ein Zeiger auf eine Beschreibung des Tiefen-Schablonenzustands (siehe [**D3D11 \_ DEPTH \_ STENCIL \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc)).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Gibt einen der folgenden [Direct3D 11-Rückgabecodes zurück.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Hinweise

Effektvariablen werden im Arbeitsspeicher im Hintergrundspeicher gespeichert. Wenn eine Technik angewendet wird, werden die Werte im Hintergrundspeicher auf das Gerät kopiert. Speicherdaten können verwendet werden, um die Variable bei Bedarf neu zu erstellen.

> [!Note]  
> Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit. Sie müssen die Quelle Effects 11 verwenden, um Ihre Effekttypanwendung zu erstellen. Weitere Informationen zur Verwendung der Quelle Effects 11 finden Sie unter [Unterschiede zwischen Effekten 10 und Effekten 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Bibliothek<br/> | <dl> <dt>Nicht verfügbar (eine Effects 11-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DX11EffectDepthStencilVariable](id3dx11effectdepthstencilvariable.md)
</dt> </dl>

 

