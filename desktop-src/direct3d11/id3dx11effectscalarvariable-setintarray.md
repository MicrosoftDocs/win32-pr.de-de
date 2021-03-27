---
title: ID3DX11EffectScalarVariable-Methode "tartintarray" (D3dx11effect. h)
description: Legen Sie ein Array von ganzzahligen Variablen fest.
ms.assetid: 27efb643-0762-4cd7-84ad-f82b2bb1584a
keywords:
- Methode "tartintarray" Direct3D 11
- "\"Tartintarray\"-Methode Direct3D 11, ID3DX11EffectScalarVariable-Schnittstelle"
- ID3DX11EffectScalarVariable-Schnittstelle Direct3D 11, Methode "tartintarray"
topic_type:
- apiref
api_name:
- ID3DX11EffectScalarVariable.SetIntArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 142a1686b9dde8f6a2c8f41d521ac085bd403ec0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982155"
---
# <a name="id3dx11effectscalarvariablesetintarray-method"></a>ID3DX11EffectScalarVariable:: tartintarray-Methode

Legen Sie ein Array von ganzzahligen Variablen fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetIntArray(
   int  *pData,
   UINT Offset,
   UINT Count
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pData* 
</dt> <dd>

Typ: **[ **int**](/windows/desktop/WinProg/windows-data-types)\***

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

 

