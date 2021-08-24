---
title: ID3DX11EffectScalarVariable SetFloat-Methode (D3dx11effect.h)
description: Legen Sie eine Gleitkommavariable fest.
ms.assetid: e13f3ba1-437a-47f0-bd08-4423ffc25ddb
keywords:
- SetFloat-Methode Direct3D 11
- SetFloat-Methode Direct3D 11 , ID3DX11EffectScalarVariable-Schnittstelle
- ID3DX11EffectScalarVariable-Schnittstelle Direct3D 11, SetFloat-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectScalarVariable.SetFloat
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 573880f07752e353e7a623d249353f7e0f020902443fde23538f38a2227e7d4a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119460850"
---
# <a name="id3dx11effectscalarvariablesetfloat-method"></a>ID3DX11EffectScalarVariable::SetFloat-Methode

Legen Sie eine Gleitkommavariable fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetFloat(
   float Value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Wert* 
</dt> <dd>

Typ: **float**

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

 

 





