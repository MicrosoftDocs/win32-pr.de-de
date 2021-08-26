---
title: ID3DX11EffectVariable AsString-Methode (D3dx11effect.h)
description: Hier erhalten Sie eine Zeichenfolgenvariable.
ms.assetid: 60f8a730-bf95-4577-9259-7348d479ac3d
keywords:
- AsString-Methode Direct3D 11
- AsString-Methode Direct3D 11, ID3DX11EffectVariable-Schnittstelle
- ID3DX11EffectVariable-Schnittstelle Direct3D 11 , AsString-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsString
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c69eecaabec6b7da49f7f36f6c75677fdd20cdb462f26fe5e02650e6746c01f8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069610"
---
# <a name="id3dx11effectvariableasstring-method"></a>ID3DX11EffectVariable::AsString-Methode

Hier erhalten Sie eine Zeichenfolgenvariable.

## <a name="syntax"></a>Syntax


```C++
ID3DX11EffectStringVariable* AsString();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **[ **ID3DX11EffectStringVariable**](id3dx11effectstringvariable.md)\***

Ein Zeiger auf eine Zeichenfolgenvariable. Siehe [**ID3DX11EffectStringVariable**](id3dx11effectstringvariable.md).

## <a name="remarks"></a>Hinweise

AsString gibt eine Version der Effektvariablen zurück, die auf eine Zeichenfolgenvariable spezialisiert wurde. Ähnlich wie eine Cast gibt diese Spezialisierung ein ungültiges Objekt zurück, wenn die Effect-Variable keine Zeichenfolgendaten enthält.

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

 

 





