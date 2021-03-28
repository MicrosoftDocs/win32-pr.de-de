---
title: ID3DX11EffectType-Schnittstelle (D3dx11effect. h)
description: Die ID3DX11EffectType-Schnittstelle greift auf die Effekt Variablen nach Typ zu. Die Lebensdauer eines ID3DX11EffectType-Objekts entspricht der Lebensdauer seines übergeordneten ID3DX11Effect-Objekts.
ms.assetid: 700076ee-a5fe-4af2-a5f4-053c05d8ddf0
keywords:
- ID3DX11EffectType-Schnittstelle Direct3D 11
- ID3DX11EffectType Interface Direct3D 11, beschrieben
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
ms.openlocfilehash: 4e3c210ca60abc9e55b8864a2b121cf92be369a3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103761982"
---
# <a name="id3dx11effecttype-interface"></a>ID3DX11EffectType-Schnittstelle

Die **ID3DX11EffectType** -Schnittstelle greift auf die Effekt Variablen nach Typ zu.

Die Lebensdauer eines **ID3DX11EffectType** -Objekts entspricht der Lebensdauer seines übergeordneten [**ID3DX11Effect**](id3dx11effect.md) -Objekts.

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DX11EffectType** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                       | BESCHREIBUNG                                       |
|:-----------------------------------------------------------------------------|:--------------------------------------------------|
| [**GetDesc**](id3dx11effecttype-getdesc.md)                                 | Geben Sie eine Beschreibung des Effekt Typs an.<br/>        |
| [**Getmembership Name**](id3dx11effecttype-getmembername.md)                     | Den Namen eines Members zu erhalten.<br/>              |
| [**Getmembership Semantic**](id3dx11effecttype-getmembersemantic.md)             | Die an einen Member angefügte Semantik wird angezeigt.<br/> |
| [**GetMemberTypeByIndex**](id3dx11effecttype-getmembertypebyindex.md)       | Einen Elementtyp nach Index erhalten.<br/>            |
| [**GetMemberTypeByName**](id3dx11effecttype-getmembertypebyname.md)         | Einen Elementtyp nach Name erhalten.<br/>            |
| [**Getmembership typebysemantic**](id3dx11effecttype-getmembertypebysemantic.md) | Einen Elementtyp nach Semantik erhalten.<br/>         |
| [**IsValid**](id3dx11effecttype-isvalid.md)                                 | Testet, ob der Effekts-Typ gültig ist.<br/>   |



 

## <a name="remarks"></a>Bemerkungen

Zum Abrufen von Informationen zu einem Effekts-Typ aus einer Effekt Variablen, aufrufen Sie [**ID3DX11EffectVariable:: GetType**](id3dx11effectvariable-gettype.md).

> [!Note]  
> Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit. Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen. Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Bibliothek<br/> | <dl> <dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Effekte 11-Schnittstellen](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[D3DX-Schnittstellen](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





