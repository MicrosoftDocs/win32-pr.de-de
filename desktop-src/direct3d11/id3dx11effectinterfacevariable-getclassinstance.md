---
title: ID3DX11EffectInterfaceVariable GetClassInstance-Methode (D3dx11effect.h)
description: Hier erhalten Sie eine Klasseninstanz.
ms.assetid: a965f4e7-1761-45f1-a72e-7ad0ed1ad671
keywords:
- GetClassInstance-Methode Direct3D 11
- GetClassInstance-Methode Direct3D 11, ID3DX11EffectInterfaceVariable-Schnittstelle
- ID3DX11EffectInterfaceVariable-Schnittstelle Direct3D 11 , GetClassInstance-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectInterfaceVariable.GetClassInstance
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa6fb05473b2671e0224fe36214fa7d8be93dc3bea17ceb90b0b8f0a871cc755
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119988460"
---
# <a name="id3dx11effectinterfacevariablegetclassinstance-method"></a>ID3DX11EffectInterfaceVariable::GetClassInstance-Methode

Hier erhalten Sie eine Klasseninstanz.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetClassInstance(
   ID3DX11EffectClassInstanceVariable **ppEffectClassInstance
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppEffectClassInstance* 
</dt> <dd>

Typ: **[ **ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md)\*\***

Zeiger auf einen [**ID3DX11EffectClassInstanceVariable-Zeiger,**](id3dx11effectclassinstancevariable.md) der auf die Klasseninstanz festgelegt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Gibt einen der folgenden [Direct3D 11-Rückgabecodes zurück.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Hinweise

> [!Note]  
> Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit. Sie müssen die Quelle Effects 11 verwenden, um Ihre Effekttypanwendung zu erstellen. Weitere Informationen zur Verwendung der Quelle Effects 11 finden Sie unter [Unterschiede zwischen Effekten 10 und Effekten 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Bibliothek<br/> | <dl> <dt>Nicht verfügbar (eine Effects 11-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DX11EffectInterfaceVariable](id3dx11effectinterfacevariable.md)
</dt> </dl>

 

 





