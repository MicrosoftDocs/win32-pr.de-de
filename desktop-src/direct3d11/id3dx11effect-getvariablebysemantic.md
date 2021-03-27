---
title: ID3DX11Effect getvariablebysemantic-Methode (D3dx11effect. h)
description: Eine Variable nach Semantik erhalten.
ms.assetid: fe731af6-3e9b-4f3e-9761-121796ac8c48
keywords:
- Getvariablebysemantic-Methode Direct3D 11
- Getvariablebysemantic-Methode Direct3D 11, ID3DX11Effect-Schnittstelle
- ID3DX11Effect-Schnittstelle Direct3D 11, getvariablebysemantic-Methode
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
ms.openlocfilehash: b8276b1850242bd83639883bf75fc927d8484765
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219644"
---
# <a name="id3dx11effectgetvariablebysemantic-method"></a>ID3DX11Effect:: getvariablebysemantic-Methode

Eine Variable nach Semantik erhalten.

## <a name="syntax"></a>Syntax


```C++
ID3DX11EffectVariable* GetVariableBySemantic(
   LPCSTR Semantic
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Tischer* 
</dt> <dd>

Typ: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Der semantische Name.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***

Ein Zeiger auf die von der Semantik angegeben Effekt Variable. Siehe [**ID3DX11EffectVariable**](id3dx11effectvariable.md).

## <a name="remarks"></a>Bemerkungen

Jeder Effekt Variablen kann eine Semantik angefügt werden, die eine benutzerdefinierte Metadatenzeichenfolge ist. Einige [System-Wert-Semantik](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics) sind reservierte Wörter, die integrierte Funktionen nach Pipeline Stufen auslöst.

Die-Methode gibt einen Zeiger auf eine [**Effekt Variable-Schnittstelle**](id3dx11effectvariable.md) zurück, wenn eine Variable nicht gefunden wird. Sie können [**ID3DX11Effect:: IsValid**](id3dx11effect-isvalid.md) aufgerufen, um zu überprüfen, ob die Semantik vorhanden ist.

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

 

