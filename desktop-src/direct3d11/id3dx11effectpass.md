---
title: ID3DX11EffectPass-Schnittstelle (D3dx11effect. h)
description: Eine ID3DX11EffectPass-Schnittstelle kapselt Zustands Zuweisungen innerhalb eines Verfahrens. Die Lebensdauer eines ID3DX11EffectPass-Objekts entspricht der Lebensdauer seines übergeordneten ID3DX11Effect-Objekts.
ms.assetid: 4d86c362-b0f8-4396-86de-c7c89710f46d
keywords:
- ID3DX11EffectPass-Schnittstelle Direct3D 11
- ID3DX11EffectPass Interface Direct3D 11, beschrieben
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
ms.openlocfilehash: a26732543d1033cfc439755df6ac397d2a28ec1b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219648"
---
# <a name="id3dx11effectpass-interface"></a>ID3DX11EffectPass-Schnittstelle

Eine **ID3DX11EffectPass** -Schnittstelle kapselt Zustands Zuweisungen innerhalb eines Verfahrens.

Die Lebensdauer eines **ID3DX11EffectPass** -Objekts entspricht der Lebensdauer seines übergeordneten [**ID3DX11Effect**](id3dx11effect.md) -Objekts.

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DX11EffectPass** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                   | BESCHREIBUNG                                                       |
|:-------------------------------------------------------------------------|:------------------------------------------------------------------|
| [**Anwenden**](id3dx11effectpass-apply.md)                                 | Legen Sie den in einem Pass enthaltenen Status auf das Gerät fest.<br/>       |
| [**Computestateblockmask**](id3dx11effectpass-computestateblockmask.md) | Generiert eine Maske zum zulassen/verhindern von Zustandsänderungen.<br/> |
| [**Getannotationbyindex**](id3dx11effectpass-getannotationbyindex.md)   | Eine Anmerkung nach Index erhalten.<br/>                            |
| [**Getannotationbyname**](id3dx11effectpass-getannotationbyname.md)     | Eine Anmerkung anhand des Namens erhalten.<br/>                             |
| [**Getcomputeshaderentsc**](id3dx11effectpass-getcomputeshaderdesc.md)   | Eine COMPUTE-shaderbeschreibung erhalten.<br/>                      |
| [**GetDesc**](id3dx11effectpass-getdesc.md)                             | Eine Pass Beschreibung erhalten.<br/>                                |
| [**Getdomainshaderdebug**](id3dx11effectpass-getdomainshaderdesc.md)     | Eine Domänen-Shader-Beschreibung erhalten.<br/>                       |
| [**Getgeometryshaderdebug**](id3dx11effectpass-getgeometryshaderdesc.md) | Eine Geometry-shaderbeschreibung erhalten.<br/>                     |
| [**Gethullshaderdebug**](id3dx11effectpass-gethullshaderdesc.md)         | Die Beschreibung von "Hull-Shader" wird angezeigt.<br/>                           |
| [**Getpixelshaderdebug**](id3dx11effectpass-getpixelshaderdesc.md)       | Eine Pixel-shaderbeschreibung erhalten.<br/>                        |
| [**Getvertexshaderdebug**](id3dx11effectpass-getvertexshaderdesc.md)     | Eine Vertex-shaderbeschreibung erhalten.<br/>                       |
| [**IsValid**](id3dx11effectpass-isvalid.md)                             | Testen Sie einen Durchlauf, um festzustellen, ob er eine gültige Syntax enthält.<br/>        |



 

## <a name="remarks"></a>Bemerkungen

Ein Durchlauf ist ein Codeblock, der renderstatusobjekte und Shader festlegt. Ein Durchlauf wird innerhalb einer Technik deklariert.

Um eine Effect-Pass-Schnittstelle zu erhalten, müssen Sie eine Methode wie [**ID3DX11EffectTechnique:: getpassbyname**](id3dx11effecttechnique-getpassbyname.md)aufrufen.

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

 

 





