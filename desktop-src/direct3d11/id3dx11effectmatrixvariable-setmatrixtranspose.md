---
title: ID3DX11EffectMatrixVariable setmatrixtransform-Methode (D3dx11effect. h)
description: Sie sollten eine Gleit Komma Matrix austauschen und festlegen.
ms.assetid: 228546c9-0141-4e17-bc8f-bff7201825d7
keywords:
- Setmatrixtransform-Methode Direct3D 11
- Setmatrixtransform-Methode Direct3D 11, ID3DX11EffectMatrixVariable-Schnittstelle
- ID3DX11EffectMatrixVariable-Schnittstelle Direct3D 11, setmatrixtransform-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectMatrixVariable.SetMatrixTranspose
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5daf77b6e2e9578dcbc6c9cfe80f57b149097c32
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982258"
---
# <a name="id3dx11effectmatrixvariablesetmatrixtranspose-method"></a>ID3DX11EffectMatrixVariable:: setmatrixtransform-Methode

Sie sollten eine Gleit Komma Matrix austauschen und festlegen.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetMatrixTranspose(
   float *pData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pData* 
</dt> <dd>

Typ: **float \***

Ein Zeiger auf das erste Element einer Matrix.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Gibt einen der folgenden [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)zurück.

## <a name="remarks"></a>Bemerkungen

Beim Durchführen einer Matrix wird die Reihenfolge der Daten in der Reihenfolge der Zeilen Spalten in der Reihenfolge der Spalten Zeilen (oder umgekehrt) neu angeordnet.

> [!Note]  
> Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit. Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen. Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Bibliothek<br/> | <dl> <dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DX11EffectMatrixVariable](id3dx11effectmatrixvariable.md)
</dt> </dl>

 

 





