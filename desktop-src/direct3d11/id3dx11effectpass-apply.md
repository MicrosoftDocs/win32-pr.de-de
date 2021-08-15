---
title: ID3DX11EffectPass Apply-Methode (D3dx11effect.h)
description: Legen Sie den Zustand fest, der in einem Pass an das Gerät enthalten ist.
ms.assetid: d67fe968-bfb2-4f3a-b393-3f72f680211f
keywords:
- Anwenden der Direct3D 11-Methode
- Apply method Direct3D 11 , ID3DX11EffectPass interface (Methode anwenden Direct3D 11, ID3DX11EffectPass-Schnittstelle)
- ID3DX11EffectPass-Schnittstelle Direct3D 11 , Methode anwenden
topic_type:
- apiref
api_name:
- ID3DX11EffectPass.Apply
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e18d3d546a1bf6381103b7d38f7467fe4d66ed8e0d9702afcf7640197abb5c0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119046048"
---
# <a name="id3dx11effectpassapply-method"></a>ID3DX11EffectPass::Apply-Methode

Legen Sie den Zustand fest, der in einem Pass an das Gerät enthalten ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT Apply(
   UINT                Flags,
   ID3D11DeviceContext *pContext
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Flags* 
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Nicht verwendet.

</dd> <dt>

*pContext* 
</dt> <dd>

Typ: **[ **ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***

Der [**ID3D11DeviceContext,**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) auf den der Pass angewendet werden soll.

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

[ID3DX11EffectPass](id3dx11effectpass.md)
</dt> </dl>

 

