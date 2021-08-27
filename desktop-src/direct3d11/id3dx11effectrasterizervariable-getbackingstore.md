---
title: ID3DX11EffectRasterizerVariable GetBackingStore-Methode (D3dx11effect.h)
description: Sie erhalten einen Zeiger auf eine Variable, die den Rasteriserzustand enthält.
ms.assetid: aff62a6c-bdef-49ad-9492-5db0878f632e
keywords:
- GetBackingStore-Methode Direct3D 11
- GetBackingStore-Methode Direct3D 11, ID3DX11EffectRasterizerVariable-Schnittstelle
- ID3DX11EffectRasterizerVariable-Schnittstelle Direct3D 11 , GetBackingStore-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectRasterizerVariable.GetBackingStore
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80912da541d5d5386da4e9612216db3ce62904bdb32ba262b5a2d1ae773201cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118534686"
---
# <a name="id3dx11effectrasterizervariablegetbackingstore-method"></a>ID3DX11EffectRasterizerVariable::GetBackingStore-Methode

Sie erhalten einen Zeiger auf eine Variable, die den Rasteriserzustand enthält.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetBackingStore(
   UINT                  Index,
   D3D11_RASTERIZER_DESC *pRasterizerDesc
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Index* 
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Indizieren Sie in ein Array von Rasteriserzustandsbeschreibungen. Wenn nur eine Rasteriservariable im Effekt ist, verwenden Sie 0.

</dd> <dt>

*pRasterizerDesc* 
</dt> <dd>

Typ: **[ **D3D11 \_ RASTERIZER \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_rasterizer_desc)\***

Ein Zeiger auf eine Rasteriserzustandsbeschreibung (siehe [**D3D11 \_ RASTERIZER \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_rasterizer_desc)).

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

[ID3DX11EffectRasterizerVariable](id3dx11effectrasterizervariable.md)
</dt> </dl>

 

