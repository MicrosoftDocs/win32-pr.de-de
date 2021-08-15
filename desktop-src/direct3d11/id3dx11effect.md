---
title: ID3DX11Effect-Schnittstelle (D3dx11effect.h)
description: Eine ID3DX11Effect-Schnittstelle verwaltet eine Reihe von Zustandsobjekten, Ressourcen und Shadern für die Implementierung eines Renderingeffekts.
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
ms.openlocfilehash: 670e60cf68c812b6d8b296aac41c3000fa8c1405c909e8827532625a6cd93b0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118535928"
---
# <a name="id3dx11effect-interface"></a>ID3DX11Effect-Schnittstelle

Eine **ID3DX11Effect-Schnittstelle** verwaltet eine Reihe von Zustandsobjekten, Ressourcen und Shadern für die Implementierung eines Renderingeffekts.

## <a name="members"></a>Member

Die **ID3DX11Effect-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **ID3DX11Effect** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DX11Effect-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                     | BESCHREIBUNG                                                                               |
|:---------------------------------------------------------------------------|:------------------------------------------------------------------------------------------|
| [**CloneEffect**](id3dx11effect-cloneeffect.md)                           | Erstellt eine Kopie einer Effektschnittstelle.<br/>                                         |
| [**GetClassLinkage**](id3dx11effect-getclasslinkage.md)                   | Ruft eine Klassenbindungsschnittstelle ab.<br/>                                                |
| [**GetConstantBufferByIndex**](id3dx11effect-getconstantbufferbyindex.md) | Abrufen eines konstanten Puffers nach Index.<br/>                                                |
| [**GetConstantBufferByName**](id3dx11effect-getconstantbufferbyname.md)   | Abrufen eines konstanten Puffers anhand des Namens.<br/>                                                 |
| [**GetDesc**](id3dx11effect-getdesc.md)                                   | Abrufen einer Effektbeschreibung.<br/>                                                     |
| [**GetDevice**](id3dx11effect-getdevice.md)                               | Abrufen des Geräts, das den Effekt erstellt hat.<br/>                                        |
| [**GetGroupByIndex**](id3dx11effect-getgroupbyindex.md)                   | Ruft eine Effektgruppe nach Index ab.<br/>                                                 |
| [**GetGroupByName**](id3dx11effect-getgroupbyname.md)                     | Ruft eine Effektgruppe nach Namen ab.<br/>                                                  |
| [**GetTechniqueByIndex**](id3dx11effect-gettechniquebyindex.md)           | Abrufen einer Technik nach Index.<br/>                                                      |
| [**GetTechniqueByName**](id3dx11effect-gettechniquebyname.md)             | Abrufen einer Technik anhand des Namens.<br/>                                                       |
| [**GetVariableByIndex**](id3dx11effect-getvariablebyindex.md)             | Abrufen einer Variablen nach Index.<br/>                                                       |
| [**GetVariableByName**](id3dx11effect-getvariablebyname.md)               | Abrufen einer Variablen anhand des Namens.<br/>                                                        |
| [**GetVariableBySemantic**](id3dx11effect-getvariablebysemantic.md)       | Abrufen einer Variablen nach Semantik.<br/>                                                    |
| [**IsOptimized**](id3dx11effect-isoptimized.md)                           | Testen Sie einen Effekt, um festzustellen, ob die Reflektionsmetadaten aus dem Arbeitsspeicher entfernt wurden.<br/> |
| [**IsValid**](id3dx11effect-isvalid.md)                                   | Testen Sie einen Effekt, um festzustellen, ob er eine gültige Syntax enthält.<br/>                             |
| [**Optimieren**](id3dx11effect-optimize.md)                                 | Minimieren Sie den für einen Effekt erforderlichen Arbeitsspeicher.<br/>                          |



 

## <a name="remarks"></a>Hinweise

Ein Effekt wird durch Aufrufen von [**D3DX11CreateEffectFromMemory**](d3dx11createeffectfrommemory.md)erstellt.

Das Effect-System gruppiert die für das Rendern erforderlichen Informationen in einen Effekt, der Folgendes enthält: Zustandsobjekte zum Zuweisen von Zustandsänderungen in Gruppen, Ressourcen zum Bereitstellen von Eingabedaten und Speichern von Ausgabedaten und Programme, die steuern, wie das Rendering durchgeführt wird, als Shader bezeichnet.

> [!Note]  
> Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte zur Verfügung. Sie müssen die Effects 11-Quelle verwenden, um ihre Effekte-Typ-Anwendung zu erstellen. Weitere Informationen zur Verwendung der Quelle Effects 11 finden Sie unter [Unterschiede zwischen Effekten 10 und Effekten 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

> [!Note]
>
> Wenn Sie [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) für ein **ID3DX11Effect-Objekt** aufrufen, um die [**IUnknown-Schnittstelle**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) abzurufen, gibt **QueryInterface** E \_ NOINTERFACE zurück. Verwenden Sie den folgenden Code, um dieses Problem zu umgehen:
>
> <span codelanguage=""></span>
>
> <table>
> <colgroup>
> <col style="width: 100%" />
> </colgroup>
> <tbody>
> <tr class="odd">
> <td><pre><code>    IUnknown* pIUnknown = (IUnknown*)pEffect;
>     pIUnknown->AddRef();</code></pre></td>
> </tr>
> </tbody>
> </table>>
>  

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-------------|-------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Bibliothek<br/> | <dl> <dt>N/A (Eine Effects 11-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt> </dl> |

## <a name="see-also"></a>Weitere Informationen

[Effekte 11 Schnittstellen](d3d11-graphics-reference-effects11-interfaces.md)

[D3DX-Schnittstellen](d3d11-graphics-reference-d3dx11-interfaces.md)
