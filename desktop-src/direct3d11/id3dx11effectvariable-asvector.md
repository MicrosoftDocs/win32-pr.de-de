---
title: ID3DX11EffectVariable AsVector-Methode (D3dx11effect.h)
description: Hier erhalten Sie eine Vektorvariable.
ms.assetid: 995bd9f3-1417-4048-9a23-4dcb3864c77d
keywords:
- AsVector-Methode Direct3D 11
- AsVector-Methode Direct3D 11, ID3DX11EffectVariable-Schnittstelle
- ID3DX11EffectVariable-Schnittstelle Direct3D 11 , AsVector-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsVector
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd5ce5023c0fd77109d91705c3faaf788b5f0e6edd3bd3ba15b7aeb367b8d061
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119690"
---
# <a name="id3dx11effectvariableasvector-method"></a>ID3DX11EffectVariable::AsVector-Methode

Hier erhalten Sie eine Vektorvariable.

## <a name="syntax"></a>Syntax


```C++
ID3DX11EffectVectorVariable* AsVector();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **[ **ID3DX11EffectVectorVariable**](id3dx11effectvectorvariable.md)\***

Ein Zeiger auf eine Vektorvariable. Siehe [**ID3DX11EffectVectorVariable**](id3dx11effectvectorvariable.md).

## <a name="remarks"></a>Hinweise

AsVector gibt eine Version der Effektvariablen zurück, die auf eine Vektorvariable spezialisiert wurde. Ähnlich wie bei einer Cast gibt diese Spezialisierung ein ungültiges Objekt zurück, wenn die Effect-Variable keine Vektordaten enthält.

Anwendungen können das zurückgegebene Objekt auf Gültigkeit testen, indem sie [**IsValid aufrufen.**](id3dx11effectvariable-isvalid.md)

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

 

 





