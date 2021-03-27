---
title: ID3DX11EffectVariable getannotationbyname-Methode (D3dx11effect. h)
description: Eine Anmerkung anhand des Namens erhalten. | ID3DX11EffectVariable getannotationbyname-Methode (D3dx11effect. h)
ms.assetid: 0ca3df07-c721-48c4-9422-f6af24acbaef
keywords:
- Getannotationbyname-Methode Direct3D 11
- Getannotationbyname-Methode Direct3D 11, ID3DX11EffectVariable-Schnittstelle
- ID3DX11EffectVariable Interface Direct3D 11, getannotationbyname-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.GetAnnotationByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e37efcd773728e563a4112f61a7c6c965d05bad4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355117"
---
# <a name="id3dx11effectvariablegetannotationbyname-method"></a>ID3DX11EffectVariable:: getannotationbyname-Methode

Eine Anmerkung anhand des Namens erhalten.

## <a name="syntax"></a>Syntax


```C++
ID3DX11EffectVariable* GetAnnotationByName(
   LPCSTR Name
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Name* 
</dt> <dd>

Typ: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Der Name der Anmerkung.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***

Ein Zeiger auf eine [**ID3DX11EffectVariable**](id3dx11effectvariable.md). Beachten Sie, dass die zurückgegebene **ID3DX11EffectVariable** leer ist, wenn die Anmerkung nicht gefunden wird. Die [**ID3DX11EffectVariable:: IsValid**](id3dx11effectvariable-isvalid.md) -Methode sollte aufgerufen werden, um zu bestimmen, ob die Anmerkung gefunden wurde.

## <a name="remarks"></a>Bemerkungen

Anmerkungen können an eine Technik, einen Durchlauf oder eine globale Variable angefügt werden.

> [!Note]  
> Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit. Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen. Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Bibliothek<br/> | <dl> <dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DX11EffectVariable](id3dx11effectvariable.md)
</dt> </dl>

 

