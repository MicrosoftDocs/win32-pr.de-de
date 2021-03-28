---
title: ID3DX11EffectSamplerVariable getsampler-Methode (D3dx11effect. h)
description: Einen Zeiger auf eine samplerschnittstelle erhalten.
ms.assetid: ac2a05f1-e3ca-4ebf-b655-34133c4e50ac
keywords:
- Getsampler-Methode Direct3D 11
- Getsampler-Methode Direct3D 11, ID3DX11EffectSamplerVariable-Schnittstelle
- ID3DX11EffectSamplerVariable Interface Direct3D 11, getsampler-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectSamplerVariable.GetSampler
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f53260a07e544d5f69a9575851614f694b778619
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961746"
---
# <a name="id3dx11effectsamplervariablegetsampler-method"></a>ID3DX11EffectSamplerVariable:: getsampler-Methode

Einen Zeiger auf eine samplerschnittstelle erhalten.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetSampler(
   UINT               Index,
   ID3D11SamplerState **ppSampler
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Index* 
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Indizieren Sie in ein Array von samplingschnittstellen. Wenn nur eine samplerschnittstelle vorhanden ist, verwenden Sie 0.

</dd> <dt>

*ppsampler* 
</dt> <dd>

Typ: **[ **ID3D11SamplerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11samplerstate)\*\***

Die Adresse eines Zeigers auf eine samplerschnittstelle (siehe [**ID3D11SamplerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11samplerstate)).

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

 

