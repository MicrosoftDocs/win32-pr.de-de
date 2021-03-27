---
title: ID3DX11EffectVectorVariable setboolvectorarray-Methode (D3dx11effect. h)
description: Legen Sie ein Array von Vektoren mit vier Komponenten fest, die boolesche Daten enthalten.
ms.assetid: 063735de-093c-4891-9a5c-fe1622da283b
keywords:
- Setboolvectorarray-Methode Direct3D 11
- Setboolvectorarray-Methode Direct3D 11, ID3DX11EffectVectorVariable-Schnittstelle
- ID3DX11EffectVectorVariable-Schnittstelle Direct3D 11, setboolvectorarray-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectVectorVariable.SetBoolVectorArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ce1f34783390c4bcef55df81ba6c9a2215486cb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355467"
---
# <a name="id3dx11effectvectorvariablesetboolvectorarray-method"></a>ID3DX11EffectVectorVariable:: setboolvectorarray-Methode

Legen Sie ein Array von Vektoren mit vier Komponenten fest, die boolesche Daten enthalten.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetBoolVectorArray(
   BOOL *pData,
   UINT Offset,
   UINT Count
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pData* 
</dt> <dd>

Typ: **[ **bool**](/windows/desktop/WinProg/windows-data-types)\***

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

[ID3DX11EffectVectorVariable](id3dx11effectvectorvariable.md)
</dt> </dl>

 

