---
title: ID3DX11EffectVectorVariable setfloatvector-Methode (D3dx11effect. h)
description: Legen Sie einen Vektor mit vier Komponenten fest, der Gleit Komma Daten enthält.
ms.assetid: fb646df6-b9f9-4d71-93c3-38833076b781
keywords:
- Setfloatvector-Methode Direct3D 11
- Setfloatvector-Methode Direct3D 11, ID3DX11EffectVectorVariable-Schnittstelle
- ID3DX11EffectVectorVariable-Schnittstelle Direct3D 11, setfloatvector-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectVectorVariable.SetFloatVector
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5541f2773e992c4c52bf748bceb832d67b28825
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394201"
---
# <a name="id3dx11effectvectorvariablesetfloatvector-method"></a>ID3DX11EffectVectorVariable:: setfloatvector-Methode

Legen Sie einen Vektor mit vier Komponenten fest, der Gleit Komma Daten enthält.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetFloatVector(
   float *pData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pData* 
</dt> <dd>

Typ: **float \***

Ein Zeiger auf die erste Komponente.

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

[ID3DX11EffectVectorVariable](id3dx11effectvectorvariable.md)
</dt> </dl>

 

 





