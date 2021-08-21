---
title: ID3DX11EffectVariable AsBlend-Methode (D3dx11effect.h)
description: Abrufen einer Effektblendvariable.
ms.assetid: e9670d13-e006-408b-9cdf-352bcfa66a52
keywords:
- AsBlend-Methode Direct3D 11
- AsBlend-Methode Direct3D 11 , ID3DX11EffectVariable-Schnittstelle
- ID3DX11EffectVariable-Schnittstelle Direct3D 11, AsBlend-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsBlend
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fd9f6f76c0e3aa46e176b2f35960196fcc73eb021d4e5a250be4a5b245a5ca4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118531602"
---
# <a name="id3dx11effectvariableasblend-method"></a>ID3DX11EffectVariable::AsBlend-Methode

Abrufen einer Effektblendvariable.

## <a name="syntax"></a>Syntax


```C++
ID3DX11EffectBlendVariable* AsBlend();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **[ **ID3DX11EffectBlendVariable**](id3dx11effectblendvariable.md)\***

Ein Zeiger auf eine Effektmischungsvariable. Siehe [**ID3DX11EffectBlendVariable**](id3dx11effectblendvariable.md).

## <a name="remarks"></a>Hinweise

AsBlend gibt eine Version der Effektvariablen zurück, die auf eine Effektmischungsvariable spezialisiert wurde. Ähnlich wie bei einer Umwandlung gibt diese Spezialisierung ein ungültiges Objekt zurück, wenn die Effect-Variable keine Effect Blend-Daten enthält.

Anwendungen können das zurückgegebene Objekt auf Gültigkeit testen, indem [**sie IsValid**](id3dx11effectvariable-isvalid.md)aufrufen.

> [!Note]  
> Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte zur Verfügung. Sie müssen die Effects 11-Quelle verwenden, um ihre Effekte-Typ-Anwendung zu erstellen. Weitere Informationen zur Verwendung der Quelle Effects 11 finden Sie unter [Unterschiede zwischen Effekten 10 und Effekten 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Bibliothek<br/> | <dl> <dt>N/A (Eine Effects 11-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DX11EffectVariable](id3dx11effectvariable.md)
</dt> </dl>

 

 





