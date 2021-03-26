---
title: ID3DX11EffectSamplerVariable getbackingstore-Methode (D3dx11effect. h)
description: Einen Zeiger auf eine Variable mit dem samplerstatus erhalten.
ms.assetid: b188fb86-f54b-481e-9110-7b8af70ff303
keywords:
- Getbackingstore-Methode Direct3D 11
- Getbackingstore-Methode Direct3D 11, ID3DX11EffectSamplerVariable-Schnittstelle
- ID3DX11EffectSamplerVariable Interface Direct3D 11, getbackingstore-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectSamplerVariable.GetBackingStore
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03f2d6ac3035d1dd2fd3aee8950135d7b4481862
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355366"
---
# <a name="id3dx11effectsamplervariablegetbackingstore-method"></a>ID3DX11EffectSamplerVariable:: getbackingstore-Methode

Einen Zeiger auf eine Variable mit dem samplerstatus erhalten.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetBackingStore(
   UINT               Index,
   D3D11_SAMPLER_DESC *pSamplerDesc
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Index* 
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Indizieren Sie in ein Array von Sampler-Beschreibungen. Wenn nur eine samplervariable vorhanden ist, verwenden Sie 0.

</dd> <dt>

*psamplerdebug* 
</dt> <dd>

Type: **[ **D3D11 \_ Sampler \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_sampler_desc)\***

Ein Zeiger auf eine samplerbeschreibung (siehe [**D3D11 \_ Sampler \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_sampler_desc)Debug).

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

[ID3DX11EffectSamplerVariable](id3dx11effectsamplervariable.md)
</dt> </dl>

 

