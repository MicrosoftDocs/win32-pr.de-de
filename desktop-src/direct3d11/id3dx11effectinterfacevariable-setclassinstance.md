---
title: ID3DX11EffectInterfaceVariable setclassinstance-Methode (D3dx11effect. h)
description: Legt eine Klasseninstanz fest.
ms.assetid: fc71a0d2-054a-48ed-86a5-54cf0017062a
keywords:
- Setclassinstance-Methode Direct3D 11
- Setclassinstance-Methode Direct3D 11, ID3DX11EffectInterfaceVariable-Schnittstelle
- ID3DX11EffectInterfaceVariable-Schnittstelle Direct3D 11, setclassinstance-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectInterfaceVariable.SetClassInstance
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c03d319d55b073393ff511b2e072aa07c244e5a2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982275"
---
# <a name="id3dx11effectinterfacevariablesetclassinstance-method"></a>ID3DX11EffectInterfaceVariable:: setclassinstance-Methode

Legt eine Klasseninstanz fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetClassInstance(
   ID3DX11EffectClassInstanceVariable *pEffectClassInstance
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*"Peer-ectclassinstance"* 
</dt> <dd>

Typ: **[ **ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md)\***

Zeiger auf eine [**ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md) -Schnittstelle.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Gibt einen der folgenden [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)zurück.

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit. Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen. Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Bibliothek<br/> | <dl> <dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DX11EffectInterfaceVariable](id3dx11effectinterfacevariable.md)
</dt> </dl>

 

 





