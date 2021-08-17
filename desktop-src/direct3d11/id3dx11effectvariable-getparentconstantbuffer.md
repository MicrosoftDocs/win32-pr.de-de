---
title: ID3DX11EffectVariable GetParentConstantBuffer-Methode (D3dx11effect.h)
description: Hier erhalten Sie einen konstanten Puffer. | ID3DX11EffectVariable GetParentConstantBuffer-Methode (D3dx11effect.h)
ms.assetid: 43b46b05-951e-4c52-8bc7-4bb5f657ea78
keywords:
- GetParentConstantBuffer-Methode Direct3D 11
- GetParentConstantBuffer-Methode Direct3D 11, ID3DX11EffectVariable-Schnittstelle
- ID3DX11EffectVariable-Schnittstelle Direct3D 11 , GetParentConstantBuffer-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.GetParentConstantBuffer
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2319a72e50d83f3780b68de163dc370d5627c28ab4ab84f6621c11faf6df7805
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117734113"
---
# <a name="id3dx11effectvariablegetparentconstantbuffer-method"></a>ID3DX11EffectVariable::GetParentConstantBuffer-Methode

Hier erhalten Sie einen konstanten Puffer.

## <a name="syntax"></a>Syntax


```C++
ID3DX11EffectConstantBuffer* GetParentConstantBuffer();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **[ **ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md)\***

Ein Zeiger auf eine [**ID3DX11EffectConstantBuffer.**](id3dx11effectconstantbuffer.md)

## <a name="remarks"></a>Hinweise

Effect-Variablen werden aus einem konstanten Puffer gelesen oder in einen konstanten Puffer geschrieben.

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

 

 





