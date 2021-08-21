---
title: ID3DX11EffectVariable AsRenderTargetView-Methode (D3dx11effect.h)
description: Hier erhalten Sie eine Renderzielansichtsvariable.
ms.assetid: 1eec342e-267a-4eab-886a-a309758065c7
keywords:
- AsRenderTargetView-Methode Direct3D 11
- AsRenderTargetView-Methode Direct3D 11, ID3DX11EffectVariable-Schnittstelle
- ID3DX11EffectVariable-Schnittstelle Direct3D 11 , AsRenderTargetView-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsRenderTargetView
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a8b44b3ed67b6293d4b4add329eef532fdc44cb12cea9e84b1ddf43fb72cc05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118531421"
---
# <a name="id3dx11effectvariableasrendertargetview-method"></a>ID3DX11EffectVariable::AsRenderTargetView-Methode

Hier erhalten Sie eine Renderzielansichtsvariable.

## <a name="syntax"></a>Syntax


```C++
ID3DX11EffectRenderTargetViewVariable* AsRenderTargetView();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **[ **ID3DX11EffectRenderTargetViewVariable**](id3dx11effectrendertargetviewvariable.md)\***

Ein Zeiger auf eine Renderzielansichtsvariable. Siehe [**ID3DX11EffectRenderTargetViewVariable**](id3dx11effectrendertargetviewvariable.md).

## <a name="remarks"></a>Hinweise

Diese Methode gibt eine Version der Effektvariablen zurück, die auf eine Renderzielansichtsvariable spezialisiert wurde. Ähnlich wie bei einer Cast gibt diese Spezialisierung ein ungültiges Objekt zurück, wenn die Effect-Variable keine Renderzielansichtsdaten enthält.

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

 

 





