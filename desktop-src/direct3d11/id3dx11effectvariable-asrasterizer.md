---
title: ID3DX11EffectVariable AsRasterizer-Methode (D3dx11effect.h)
description: Hier erhalten Sie eine Rasterizervariable.
ms.assetid: 6a55d067-f527-4a1b-a4d4-a6d1719aebe7
keywords:
- AsRasterizer-Methode Direct3D 11
- AsRasterizer-Methode Direct3D 11, ID3DX11EffectVariable-Schnittstelle
- ID3DX11EffectVariable-Schnittstelle Direct3D 11 , AsRasterizer-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsRasterizer
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfaf83debc6c7e73a89f78b0c8c3899cce2fb83fb6a5884fa5a5ed9ed5b35912
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858100"
---
# <a name="id3dx11effectvariableasrasterizer-method"></a>ID3DX11EffectVariable::AsRasterizer-Methode

Hier erhalten Sie eine Rasterizervariable.

## <a name="syntax"></a>Syntax


```C++
ID3DX11EffectRasterizerVariable* AsRasterizer();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **[ **ID3DX11EffectRasterizerVariable**](id3dx11effectrasterizervariable.md)\***

Ein Zeiger auf eine Rasterizervariable. Siehe [**ID3DX11EffectRasterizerVariable**](id3dx11effectrasterizervariable.md).

## <a name="remarks"></a>Hinweise

AsRasterizer gibt eine Version der Effektvariablen zurück, die auf eine Rasterizervariable spezialisiert wurde. Ähnlich wie bei einer Typisierung gibt diese Spezialisierung ein ungültiges Objekt zurück, wenn die Effect-Variable keine Rasterizerdaten enthält.

Anwendungen können das zurückgegebene Objekt auf Gültigkeit testen, indem sie [**IsValid aufrufen.**](id3dx11effectvariable-isvalid.md)

> [!Note]  
> Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit. Sie müssen die Quelle Effects 11 verwenden, um Ihre Effekttypanwendung zu erstellen. Weitere Informationen zur Verwendung der Quelle Effects 11 finden Sie unter [Unterschiede zwischen Effekten 10 und Effekten 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Bibliothek<br/> | <dl> <dt>Nicht verfügbar (eine Effects 11-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DX11EffectVariable](id3dx11effectvariable.md)
</dt> </dl>

 

 





