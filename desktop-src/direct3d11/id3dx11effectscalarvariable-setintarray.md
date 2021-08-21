---
title: ID3DX11EffectScalarVariable SetIntArray-Methode (D3dx11effect.h)
description: Legen Sie ein Array von ganzzahligen Variablen fest.
ms.assetid: 27efb643-0762-4cd7-84ad-f82b2bb1584a
keywords:
- SetIntArray-Methode Direct3D 11
- SetIntArray-Methode Direct3D 11 , ID3DX11EffectScalarVariable-Schnittstelle
- ID3DX11EffectScalarVariable-Schnittstelle Direct3D 11 , SetIntArray-Methode
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
ms.openlocfilehash: 3f5b0c796d47986ba7383cf246a8310542150466de6eb2d33c7fc995d50af21b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118534046"
---
# <a name="id3dx11effectscalarvariablesetintarray-method"></a>ID3DX11EffectScalarVariable::SetIntArray-Methode

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

*Pdata* 
</dt> <dd>

Typ: **[ **int**](/windows/desktop/WinProg/windows-data-types)\***

Ein Zeiger auf den Anfang der festzulegende Daten.

</dd> <dt>

*Offset* 
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Muss auf 0 festgelegt werden. dies ist für die zukünftige Verwendung reserviert.

</dd> <dt>

*Count* 
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Die Anzahl der festzulegende Arrayelemente.

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

 

