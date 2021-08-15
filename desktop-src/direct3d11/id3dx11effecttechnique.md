---
title: ID3DX11EffectTechnique-Schnittstelle (D3dx11effect.h)
description: Eine ID3DX11EffectTechnique-Schnittstelle ist eine Auflistung von Durchläufen. Die Lebensdauer eines ID3DX11EffectTechnique-Objekts entspricht der Lebensdauer des übergeordneten ID3DX11Effect-Objekts.
ms.assetid: 63d52cac-287d-4432-bf2b-7b4e67e525e6
keywords:
- ID3DX11EffectTechnique-Schnittstelle Direct3D 11
- ID3DX11EffectTechnique-Schnittstelle Direct3D 11 , beschrieben
topic_type:
- apiref
api_name:
- ID3DX11EffectTechnique
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d8970ad1e75f37e8270a013d3830216ae128e41c03d4ad5245ac6ffc7615691
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118532352"
---
# <a name="id3dx11effecttechnique-interface"></a>ID3DX11EffectTechnique-Schnittstelle

Eine **ID3DX11EffectTechnique-Schnittstelle** ist eine Auflistung von Durchläufen.

Die Lebensdauer eines **ID3DX11EffectTechnique-Objekts** entspricht der Lebensdauer des übergeordneten [**ID3DX11Effect-Objekts.**](id3dx11effect.md)

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DX11EffectTechnique-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                        | BESCHREIBUNG                                                           |
|:------------------------------------------------------------------------------|:----------------------------------------------------------------------|
| [**ComputeStateBlockMask**](id3dx11effecttechnique-computestateblockmask.md) | Berechnen Sie eine Zustandsblockmaske, um Zustandsänderungen zu ermöglichen bzw. zu verhindern.<br/> |
| [**GetAnnotationByIndex**](id3dx11effecttechnique-getannotationbyindex.md)   | Sie erhalten eine Anmerkung nach Index.<br/>                                |
| [**GetAnnotationByName**](id3dx11effecttechnique-getannotationbyname.md)     | Erhalten Sie eine Anmerkung nach Namen.<br/>                                 |
| [**GetDesc**](id3dx11effecttechnique-getdesc.md)                             | Erhalten Sie eine Technikbeschreibung.<br/>                               |
| [**GetPassByIndex**](id3dx11effecttechnique-getpassbyindex.md)               | Get a pass by index (Index für Pass-by-Index).<br/>                                       |
| [**GetPassByName**](id3dx11effecttechnique-getpassbyname.md)                 | Erhalten Sie einen Pass nach Name.<br/>                                        |
| [**IsValid**](id3dx11effecttechnique-isvalid.md)                             | Testen Sie eine Technik, um zu überprüfen, ob sie eine gültige Syntax enthält.<br/>       |



 

## <a name="remarks"></a>Hinweise

Ein Effekt enthält eine oder mehrere Techniken. jede Technik enthält einen oder mehrere Durchläufe. Jeder Durchgang enthält Zustandszuweisungen.

Um eine Effekttechnikschnittstelle zu erhalten, rufen Sie eine Methode wie [**ID3DX11Effect::GetTechniqueByName auf.**](id3dx11effect-gettechniquebyname.md)

> [!Note]  
> Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit. Sie müssen die Quelle Effects 11 verwenden, um Ihre Effekttypanwendung zu erstellen. Weitere Informationen zur Verwendung der Quelle Effects 11 finden Sie unter [Unterschiede zwischen Effekten 10 und Effekten 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Bibliothek<br/> | <dl> <dt>Nicht verfügbar (eine Effects 11-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Effekte 11 Schnittstellen](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[D3DX-Schnittstellen](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





