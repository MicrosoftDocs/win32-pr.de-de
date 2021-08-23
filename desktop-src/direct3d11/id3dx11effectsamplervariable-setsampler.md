---
title: ID3DX11EffectSamplerVariable SetSampler-Methode (D3dx11effect.h)
description: Legen Sie den Samplerzustand fest.
ms.assetid: 1826923d-d770-4d79-818a-a42a279f0a8c
keywords:
- SetSampler-Methode Direct3D 11
- SetSampler-Methode Direct3D 11 , ID3DX11EffectSamplerVariable-Schnittstelle
- ID3DX11EffectSamplerVariable-Schnittstelle Direct3D 11, SetSampler-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectSamplerVariable.SetSampler
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4667b8261b46b1ecb1732c1ecc77efcf93d327426f0ea20f6c7710e94ed825e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119791940"
---
# <a name="id3dx11effectsamplervariablesetsampler-method"></a>ID3DX11EffectSamplerVariable::SetSampler-Methode

Legen Sie den Samplerzustand fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetSampler(
   UINT               Index,
   ID3D11SamplerState *pSampler
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Index* 
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Index in ein Array von Samplerschnittstellen. Wenn nur eine Samplerschnittstelle vorhanden ist, verwenden Sie 0.

</dd> <dt>

*pSampler* 
</dt> <dd>

Typ: **[ **ID3D11SamplerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11samplerstate)\***

Zeiger auf eine [**ID3D11SamplerState-Schnittstelle,**](/windows/desktop/api/D3D11/nn-d3d11-id3d11samplerstate) die den Samplerzustand enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Gibt einen der folgenden [Direct3D 11-Rückgabecodes zurück.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Hinweise

> [!Note]  
> Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte zur Verfügung. Sie müssen die Effects 11-Quelle verwenden, um ihre Effekte-Typ-Anwendung zu erstellen. Weitere Informationen zur Verwendung der Quelle Effects 11 finden Sie unter [Unterschiede zwischen Effekten 10 und Effekten 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Bibliothek<br/> | <dl> <dt>N/A (Eine Effects 11-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DX11EffectSamplerVariable](id3dx11effectsamplervariable.md)
</dt> </dl>

 

