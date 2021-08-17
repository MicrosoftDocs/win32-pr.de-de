---
title: ID3DX11EffectVectorVariable SetBoolVector-Methode (D3dx11effect.h)
description: Legen Sie einen Vektor mit vier Komponenten fest, der boolesche Daten enthält.
ms.assetid: 2138eeb9-6aa0-43f5-852c-1ab9c8117a88
keywords:
- SetBoolVector-Methode Direct3D 11
- SetBoolVector-Methode Direct3D 11 , ID3DX11EffectVectorVariable-Schnittstelle
- ID3DX11EffectVectorVariable-Schnittstelle Direct3D 11, SetBoolVector-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectVectorVariable.SetBoolVector
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ec75ab46bcebb796680310b88897ac8519cdeeb640967e1ddd1a5f413e1a3af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117734032"
---
# <a name="id3dx11effectvectorvariablesetboolvector-method"></a>ID3DX11EffectVectorVariable::SetBoolVector-Methode

Legen Sie einen Vektor mit vier Komponenten fest, der boolesche Daten enthält.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetBoolVector(
   BOOL *pData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Pdata* 
</dt> <dd>

Typ: **[ **BOOL**](/windows/desktop/WinProg/windows-data-types)\***

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



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DX11EffectVectorVariable](id3dx11effectvectorvariable.md)
</dt> </dl>

 

