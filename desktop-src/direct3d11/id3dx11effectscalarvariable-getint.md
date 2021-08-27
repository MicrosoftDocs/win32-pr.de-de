---
title: ID3DX11EffectScalarVariable GetInt-Methode (D3dx11effect.h)
description: Abrufen einer ganzzahligen Variablen.
ms.assetid: 82a5a7a5-17cb-4e5e-ae4e-57c0ff9757c5
keywords:
- GetInt-Methode Direct3D 11
- GetInt-Methode Direct3D 11 , ID3DX11EffectScalarVariable-Schnittstelle
- ID3DX11EffectScalarVariable-Schnittstelle Direct3D 11 , GetInt-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectScalarVariable.GetInt
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7619fe4e0fd668e280efa094cc8b8d8d91b2b99f559612bfc6a7af09e08dab1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118534176"
---
# <a name="id3dx11effectscalarvariablegetint-method"></a>ID3DX11EffectScalarVariable::GetInt-Methode

Abrufen einer ganzzahligen Variablen.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetInt(
   int *pValue
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Pvalue* 
</dt> <dd>

Typ: **[ **int**](/windows/desktop/WinProg/windows-data-types)\***

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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DX11EffectScalarVariable](id3dx11effectscalarvariable.md)
</dt> </dl>

 

