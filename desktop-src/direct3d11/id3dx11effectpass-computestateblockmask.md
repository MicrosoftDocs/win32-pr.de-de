---
title: ID3DX11EffectPass computestateblockmask-Methode (D3dx11effect. h)
description: Generiert eine Maske zum zulassen/verhindern von Zustandsänderungen.
ms.assetid: 584be931-0e22-43e6-b852-f0d2ab050bdd
keywords:
- Computestateblockmask-Methode Direct3D 11
- Computestateblockmask-Methode Direct3D 11, ID3DX11EffectPass-Schnittstelle
- ID3DX11EffectPass-Schnittstelle Direct3D 11, computestateblockmask-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectPass.ComputeStateBlockMask
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8fc5cb32ce9e9644d7d5b62868bfa99f150cc94
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982365"
---
# <a name="id3dx11effectpasscomputestateblockmask-method"></a>ID3DX11EffectPass:: computestateblockmask-Methode

Generiert eine Maske zum zulassen/verhindern von Zustandsänderungen.

## <a name="syntax"></a>Syntax


```C++
HRESULT ComputeStateBlockMask(
   D3DX11_STATE_BLOCK_MASK *pStateBlockMask
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pstateblockmask* 
</dt> <dd>

Type: **[ **Bibliothek d3dx11 \_ State \_ Block \_ Mask**](d3dx11-state-block-mask.md)\***

Ein Zeiger auf eine Zustands Block Maske (siehe [**Bibliothek d3dx11 \_ State \_ Block \_ Mask**](d3dx11-state-block-mask.md)).

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

[ID3DX11EffectPass](id3dx11effectpass.md)
</dt> </dl>

 

 





