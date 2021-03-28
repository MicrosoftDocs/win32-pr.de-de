---
title: ID3DX11EffectScalarVariable getfloatarray-Methode (D3dx11effect. h)
description: Ein Array von Gleit Komma Variablen erhalten.
ms.assetid: e5e0dbee-47f5-46ed-89a0-01782345498f
keywords:
- Getfloatarray-Methode Direct3D 11
- Getfloatarray-Methode Direct3D 11, ID3DX11EffectScalarVariable-Schnittstelle
- ID3DX11EffectScalarVariable Interface Direct3D 11, getfloatarray-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectScalarVariable.GetFloatArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90cc760b7b7b57172becee0b9df9765be4d097f1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982517"
---
# <a name="id3dx11effectscalarvariablegetfloatarray-method"></a>ID3DX11EffectScalarVariable:: getfloatarray-Methode

Ein Array von Gleit Komma Variablen erhalten.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetFloatArray(
   float *pData,
   UINT  Offset,
   UINT  Count
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pData* 
</dt> <dd>

Typ: **float \***

Ein Zeiger auf den Anfang der festzulegenden Daten.

</dd> <dt>

*Offset* 
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Muss auf 0 (null) festgelegt werden. Dies ist für die zukünftige Verwendung reserviert.

</dd> <dt>

*Count* 
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Die Anzahl der festzulegenden Array Elemente.

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

[ID3DX11EffectScalarVariable](id3dx11effectscalarvariable.md)
</dt> </dl>

 

