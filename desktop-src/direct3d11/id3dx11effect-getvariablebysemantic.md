---
title: ID3DX11Effect GetVariableBySemantic-Methode (D3dx11effect.h)
description: Eine Variable wird semantisch erhalten.
ms.assetid: fe731af6-3e9b-4f3e-9761-121796ac8c48
keywords:
- GetVariableBySemantic-Methode Direct3D 11
- GetVariableBySemantic-Methode Direct3D 11, ID3DX11Effect-Schnittstelle
- ID3DX11Effect-Schnittstelle Direct3D 11, GetVariableBySemantic-Methode
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetVariableBySemantic
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e1a636b4a5d9ca4094167e81a74d316e2b57f14e5dacd5926897f8190d50405
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118808092"
---
# <a name="id3dx11effectgetvariablebysemantic-method"></a>ID3DX11Effect::GetVariableBySemantic-Methode

Eine Variable wird semantisch erhalten.

## <a name="syntax"></a>Syntax


```C++
ID3DX11EffectVariable* GetVariableBySemantic(
   LPCSTR Semantic
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Semantische* 
</dt> <dd>

Typ: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Der semantische Name.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***

Ein Zeiger auf die durch die Semantik angegebene Effektvariable. Siehe [**ID3DX11EffectVariable**](id3dx11effectvariable.md).

## <a name="remarks"></a>Hinweise

An jede Effektvariable kann eine semantische Variable angefügt werden, bei der es sich um eine benutzerdefinierte Metadatenzeichenfolge handelt. Einige [Systemwertsemantiken sind](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics) reservierte Wörter, die integrierte Funktionen nach Pipelinestufen auslösen.

Die -Methode gibt einen Zeiger auf eine [**Effect-Variable-Schnittstelle zurück,**](id3dx11effectvariable.md) wenn keine Variable gefunden wird. Sie können [**ID3DX11Effect::IsValid**](id3dx11effect-isvalid.md) aufrufen, um zu überprüfen, ob die Semantik vorhanden ist.

> [!Note]  
> Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit. Sie müssen die Quelle Effects 11 verwenden, um Ihre Effekttypanwendung zu erstellen. Weitere Informationen zur Verwendung der Quelle Effects 11 finden Sie unter [Unterschiede zwischen Effekten 10 und Effekten 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Bibliothek<br/> | <dl> <dt>Nicht verfügbar (eine Effects 11-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DX11Effect](id3dx11effect.md)
</dt> </dl>

 

