---
title: ID3DX11EffectVariable AsMatrix-Methode (D3dx11effect.h)
description: Hier erhalten Sie eine Matrixvariable.
ms.assetid: 5d2baf65-ab0d-44df-bc6f-6ffae16cbb01
keywords:
- AsMatrix-Methode Direct3D 11
- AsMatrix-Methode Direct3D 11, ID3DX11EffectVariable-Schnittstelle
- ID3DX11EffectVariable-Schnittstelle Direct3D 11 , AsMatrix-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsMatrix
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 294f3f6a01d88f92f606e5120edbfa8d5086f2e0173375fd78f5525c17c4f1f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118531501"
---
# <a name="id3dx11effectvariableasmatrix-method"></a>ID3DX11EffectVariable::AsMatrix-Methode

Hier erhalten Sie eine Matrixvariable.

## <a name="syntax"></a>Syntax


```C++
ID3DX11EffectMatrixVariable* AsMatrix();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **[ **ID3DX11EffectMatrixVariable**](id3dx11effectmatrixvariable.md)\***

Ein Zeiger auf eine Matrixvariable. Siehe [**ID3DX11EffectMatrixVariable**](id3dx11effectmatrixvariable.md).

## <a name="remarks"></a>Hinweise

AsMatrix gibt eine Version der Effektvariablen zurück, die auf eine Matrixvariable spezialisiert wurde. Ähnlich wie eine Cast gibt diese Spezialisierung ein ungültiges Objekt zurück, wenn die Effect-Variable keine Matrixdaten enthält.

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

 

 





