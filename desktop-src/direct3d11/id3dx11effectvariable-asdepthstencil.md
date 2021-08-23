---
title: ID3DX11EffectVariable AsDepthStencil-Methode (D3dx11effect.h)
description: Abrufen einer Tiefenschablonenvariablen.
ms.assetid: 3526812b-6c43-492e-b529-12f61ecd20e3
keywords:
- AsDepthStencil-Methode Direct3D 11
- AsDepthStencil-Methode Direct3D 11 , ID3DX11EffectVariable-Schnittstelle
- ID3DX11EffectVariable-Schnittstelle Direct3D 11 , AsDepthStencil-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsDepthStencil
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 771f22b6b757b9144fca7e2637a3a702232b3d2a4a837938454b2acd5237cfae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119729130"
---
# <a name="id3dx11effectvariableasdepthstencil-method"></a>ID3DX11EffectVariable::AsDepthStencil-Methode

Abrufen einer Tiefenschablonenvariablen.

## <a name="syntax"></a>Syntax


```C++
ID3DX11EffectDepthStencilVariable* AsDepthStencil();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **[ **ID3DX11EffectDepthStencilVariable**](id3dx11effectdepthstencilvariable.md)\***

Ein Zeiger auf eine Tiefenschablonenvariable. Siehe [**ID3DX11EffectDepthStencilVariable**](id3dx11effectdepthstencilvariable.md).

## <a name="remarks"></a>Hinweise

AsDepthStencil gibt eine Version der Effect-Variablen zurück, die auf eine Tiefenschablonenvariable spezialisiert wurde. Ähnlich wie bei einer Umwandlung gibt diese Spezialisierung ein ungültiges Objekt zurück, wenn die Effect-Variable keine Tiefenschablonendaten enthält.

Anwendungen können das zurückgegebene Objekt auf Gültigkeit testen, indem [**sie IsValid**](id3dx11effectvariable-isvalid.md)aufrufen.

> [!Note]  
> Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte zur Verfügung. Sie müssen die Effects 11-Quelle verwenden, um ihre Effekte-Typ-Anwendung zu erstellen. Weitere Informationen zur Verwendung der Quelle Effects 11 finden Sie unter [Unterschiede zwischen Effekten 10 und Effekten 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Bibliothek<br/> | <dl> <dt>N/A (Eine Effects 11-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DX11EffectVariable](id3dx11effectvariable.md)
</dt> </dl>

 

 





