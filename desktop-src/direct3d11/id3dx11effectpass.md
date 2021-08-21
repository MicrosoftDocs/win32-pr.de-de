---
title: ID3DX11EffectPass-Schnittstelle (D3dx11effect.h)
description: Eine ID3DX11EffectPass-Schnittstelle kapselt Zustandszuweisungen innerhalb einer Technik. Die Lebensdauer eines ID3DX11EffectPass-Objekts entspricht der Lebensdauer des übergeordneten ID3DX11Effect-Objekts.
ms.assetid: 4d86c362-b0f8-4396-86de-c7c89710f46d
keywords:
- ID3DX11EffectPass-Schnittstelle Direct3D 11
- ID3DX11EffectPass-Schnittstelle Direct3D 11 , beschrieben
topic_type:
- apiref
api_name:
- ID3DX11EffectPass
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33b24fe0154e447cd993e8e7e939a9a023ed37183a56980dab8f5d803a0ea41e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045975"
---
# <a name="id3dx11effectpass-interface"></a>ID3DX11EffectPass-Schnittstelle

Eine **ID3DX11EffectPass-Schnittstelle** kapselt Zustandszuweisungen innerhalb einer Technik.

Die Lebensdauer eines **ID3DX11EffectPass-Objekts** entspricht der Lebensdauer des übergeordneten [**ID3DX11Effect-Objekts.**](id3dx11effect.md)

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DX11EffectPass-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                   | Beschreibung                                                       |
|:-------------------------------------------------------------------------|:------------------------------------------------------------------|
| [**Anwenden**](id3dx11effectpass-apply.md)                                 | Legen Sie den Zustand fest, der in einem Pass an das Gerät enthalten ist.<br/>       |
| [**ComputeStateBlockMask**](id3dx11effectpass-computestateblockmask.md) | Generieren Sie eine Maske zum Zulassen/Verhindern von Zustandsänderungen.<br/> |
| [**GetAnnotationByIndex**](id3dx11effectpass-getannotationbyindex.md)   | Sie erhalten eine Anmerkung nach Index.<br/>                            |
| [**GetAnnotationByName**](id3dx11effectpass-getannotationbyname.md)     | Erhalten Sie eine Anmerkung nach Namen.<br/>                             |
| [**GetComputeShaderDesc**](id3dx11effectpass-getcomputeshaderdesc.md)   | Hier finden Sie eine Beschreibung des Compute-Shaders.<br/>                      |
| [**GetDesc**](id3dx11effectpass-getdesc.md)                             | Hier erhalten Sie eine Passbeschreibung.<br/>                                |
| [**GetDomainShaderDesc**](id3dx11effectpass-getdomainshaderdesc.md)     | Hier erhalten Sie eine Domänen-Shader-Beschreibung.<br/>                       |
| [**GetGeometryShaderDesc**](id3dx11effectpass-getgeometryshaderdesc.md) | Hier erhalten Sie eine Geometry-Shader-Beschreibung.<br/>                     |
| [**GetHullShaderDesc**](id3dx11effectpass-gethullshaderdesc.md)         | Hier finden Sie eine Beschreibung für den Hüllen-Shader.<br/>                           |
| [**GetPixelShaderDesc**](id3dx11effectpass-getpixelshaderdesc.md)       | Hier erhalten Sie eine Pixel-Shader-Beschreibung.<br/>                        |
| [**GetVertexShaderDesc**](id3dx11effectpass-getvertexshaderdesc.md)     | Hier finden Sie eine Vertex-Shader-Beschreibung.<br/>                       |
| [**IsValid**](id3dx11effectpass-isvalid.md)                             | Testen Sie einen Pass, um zu überprüfen, ob er eine gültige Syntax enthält.<br/>        |



 

## <a name="remarks"></a>Hinweise

Ein Durchgang ist ein Codeblock, der Renderzustandsobjekte und Shader fest legt. Ein Durchgang wird innerhalb einer Technik deklariert.

Um eine Effektpassschnittstelle zu erhalten, rufen Sie eine Methode wie [**ID3DX11EffectTechnique::GetPassByName auf.**](id3dx11effecttechnique-getpassbyname.md)

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

 

 





