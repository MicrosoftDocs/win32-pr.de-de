---
title: ID3DX11Effect GetVariableByName-Methode (D3dx11effect.h)
description: Abrufen einer Variablen anhand des Namens.
ms.assetid: d20c5a85-51a5-482f-b5b0-197d8e993910
keywords:
- GetVariableByName-Methode Direct3D 11
- GetVariableByName-Methode Direct3D 11, ID3DX11Effect-Schnittstelle
- ID3DX11Effect-Schnittstelle Direct3D 11 , GetVariableByName-Methode
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
ms.openlocfilehash: b3e8741eaf2ced1022a130ecb94c7f8553159e862ca23b50ba4d12786ad37620
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118099043"
---
# <a name="id3dx11effectgetvariablebyname-method"></a>ID3DX11Effect::GetVariableByName-Methode

Abrufen einer Variablen anhand des Namens.

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

## <a name="remarks"></a>Hinweise

Ein Effekt kann eine oder mehrere Variablen enthalten. Variablen außerhalb einer Technik werden für alle Effekte als global betrachtet, diejenigen, die sich innerhalb einer Technik befinden, sind für diese Technik lokal. Sie können auf eine Effektvariable mit ihrem Namen oder mit einem Index zugreifen.

Die -Methode gibt einen Zeiger auf eine [**Effektvariablenschnittstelle**](id3dx11effectvariable.md) zurück, unabhängig davon, ob eine Variable gefunden wird oder nicht. [**ID3DX11Effect::IsValid**](id3dx11effect-isvalid.md) sollte aufgerufen werden, um zu überprüfen, ob der Name vorhanden ist.

> [!Note]  
> Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte zur Verfügung. Sie müssen die Effects 11-Quelle verwenden, um ihre Effekte-Typ-Anwendung zu erstellen. Weitere Informationen zur Verwendung der Quelle Effects 11 finden Sie unter [Unterschiede zwischen Effekten 10 und Effekten 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Bibliothek<br/> | <dl> <dt>N/A (Eine Effects 11-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DX11Effect](id3dx11effect.md)
</dt> </dl>

 

