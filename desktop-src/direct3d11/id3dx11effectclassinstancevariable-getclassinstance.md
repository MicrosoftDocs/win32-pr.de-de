---
title: ID3DX11EffectClassInstanceVariable getclassinstance-Methode (D3dx11effect. h)
description: Ruft eine-Klasseninstanz ab.
ms.assetid: dec00a6b-0587-40cf-abae-dd110a639fe0
keywords:
- Getclassinstance-Methode Direct3D 11
- Getclassinstance-Methode Direct3D 11, ID3DX11EffectClassInstanceVariable-Schnittstelle
- ID3DX11EffectClassInstanceVariable-Schnittstelle Direct3D 11, getclassinstance-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectClassInstanceVariable.GetClassInstance
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5dae96d42a0088adc683ca93d7e3215c12912a87
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104356037"
---
# <a name="id3dx11effectclassinstancevariablegetclassinstance-method"></a>ID3DX11EffectClassInstanceVariable:: getclassinstance-Methode

Ruft eine-Klasseninstanz ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetClassInstance(
   ID3D11ClassInstance **ppClassInstance
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppclassinstance* 
</dt> <dd>

Typ: **[ **ID3D11ClassInstance**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classinstance)\*\***

Zeiger auf einen [**ID3D11ClassInstance**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classinstance) -Zeiger, der auf eine Klasseninstanz festgelegt wird.

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

[ID3DX11EffectClassInstanceVariable](id3dx11effectclassinstancevariable.md)
</dt> </dl>

 

 





