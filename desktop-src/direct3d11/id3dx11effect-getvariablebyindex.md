---
title: ID3DX11Effect getvariablebyindex-Methode (D3dx11effect. h)
description: Eine Variable nach Index erhalten.
ms.assetid: af25b945-9526-45c2-8746-8b62f8166de7
keywords:
- Getvariablebyindex-Methode Direct3D 11
- Getvariablebyindex-Methode Direct3D 11, ID3DX11Effect-Schnittstelle
- ID3DX11Effect Interface Direct3D 11, getvariablebyindex-Methode
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetVariableByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd262ea0aa778f03c2d723dec99f531f3419f3be
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996100"
---
# <a name="id3dx11effectgetvariablebyindex-method"></a>ID3DX11Effect:: getvariablebyindex-Methode

Eine Variable nach Index erhalten.

## <a name="syntax"></a>Syntax


```C++
ID3DX11EffectVariable* GetVariableByIndex(
   UINT Index
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Index* 
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Ein NULL basierter Index.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***

Ein Zeiger auf eine [**ID3DX11EffectVariable**](id3dx11effectvariable.md).

## <a name="remarks"></a>Bemerkungen

Ein Effekt kann eine oder mehrere Variablen enthalten. Variablen außerhalb eines Verfahrens werden als Global für alle Effekte betrachtet, die sich innerhalb eines Verfahrens vor Ort befinden. Sie können auf eine beliebige lokale nicht statische Effekt Variable mithilfe Ihres Namens oder mit einem Index zugreifen.

Die-Methode gibt einen Zeiger auf eine [**Effekt Variable-Schnittstelle**](id3dx11effectvariable.md) zurück, wenn eine Variable nicht gefunden wird. Sie können [**ID3DX11Effect:: IsValid**](id3dx11effect-isvalid.md) aufgerufen, um zu überprüfen, ob der Index vorhanden ist.

> [!Note]  
> Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit. Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen. Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Bibliothek<br/> | <dl> <dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DX11Effect](id3dx11effect.md)
</dt> </dl>

 

