---
title: ID3DX11EffectTechnique-Schnittstelle (D3dx11effect. h)
description: Eine ID3DX11EffectTechnique-Schnittstelle ist eine Auflistung von Durchläufen. Die Lebensdauer eines ID3DX11EffectTechnique-Objekts entspricht der Lebensdauer seines übergeordneten ID3DX11Effect-Objekts.
ms.assetid: 63d52cac-287d-4432-bf2b-7b4e67e525e6
keywords:
- ID3DX11EffectTechnique-Schnittstelle Direct3D 11
- ID3DX11EffectTechnique Interface Direct3D 11, beschrieben
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
ms.openlocfilehash: e582d8f94b2dbcbb2052a8cf3a59d8ba514367cc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982540"
---
# <a name="id3dx11effecttechnique-interface"></a>ID3DX11EffectTechnique-Schnittstelle

Eine **ID3DX11EffectTechnique** -Schnittstelle ist eine Auflistung von Durchläufen.

Die Lebensdauer eines **ID3DX11EffectTechnique** -Objekts entspricht der Lebensdauer seines übergeordneten [**ID3DX11Effect**](id3dx11effect.md) -Objekts.

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DX11EffectTechnique** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                        | BESCHREIBUNG                                                           |
|:------------------------------------------------------------------------------|:----------------------------------------------------------------------|
| [**Computestateblockmask**](id3dx11effecttechnique-computestateblockmask.md) | Berechnen Sie eine Zustands Block Maske, um Zustandsänderungen zuzulassen/zu verhindern.<br/> |
| [**Getannotationbyindex**](id3dx11effecttechnique-getannotationbyindex.md)   | Eine Anmerkung nach Index erhalten.<br/>                                |
| [**Getannotationbyname**](id3dx11effecttechnique-getannotationbyname.md)     | Eine Anmerkung anhand des Namens erhalten.<br/>                                 |
| [**GetDesc**](id3dx11effecttechnique-getdesc.md)                             | Hier finden Sie eine Technik Beschreibung.<br/>                               |
| [**Getpassbyindex**](id3dx11effecttechnique-getpassbyindex.md)               | Einen Pass-by-Index erhalten.<br/>                                       |
| [**Getpassbyname**](id3dx11effecttechnique-getpassbyname.md)                 | Einen Pass-Through-Namen erhalten.<br/>                                        |
| [**IsValid**](id3dx11effecttechnique-isvalid.md)                             | Testen Sie eine Technik, um festzustellen, ob Sie eine gültige Syntax enthält.<br/>       |



 

## <a name="remarks"></a>Bemerkungen

Ein Effekt enthält mindestens eine Technik. jede Technik enthält einen oder mehrere Durchgänge. Jeder Durchlauf enthält Zustands Zuweisungen.

Um eine Wirkungs Technik-Schnittstelle zu erhalten, müssen Sie eine Methode wie [**ID3DX11Effect:: gettechniquebyname**](id3dx11effect-gettechniquebyname.md)aufrufen.

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

 

 





