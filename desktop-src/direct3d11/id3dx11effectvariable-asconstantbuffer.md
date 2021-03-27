---
title: ID3DX11EffectVariable asconstantbuffer-Methode (D3dx11effect. h)
description: Einen konstanten Puffer erhalten. | ID3DX11EffectVariable asconstantbuffer-Methode (D3dx11effect. h)
ms.assetid: b8d8b43c-4626-43b6-8a49-8ffa7cb48427
keywords:
- Asconstantbuffer-Methode Direct3D 11
- Asconstantbuffer-Methode Direct3D 11, ID3DX11EffectVariable-Schnittstelle
- ID3DX11EffectVariable-Schnittstelle Direct3D 11, asconstantbuffer-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsConstantBuffer
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee4caca60216df0c04a773da22150dbc6f7be717
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104995919"
---
# <a name="id3dx11effectvariableasconstantbuffer-method"></a>ID3DX11EffectVariable:: asconstantbuffer-Methode

Einen konstanten Puffer erhalten.

## <a name="syntax"></a>Syntax


```C++
ID3DX11EffectConstantBuffer* AsConstantBuffer();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **[ **ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md)\***

Ein Zeiger auf einen konstanten Puffer. Siehe [**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md).

## <a name="remarks"></a>Bemerkungen

Asconstantbuffer gibt eine Version der Effekt Variablen zurück, die auf einen konstanten Puffer spezialisiert wurde. Ähnlich wie bei einer Umwandlung gibt diese Spezialisierung ein ungültiges Objekt zurück, wenn die Effekt Variable keine Konstanten Puffer Daten enthält.

Anwendungen können das zurückgegebene Objekt auf Gültigkeit testen, indem Sie [**IsValid**](id3dx11effectvariable-isvalid.md)aufrufen.

> [!Note]  
> Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit. Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen. Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Bibliothek<br/> | <dl> <dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DX11EffectVariable](id3dx11effectvariable.md)
</dt> </dl>

 

 





