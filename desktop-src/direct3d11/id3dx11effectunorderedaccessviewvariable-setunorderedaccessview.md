---
title: ID3DX11EffectUnorderedAccessViewVariable SetUnorderedAccessView-Methode (D3dx11effect.h)
description: Legen Sie eine ungeordnete Zugriffsansicht fest.
ms.assetid: a147879c-c5cf-4453-b27f-8716cb33962b
keywords:
- SetUnorderedAccessView-Methode Direct3D 11
- SetUnorderedAccessView-Methode Direct3D 11, ID3DX11EffectUnorderedAccessViewVariable-Schnittstelle
- ID3DX11EffectUnorderedAccessViewVariable-Schnittstelle Direct3D 11 , SetUnorderedAccessView-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectUnorderedAccessViewVariable.SetUnorderedAccessView
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d95dc15b0b79475cf7b8a731df291c73cb193db44fdc5bb917606dd916d6757
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119565740"
---
# <a name="id3dx11effectunorderedaccessviewvariablesetunorderedaccessview-method"></a>ID3DX11EffectUnorderedAccessViewVariable::SetUnorderedAccessView-Methode

Legen Sie eine ungeordnete Zugriffsansicht fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetUnorderedAccessView(
   ID3D11UnorderedAccessView *pResource
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pResource* 
</dt> <dd>

Typ: **[ **ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview)\***

Zeiger auf eine [**ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview).

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

[ID3DX11EffectUnorderedAccessViewVariable](id3dx11effectunorderedaccessviewvariable.md)
</dt> </dl>

 

 





