---
title: ID3DX11EffectGroup-Schnittstelle (D3dx11effect.h)
description: Die ID3DX11EffectGroup-Schnittstelle greifen auf eine Effect-Gruppe zu. Die Lebensdauer eines ID3DX11EffectGroup-Objekts entspricht der Lebensdauer des übergeordneten ID3DX11Effect-Objekts.
ms.assetid: f5a35c47-0bac-4559-bd6c-5e8bc7699e10
keywords:
- ID3DX11EffectGroup-Schnittstelle Direct3D 11
- ID3DX11EffectGroup-Schnittstelle Direct3D 11 , beschrieben
topic_type:
- apiref
api_name:
- ID3DX11EffectGroup
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fa42a884be0abd15f0d16403a95d859d89cd472fc630b51ffe586e703e1a8ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119046228"
---
# <a name="id3dx11effectgroup-interface"></a>ID3DX11EffectGroup-Schnittstelle

Die **ID3DX11EffectGroup-Schnittstelle** greifen auf eine Effect-Gruppe zu.

Die Lebensdauer eines **ID3DX11EffectGroup-Objekts** entspricht der Lebensdauer des übergeordneten [**ID3DX11Effect-Objekts.**](id3dx11effect.md)

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DX11EffectGroup-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                  | Beschreibung                                                   |
|:------------------------------------------------------------------------|:--------------------------------------------------------------|
| [**GetAnnotationByIndex**](id3dx11effectgroup-getannotationbyindex.md) | Sie erhalten eine Anmerkung nach Index.<br/>                        |
| [**GetAnnotationByName**](id3dx11effectgroup-getannotationbyname.md)   | Erhalten Sie eine Anmerkung nach Namen.<br/>                         |
| [**GetDesc**](id3dx11effectgroup-getdesc.md)                           | Ruft eine Gruppenbeschreibung ab.<br/>                          |
| [**GetTechniqueByIndex**](id3dx11effectgroup-gettechniquebyindex.md)   | Hier erhalten Sie eine Technik nach Index.<br/>                          |
| [**GetTechniqueByName**](id3dx11effectgroup-gettechniquebyname.md)     | Hier erhalten Sie eine Technik nach Namen.<br/>                           |
| [**IsValid**](id3dx11effectgroup-isvalid.md)                           | Testen Sie einen Effekt, um zu überprüfen, ob er eine gültige Syntax enthält.<br/> |



 

## <a name="remarks"></a>Hinweise

Um eine **ID3DX11EffectGroup-Schnittstelle zu** erhalten, rufen Sie eine Methode wie [**ID3DX11Effect::GetGroupByName auf.**](id3dx11effect-getgroupbyname.md)

> [!Note]  
> Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit. Sie müssen die Quelle Effects 11 verwenden, um Ihre Effekttypanwendung zu erstellen. Weitere Informationen zur Verwendung der Quelle Effects 11 finden Sie unter [Unterschiede zwischen Effekten 10 und Effekten 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Bibliothek<br/> | <dl> <dt>Nicht verfügbar (eine Effects 11-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Effekte 11 Schnittstellen](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[D3DX-Schnittstellen](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





