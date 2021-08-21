---
title: ID3DX11EffectVariable AsUnorderedAccessView-Methode (D3dx11effect.h)
description: Abrufen einer Variablen mit ungeordneten Zugriffsansichten.
ms.assetid: e8b7c104-09f7-4bfb-9980-a5603550b723
keywords:
- AsUnorderedAccessView-Methode Direct3D 11
- AsUnorderedAccessView-Methode Direct3D 11 , ID3DX11EffectVariable-Schnittstelle
- ID3DX11EffectVariable-Schnittstelle Direct3D 11 , AsUnorderedAccessView-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsUnorderedAccessView
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4cf3a1f146af7ca6faf3ff3e704285ac19f01a117809429842b45df9b7dcfd4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118531208"
---
# <a name="id3dx11effectvariableasunorderedaccessview-method"></a>ID3DX11EffectVariable::AsUnorderedAccessView-Methode

Abrufen einer Variablen mit ungeordneten Zugriffsansichten.

## <a name="syntax"></a>Syntax


```C++
ID3DX11EffectUnorderedAccessViewVariable* AsUnorderedAccessView();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **[ **ID3DX11EffectUnorderedAccessViewVariable**](id3dx11effectunorderedaccessviewvariable.md)\***

Ein Zeiger auf eine Variable mit ungeordneten Zugriffsansichten. Siehe [**ID3DX11EffectUnorderedAccessViewVariable**](id3dx11effectunorderedaccessviewvariable.md).

## <a name="remarks"></a>Hinweise

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

 

 





