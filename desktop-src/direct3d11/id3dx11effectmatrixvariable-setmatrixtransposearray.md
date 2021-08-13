---
title: ID3DX11EffectMatrixVariable SetMatrixTransposeArray-Methode (D3dx11effect.h)
description: Transponieren und Festlegen eines Arrays von Gleitkommamatrizen.
ms.assetid: 08223022-5e77-4a84-9b68-b9b0c9a02270
keywords:
- SetMatrixTransposeArray-Methode Direct3D 11
- SetMatrixTransposeArray-Methode Direct3D 11, ID3DX11EffectMatrixVariable-Schnittstelle
- ID3DX11EffectMatrixVariable-Schnittstelle Direct3D 11 , SetMatrixTransposeArray-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectMatrixVariable.SetMatrixTransposeArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ff122a5c38d4d3d0a3eee96537077b8a09695c52cefe77b39c5f9b2a804692c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119046058"
---
# <a name="id3dx11effectmatrixvariablesetmatrixtransposearray-method"></a>ID3DX11EffectMatrixVariable::SetMatrixTransposeArray-Methode

Transponieren und Festlegen eines Arrays von Gleitkommamatrizen.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetMatrixTransposeArray(
   float *pData,
   UINT  Offset,
   UINT  Count
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Pdata* 
</dt> <dd>

Typ: **\* float**

Ein Zeiger auf ein Array von Matrizen.

</dd> <dt>

*Offset* 
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Der Offset (in Der Anzahl der Matrizen) zwischen dem Anfang des Arrays und der ersten matrix, die festgelegt werden soll.

</dd> <dt>

*Count* 
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Die Anzahl der zu setzenden Matrizen im Array.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Gibt einen der folgenden [Direct3D 11-Rückgabecodes zurück.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Hinweise

Durch das Transposieren einer Matrix wird die Datenreihen reihenfolge von Zeilenspaltenreihen reihenfolge in Spaltenreihenreihen reihenfolge (oder umgekehrt) neu geordnet.

> [!Note]  
> Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit. Sie müssen die Quelle Effects 11 verwenden, um Ihre Effekttypanwendung zu erstellen. Weitere Informationen zur Verwendung der Quelle Effects 11 finden Sie unter [Unterschiede zwischen Effekten 10 und Effekten 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Bibliothek<br/> | <dl> <dt>Nicht verfügbar (eine Effects 11-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DX11EffectMatrixVariable](id3dx11effectmatrixvariable.md)
</dt> </dl>

 

