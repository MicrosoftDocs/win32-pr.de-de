---
title: ID3DX11EffectScalarVariable-Methode für die Methode (D3dx11effect. h)
description: Legen Sie eine Integer-Variable fest.
ms.assetid: 614284be-8f70-4d7e-b797-b67e813615ab
keywords:
- Methode Direct3D 11
- Direct3D 11, ID3DX11EffectScalarVariable-Schnittstelle
- ID3DX11EffectScalarVariable-Schnittstelle Direct3D 11,-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectScalarVariable.SetInt
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b4e2f44a3b67db12bd84f5dd23426c033b99b57
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219447"
---
# <a name="id3dx11effectscalarvariablesetint-method"></a>ID3DX11EffectScalarVariable:: abtint-Methode

Legen Sie eine Integer-Variable fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetInt(
   int Value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Wert* 
</dt> <dd>

Typ: **[ **int**](/windows/desktop/WinProg/windows-data-types)**

Ein Zeiger auf die Variable.

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

 

