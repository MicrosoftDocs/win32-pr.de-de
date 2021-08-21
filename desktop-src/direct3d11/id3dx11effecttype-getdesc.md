---
title: ID3DX11EffectType GetDesc-Methode (D3dx11effect.h)
description: Hier erhalten Sie eine Beschreibung des Effekttyps.
ms.assetid: 08a8a1b6-fe2d-431b-a0e4-d628f0ceb1a0
keywords:
- GetDesc-Methode Direct3D 11
- GetDesc-Methode Direct3D 11, ID3DX11EffectType-Schnittstelle
- ID3DX11EffectType-Schnittstelle Direct3D 11 , GetDesc-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectType.GetDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 381f885a15dede6a500e82b08a1f24e4f0542ffa46211e5b68ef7f73f40d0f0b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119460780"
---
# <a name="id3dx11effecttypegetdesc-method"></a>ID3DX11EffectType::GetDesc-Methode

Hier erhalten Sie eine Beschreibung des Effekttyps.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetDesc(
   D3DX11_EFFECT_TYPE_DESC *pDesc
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pDesc* 
</dt> <dd>

Typ: **[ **D3DX11 \_ EFFECT \_ TYPE \_ DESC**](d3dx11-effect-type-desc.md)\***

Ein Zeiger auf eine Beschreibung des Effekttyps. Siehe [**D3DX11 \_ EFFECT TYPE \_ \_ DESC**](d3dx11-effect-type-desc.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Gibt einen der folgenden [Direct3D 11-Rückgabecodes zurück.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Hinweise

Die Beschreibung der Effektvariablen enthält Daten zu Name, Anmerkungen, Semantik, Flags und Pufferoffset des Effekttyps.

> [!Note]  
> Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit. Sie müssen die Quelle Effects 11 verwenden, um Ihre Effekttypanwendung zu erstellen. Weitere Informationen zur Verwendung der Quelle Effects 11 finden Sie unter [Unterschiede zwischen Effekten 10 und Effekten 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Bibliothek<br/> | <dl> <dt>Nicht verfügbar (eine Effects 11-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DX11EffectType](id3dx11effecttype.md)
</dt> </dl>

 

 





