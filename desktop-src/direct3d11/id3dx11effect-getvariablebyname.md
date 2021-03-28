---
title: ID3DX11Effect getvariablebyname-Methode (D3dx11effect. h)
description: Eine Variable anhand ihres Namens erhalten.
ms.assetid: d20c5a85-51a5-482f-b5b0-197d8e993910
keywords:
- Getvariablebyname-Methode Direct3D 11
- Getvariablebyname-Methode Direct3D 11, ID3DX11Effect-Schnittstelle
- ID3DX11Effect Interface Direct3D 11, getvariablebyname-Methode
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetVariableByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e6079e7f45c21d9d7326021b2c439ab12e4e031
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996094"
---
# <a name="id3dx11effectgetvariablebyname-method"></a>ID3DX11Effect:: getvariablebyname-Methode

Eine Variable anhand ihres Namens erhalten.

## <a name="syntax"></a>Syntax


```C++
ID3DX11EffectVariable* GetVariableByName(
   LPCSTR Name
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Name* 
</dt> <dd>

Typ: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Der Variablenname.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***

Ein Zeiger auf eine [**ID3DX11EffectVariable**](id3dx11effectvariable.md). Gibt eine ungültige Variable zurück, wenn der angegebene Name nicht gefunden werden kann.

## <a name="remarks"></a>Bemerkungen

Ein Effekt kann eine oder mehrere Variablen enthalten. Variablen außerhalb eines Verfahrens werden als Global für alle Effekte betrachtet, die sich innerhalb eines Verfahrens vor Ort befinden. Sie können auf eine Effekt Variable mithilfe Ihres Namens oder mit einem Index zugreifen.

Die-Methode gibt einen Zeiger auf eine [**Effekt Variable-Schnittstelle**](id3dx11effectvariable.md) zurück, unabhängig davon, ob eine Variable gefunden wird oder nicht. [**ID3DX11Effect:: IsValid**](id3dx11effect-isvalid.md) sollte aufgerufen werden, um zu überprüfen, ob der Name vorhanden ist.

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

 

