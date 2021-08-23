---
title: ID3DX11EffectVectorVariable GetFloatVector-Methode (D3dx11effect.h)
description: Abrufen eines Vektors mit vier Komponenten, der Gleitkommadaten enthält.
ms.assetid: 980c85db-0d40-49e0-99d0-5049fdf62540
keywords:
- GetFloatVector-Methode Direct3D 11
- GetFloatVector-Methode Direct3D 11 , ID3DX11EffectVectorVariable-Schnittstelle
- ID3DX11EffectVectorVariable-Schnittstelle Direct3D 11, GetFloatVector-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectVectorVariable.GetFloatVector
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 861121c89bbeda277610c0c3e42d4d6e41795b5cd82b48ae8ba42a1783ee5eff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989670"
---
# <a name="id3dx11effectvectorvariablegetfloatvector-method"></a>ID3DX11EffectVectorVariable::GetFloatVector-Methode

Abrufen eines Vektors mit vier Komponenten, der Gleitkommadaten enthält.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetFloatVector(
   float *pData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Pdata* 
</dt> <dd>

Typ: **\* float**

Ein Zeiger auf die erste Komponente.

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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DX11EffectVectorVariable](id3dx11effectvectorvariable.md)
</dt> </dl>

 

 





