---
title: ID3DX11Effect-Schnittstelle (D3dx11effect.h)
description: Eine ID3DX11Effect-Schnittstelle verwaltet einen Satz von Zustandsobjekten, Ressourcen und Shadern für die Implementierung eines Renderingeffekts.
ms.assetid: 34429d51-6b45-4a62-bce1-50c4da02edac
keywords:
- ID3DX11Effect-Schnittstelle Direct3D 11
- ID3DX11Effect-Schnittstelle Direct3D 11 , beschrieben
topic_type:
- apiref
api_name:
- ID3DX11Effect
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4270059d02aec10905ea8aed7754bfb3a34c6897
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479146"
---
# <a name="id3dx11effect-interface"></a>ID3DX11Effect-Schnittstelle

Eine **ID3DX11Effect-Schnittstelle** verwaltet einen Satz von Zustandsobjekten, Ressourcen und Shadern für die Implementierung eines Renderingeffekts.

## <a name="members"></a>Member

Die **ID3DX11Effect-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **ID3DX11Effect** verfügt auch über diese Membertypen:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DX11Effect-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                     | BESCHREIBUNG                                                                               |
|:---------------------------------------------------------------------------|:------------------------------------------------------------------------------------------|
| [**CloneEffect**](id3dx11effect-cloneeffect.md)                           | Erstellt eine Kopie einer Effektschnittstelle.<br/>                                         |
| [**GetClassLinkage**](id3dx11effect-getclasslinkage.md)                   | Ruft eine Klassenverknüpfungsschnittstelle ab.<br/>                                                |
| [**GetConstantBufferByIndex**](id3dx11effect-getconstantbufferbyindex.md) | Sie erhalten einen konstanten Puffer nach Index.<br/>                                                |
| [**GetConstantBufferByName**](id3dx11effect-getconstantbufferbyname.md)   | Sie erhalten einen konstanten Puffer nach Namen.<br/>                                                 |
| [**GetDesc**](id3dx11effect-getdesc.md)                                   | Eine Beschreibung des Effekts wird angezeigt.<br/>                                                     |
| [**GetDevice**](id3dx11effect-getdevice.md)                               | Sie erhalten das Gerät, das den Effekt erstellt hat.<br/>                                        |
| [**GetGroupByIndex**](id3dx11effect-getgroupbyindex.md)                   | Ruft eine Effektgruppe nach Index ab.<br/>                                                 |
| [**GetGroupByName**](id3dx11effect-getgroupbyname.md)                     | Ruft eine Effektgruppe nach Namen ab.<br/>                                                  |
| [**GetTechniqueByIndex**](id3dx11effect-gettechniquebyindex.md)           | Hier erhalten Sie eine Technik nach Index.<br/>                                                      |
| [**GetTechniqueByName**](id3dx11effect-gettechniquebyname.md)             | Hier erhalten Sie eine Technik nach Namen.<br/>                                                       |
| [**GetVariableByIndex**](id3dx11effect-getvariablebyindex.md)             | Hier wird eine Variable nach Index erhalten.<br/>                                                       |
| [**GetVariableByName**](id3dx11effect-getvariablebyname.md)               | Hier erhalten Sie eine Variable nach Namen.<br/>                                                        |
| [**GetVariableBySemantic**](id3dx11effect-getvariablebysemantic.md)       | Eine Variable wird semantisch erhalten.<br/>                                                    |
| [**IsOptimized**](id3dx11effect-isoptimized.md)                           | Testen Sie einen Effekt, um zu prüfen, ob die Reflektionsmetadaten aus dem Arbeitsspeicher entfernt wurden.<br/> |
| [**IsValid**](id3dx11effect-isvalid.md)                                   | Testen Sie einen Effekt, um zu überprüfen, ob er eine gültige Syntax enthält.<br/>                             |
| [**Optimieren**](id3dx11effect-optimize.md)                                 | Minimieren Sie die Menge an Arbeitsspeicher, die für einen Effekt erforderlich ist.<br/>                          |



 

## <a name="remarks"></a>Hinweise

Ein Effekt wird durch Aufrufen von [**D3DX11CreateEffectFromMemory erstellt.**](d3dx11createeffectfrommemory.md)

Das Effektsystem unterteilt die zum Rendern erforderlichen Informationen in einen Effekt, der: Zustandsobjekte zum Zuweisen von Zustandsänderungen in Gruppen, Ressourcen zum Liefern von Eingabedaten und Speichern von Ausgabedaten sowie Programme, die steuern, wie das Rendering erfolgt, genannt Shader.

> [!Note]  
> Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit. Sie müssen die Quelle Effects 11 verwenden, um Ihre Effekttypanwendung zu erstellen. Weitere Informationen zur Verwendung der Quelle Effects 11 finden Sie unter [Unterschiede zwischen Effekten 10 und Effekten 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

> [!Note]
>
> Wenn Sie [**QueryInterface für**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) ein **ID3DX11Effect-Objekt** aufrufen, um die [**IUnknown-Schnittstelle**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) abzurufen, **gibt QueryInterface** E \_ NOINTERFACE zurück. Um dieses Problem zu beheben, verwenden Sie den folgenden Code:
>
> <span codelanguage=""></span>
>
> 
| | | <pre><code>    IUnknown* pIUnknown = (IUnknown*)pEffect;&gt;     pIUnknown-&gt;AddRef();</code></pre> | 

>
> 
>
>  

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-------------|-------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Bibliothek<br/> | <dl> <dt>Nicht verfügbar (eine Effects 11-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt> </dl> |

## <a name="see-also"></a>Weitere Informationen

[Effekte 11 Schnittstellen](d3d11-graphics-reference-effects11-interfaces.md)

[D3DX-Schnittstellen](d3d11-graphics-reference-d3dx11-interfaces.md)
