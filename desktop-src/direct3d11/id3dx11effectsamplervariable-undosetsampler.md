---
title: ID3DX11EffectSamplerVariable undosetsampler-Methode (D3dx11effect. h)
description: Einen zuvor festgelegten samplerstatus zurücksetzen.
ms.assetid: bb837b12-d6c3-47e9-a0a1-0bfcfe0f3e4e
keywords:
- Undosetsampler-Methode Direct3D 11
- Undosetsampler-Methode Direct3D 11, ID3DX11EffectSamplerVariable-Schnittstelle
- ID3DX11EffectSamplerVariable-Schnittstelle Direct3D 11, undosetsampler-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectSamplerVariable.UndoSetSampler
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e89d72130e92a477b3824f8e5f8fc935e99bd5b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355757"
---
# <a name="id3dx11effectsamplervariableundosetsampler-method"></a>ID3DX11EffectSamplerVariable:: undosetsampler-Methode

Einen zuvor festgelegten samplerstatus zurücksetzen.

## <a name="syntax"></a>Syntax


```C++
HRESULT UndoSetSampler(
   UINT Index
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Index* 
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Indizieren Sie in ein Array von samplingschnittstellen. Wenn nur eine samplerschnittstelle vorhanden ist, verwenden Sie 0.

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

 

