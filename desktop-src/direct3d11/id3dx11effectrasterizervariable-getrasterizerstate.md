---
title: ID3DX11EffectRasterizerVariable GetRasterizerState-Methode (D3dx11effect.h)
description: Abrufen eines Zeigers auf eine Rasterizerschnittstelle.
ms.assetid: 4b8515e0-b79a-4572-9142-07c50a8839b8
keywords:
- GetRasterizerState-Methode Direct3D 11
- GetRasterizerState-Methode Direct3D 11 , ID3DX11EffectRasterizerVariable-Schnittstelle
- ID3DX11EffectRasterizerVariable-Schnittstelle Direct3D 11 , GetRasterizerState-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectRasterizerVariable.GetRasterizerState
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94dbd6b45b14e8499fada4c1c5eb32b9bbd55b1dad843b05cf52a9318737cb9e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045878"
---
# <a name="id3dx11effectrasterizervariablegetrasterizerstate-method"></a>ID3DX11EffectRasterizerVariable::GetRasterizerState-Methode

Abrufen eines Zeigers auf eine Rasterizerschnittstelle.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetRasterizerState(
   UINT                  Index,
   ID3D11RasterizerState **ppRasterizerState
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Index* 
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Index in ein Array von Rasterizerschnittstellen. Wenn nur eine Rasterizerschnittstelle vorhanden ist, verwenden Sie 0.

</dd> <dt>

*ppRasterizerState* 
</dt> <dd>

Typ: **[ **ID3D11RasterizerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rasterizerstate)\*\***

Die Adresse eines Zeigers auf eine Rasterizerschnittstelle (siehe [**ID3D11RasterizerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rasterizerstate)).

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

[ID3DX11EffectRasterizerVariable](id3dx11effectrasterizervariable.md)
</dt> </dl>

 

