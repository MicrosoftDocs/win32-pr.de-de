---
title: ID3DX11EffectRasterizerVariable SetRasterizerState-Methode (D3dx11effect.h)
description: Legt den Rasterizerzustand fest.
ms.assetid: b2cd93fb-77bb-4a39-b686-7b8f683c9172
keywords:
- SetRasterizerState-Methode Direct3D 11
- SetRasterizerState-Methode Direct3D 11 , ID3DX11EffectRasterizerVariable-Schnittstelle
- ID3DX11EffectRasterizerVariable-Schnittstelle Direct3D 11 , SetRasterizerState-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectRasterizerVariable.SetRasterizerState
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2da95b99a3707b9fd9d05e9343e36a095cf3d6a346180df69ad6ecd3f749febd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118534328"
---
# <a name="id3dx11effectrasterizervariablesetrasterizerstate-method"></a>ID3DX11EffectRasterizerVariable::SetRasterizerState-Methode

Legt den Rasterizerzustand fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetRasterizerState(
   UINT                  Index,
   ID3D11RasterizerState *pRasterizerState
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Index* 
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Index in ein Array von Rasterizerschnittstellen. Wenn nur eine Rasterizerschnittstelle vorhanden ist, verwenden Sie 0.

</dd> <dt>

*pRasterizerState* 
</dt> <dd>

Typ: **[ **ID3D11RasterizerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rasterizerstate)\***

Zeiger auf eine [**ID3D11RasterizerState-Schnittstelle.**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rasterizerstate)

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



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DX11EffectRasterizerVariable](id3dx11effectrasterizervariable.md)
</dt> </dl>

 

