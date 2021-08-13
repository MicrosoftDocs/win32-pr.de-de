---
title: ID3DX11EffectScalarVariable SetInt-Methode (D3dx11effect.h)
description: Legen Sie eine ganzzahlige Variable fest.
ms.assetid: 614284be-8f70-4d7e-b797-b67e813615ab
keywords:
- SetInt-Methode Direct3D 11
- SetInt-Methode Direct3D 11 , ID3DX11EffectScalarVariable-Schnittstelle
- ID3DX11EffectScalarVariable-Schnittstelle Direct3D 11, SetInt-Methode
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
ms.openlocfilehash: 215083d35bfbdd67cd970bfe31b81a1e19594b2bf849e1c19692fa96af257036
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119377540"
---
# <a name="id3dx11effectscalarvariablesetint-method"></a>ID3DX11EffectScalarVariable::SetInt-Methode

Legen Sie eine ganzzahlige Variable fest.

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

[ID3DX11EffectScalarVariable](id3dx11effectscalarvariable.md)
</dt> </dl>

 

