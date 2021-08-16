---
title: ID3DX11EffectType-Schnittstelle (D3dx11effect.h)
description: Die ID3DX11EffectType-Schnittstelle greift auf Effektvariablen nach Typ zu. Die Lebensdauer eines ID3DX11EffectType-Objekts entspricht der Lebensdauer des übergeordneten ID3DX11Effect-Objekts.
ms.assetid: 700076ee-a5fe-4af2-a5f4-053c05d8ddf0
keywords:
- ID3DX11EffectType-Schnittstelle Direct3D 11
- ID3DX11EffectType-Schnittstelle Direct3D 11 , beschrieben
topic_type:
- apiref
api_name:
- ID3DX11EffectType
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d397f856fec49cf9909cd7089a1067250e78ca3f97c72d913d0ffdc146efb93
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118532147"
---
# <a name="id3dx11effecttype-interface"></a>ID3DX11EffectType-Schnittstelle

Die **ID3DX11EffectType-Schnittstelle** greift auf Effektvariablen nach Typ zu.

Die Lebensdauer eines **ID3DX11EffectType-Objekts** entspricht der Lebensdauer des übergeordneten [**ID3DX11Effect-Objekts.**](id3dx11effect.md)

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DX11EffectType-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                       | BESCHREIBUNG                                       |
|:-----------------------------------------------------------------------------|:--------------------------------------------------|
| [**GetDesc**](id3dx11effecttype-getdesc.md)                                 | Abrufen einer Beschreibung des Effekttyps.<br/>        |
| [**GetMemberName**](id3dx11effecttype-getmembername.md)                     | Abrufen des Namens eines Members.<br/>              |
| [**GetMemberSemantic**](id3dx11effecttype-getmembersemantic.md)             | Abrufen der an einen Member angefügten Semantik.<br/> |
| [**GetMemberTypeByIndex**](id3dx11effecttype-getmembertypebyindex.md)       | Abrufen eines Membertyps nach Index.<br/>            |
| [**GetMemberTypeByName**](id3dx11effecttype-getmembertypebyname.md)         | Abrufen eines Membertyps anhand des Namens.<br/>            |
| [**GetMemberTypeBySemantic**](id3dx11effecttype-getmembertypebysemantic.md) | Abrufen eines Membertyps nach Semantik.<br/>         |
| [**IsValid**](id3dx11effecttype-isvalid.md)                                 | Testet, dass der Effekttyp gültig ist.<br/>   |



 

## <a name="remarks"></a>Hinweise

Um Informationen zu einem Effekttyp aus einer Effektvariablen abzurufen, rufen [**Sie ID3DX11EffectVariable::GetType**](id3dx11effectvariable-gettype.md)auf.

> [!Note]  
> Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte zur Verfügung. Sie müssen die Effects 11-Quelle verwenden, um ihre Effekte-Typ-Anwendung zu erstellen. Weitere Informationen zur Verwendung der Quelle Effects 11 finden Sie unter [Unterschiede zwischen Effekten 10 und Effekten 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Bibliothek<br/> | <dl> <dt>N/A (Eine Effects 11-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Effekte 11 Schnittstellen](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[D3DX-Schnittstellen](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





