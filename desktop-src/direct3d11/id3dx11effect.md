---
title: ID3DX11Effect-Schnittstelle (D3dx11effect. h)
description: Eine ID3DX11Effect-Schnittstelle verwaltet einen Satz von Zustands Objekten, Ressourcen und Shadern zum Implementieren eines renderingeffekts.
ms.assetid: 34429d51-6b45-4a62-bce1-50c4da02edac
keywords:
- ID3DX11Effect-Schnittstelle Direct3D 11
- ID3DX11Effect Interface Direct3D 11, beschrieben
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
ms.openlocfilehash: 51c9b945f09ad0424ecd6b546aefe68bea276ffc
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314453"
---
# <a name="id3dx11effect-interface"></a>ID3DX11Effect-Schnittstelle

Eine **ID3DX11Effect** -Schnittstelle verwaltet einen Satz von Zustands Objekten, Ressourcen und Shadern zum Implementieren eines renderingeffekts.

## <a name="members"></a>Member

Die **ID3DX11Effect** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **ID3DX11Effect** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DX11Effect** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                     | Beschreibung                                                                               |
|:---------------------------------------------------------------------------|:------------------------------------------------------------------------------------------|
| [**Cloneeffect**](id3dx11effect-cloneeffect.md)                           | Erstellt eine Kopie einer Effect-Schnittstelle.<br/>                                         |
| [**Getclassverknüpfung**](id3dx11effect-getclasslinkage.md)                   | Ruft eine Schnittstelle für die Klassen Verknüpfung ab.<br/>                                                |
| [**GetConstantBufferByIndex**](id3dx11effect-getconstantbufferbyindex.md) | Einen konstanten Puffer nach Index erhalten.<br/>                                                |
| [**GetConstantBufferByName**](id3dx11effect-getconstantbufferbyname.md)   | Einen konstanten Puffer anhand des Namens erhalten.<br/>                                                 |
| [**GetDesc**](id3dx11effect-getdesc.md)                                   | Sie erhalten eine Beschreibung des Effekts.<br/>                                                     |
| [**GetDevice**](id3dx11effect-getdevice.md)                               | Holen Sie sich das Gerät, das den Effekt erzeugt hat.<br/>                                        |
| [**Getgroupbyindex**](id3dx11effect-getgroupbyindex.md)                   | Ruft eine Effekt Gruppe nach Index ab.<br/>                                                 |
| [**Getgroupbyname**](id3dx11effect-getgroupbyname.md)                     | Ruft eine Effekt Gruppe nach dem Namen ab.<br/>                                                  |
| [**Gettechniquebyindex**](id3dx11effect-gettechniquebyindex.md)           | Holen Sie sich eine Technik nach Index.<br/>                                                      |
| [**Gettechniquebyname**](id3dx11effect-gettechniquebyname.md)             | Holen Sie sich eine Technik anhand des Namens.<br/>                                                       |
| [**GetVariableByIndex**](id3dx11effect-getvariablebyindex.md)             | Eine Variable nach Index erhalten.<br/>                                                       |
| [**GetVariableByName**](id3dx11effect-getvariablebyname.md)               | Eine Variable anhand ihres Namens erhalten.<br/>                                                        |
| [**Getvariablebysemantic**](id3dx11effect-getvariablebysemantic.md)       | Eine Variable nach Semantik erhalten.<br/>                                                    |
| [**Isoptimiert**](id3dx11effect-isoptimized.md)                           | Testen eines Effekts, um zu ermitteln, ob die reflektionsintemetadaten aus dem Arbeitsspeicher entfernt wurden.<br/> |
| [**IsValid**](id3dx11effect-isvalid.md)                                   | Testen Sie einen Effekt, um festzustellen, ob er eine gültige Syntax enthält.<br/>                             |
| [**Optimieren**](id3dx11effect-optimize.md)                                 | Minimieren Sie den für einen Effekt benötigten Arbeitsspeicher.<br/>                          |



 

## <a name="remarks"></a>Bemerkungen

Ein Effekt wird durch Aufrufen von [**D3DX11CreateEffectFromMemory**](d3dx11createeffectfrommemory.md)erstellt.

Das Effect-System gruppiert die für das Rendering erforderlichen Informationen in einen Effekt, der Folgendes enthält: Zustands Objekte zum Zuweisen von Zustandsänderungen in Gruppen, Ressourcen zum Bereitstellen von Eingabedaten und Speichern von Ausgabedaten sowie Programme, die Steuern, wie das Rendering als Shader ausgeführt wird.

> [!Note]  
> Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit. Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen. Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).

 

> [!Note]
>
> Wenn Sie [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) für ein **ID3DX11Effect** -Objekt aufrufen, um die [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle abzurufen, gibt **QueryInterface** E \_ nointerface zurück. Um dieses Problem zu umgehen, verwenden Sie den folgenden Code:
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
| Header<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Bibliothek<br/> | <dl> <dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt> </dl> |

## <a name="see-also"></a>Weitere Informationen

[Effekte 11-Schnittstellen](d3d11-graphics-reference-effects11-interfaces.md)

[D3DX-Schnittstellen](d3d11-graphics-reference-d3dx11-interfaces.md)
