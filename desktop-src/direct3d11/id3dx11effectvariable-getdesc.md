---
title: ID3DX11EffectVariable GetDesc-Methode (D3dx11effect.h)
description: Hier erhalten Sie eine Beschreibung.
ms.assetid: bf6339d7-8eb0-44da-893e-c805309a3cd3
keywords:
- GetDesc-Methode Direct3D 11
- GetDesc-Methode Direct3D 11, ID3DX11EffectVariable-Schnittstelle
- ID3DX11EffectVariable-Schnittstelle Direct3D 11 , GetDesc-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.GetDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da4c4ac66c8cafee3636491513ba7a70c19be752c6d0769902bb91e771487177
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118531116"
---
# <a name="id3dx11effectvariablegetdesc-method"></a>ID3DX11EffectVariable::GetDesc-Methode

Hier erhalten Sie eine Beschreibung.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetDesc(
   D3DX11_EFFECT_VARIABLE_DESC *pDesc
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pDesc* 
</dt> <dd>

Typ: **[ **D3DX11 \_ EFFECT \_ VARIABLE \_ DESC**](d3dx11-effect-variable-desc.md)\***

Ein Zeiger auf eine Beschreibung einer Effektvariablen (siehe [**D3DX11 \_ EFFECT \_ VARIABLE \_ DESC**](d3dx11-effect-variable-desc.md)).

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

[ID3DX11EffectVariable](id3dx11effectvariable.md)
</dt> </dl>

 

 





