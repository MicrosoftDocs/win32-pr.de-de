---
title: ID3DX11EffectVariable-Schnittstelle (D3dx11effect. h)
description: Die ID3DX11EffectVariable-Schnittstelle ist die Basisklasse für alle Effekt Variablen. Die Lebensdauer eines ID3DX11EffectVariable-Objekts entspricht der Lebensdauer seines übergeordneten ID3DX11Effect-Objekts.
ms.assetid: 07f1b7d7-c266-49ae-b79a-7a645521df89
keywords:
- ID3DX11EffectVariable-Schnittstelle Direct3D 11
- ID3DX11EffectVariable Interface Direct3D 11, beschrieben
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1df38a12c54776072bb922ffc4cd5bcd0d79776
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762198"
---
# <a name="id3dx11effectvariable-interface"></a>ID3DX11EffectVariable-Schnittstelle

Die **ID3DX11EffectVariable** -Schnittstelle ist die Basisklasse für alle Effekt Variablen.

Die Lebensdauer eines **ID3DX11EffectVariable** -Objekts entspricht der Lebensdauer seines übergeordneten [**ID3DX11Effect**](id3dx11effect.md) -Objekts.

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DX11EffectVariable** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                           | BESCHREIBUNG                                            |
|:---------------------------------------------------------------------------------|:-------------------------------------------------------|
| [**Asblend**](id3dx11effectvariable-asblend.md)                                 | Eine Effect-Blend-Variable erhalten.<br/>                |
| [**Asclassinstance**](id3dx11effectvariable-asclassinstance.md)                 | Eine Klasseninstanz-Variable erhalten.<br/>              |
| [**Asconstantbuffer**](id3dx11effectvariable-asconstantbuffer.md)               | Einen konstanten Puffer erhalten.<br/>                      |
| [**Asdepthstencil**](id3dx11effectvariable-asdepthstencil.md)                   | Eine tiefen Schablone-Variable erhalten.<br/>               |
| [**Asdepthstencilview**](id3dx11effectvariable-asdepthstencilview.md)           | Eine tiefen Schablone-Ansichts Variable erhalten.<br/>          |
| [**Asinterface**](id3dx11effectvariable-asinterface.md)                         | Eine Schnittstellen Variable erhalten.<br/>                  |
| [**Asmatrix**](id3dx11effectvariable-asmatrix.md)                               | Eine Matrix Variable erhalten.<br/>                      |
| [**Asrasterizer**](id3dx11effectvariable-asrasterizer.md)                       | Eine Raster-Variable erhalten.<br/>                  |
| [**Asrendertargetview**](id3dx11effectvariable-asrendertargetview.md)           | Eine "Rendering-Target-View"-Variable erhalten.<br/>          |
| [**Assampler**](id3dx11effectvariable-assampler.md)                             | Eine samplervariable erhalten.<br/>                     |
| [**Asscalar**](id3dx11effectvariable-asscalar.md)                               | Eine skalare Variable erhalten.<br/>                      |
| [**Asshader**](id3dx11effectvariable-asshader.md)                               | Eine shadervariable erhalten.<br/>                      |
| [**Asshaderresource**](id3dx11effectvariable-asshaderresource.md)               | Eine Shader-Resource-Variable erhalten.<br/>             |
| [**AsString**](id3dx11effectvariable-asstring.md)                               | Eine Zeichen folgen Variable erhalten.<br/>                      |
| [**Asunorderedaccessview**](id3dx11effectvariable-asunorderedaccessview.md)     | Abrufen einer Variablen mit ungeordneter Zugriffs Sicht.<br/>      |
| [**Asvector**](id3dx11effectvariable-asvector.md)                               | Eine Vektor Variable erhalten.<br/>                      |
| [**Getannotationbyindex**](id3dx11effectvariable-getannotationbyindex.md)       | Eine Anmerkung nach Index erhalten.<br/>                 |
| [**Getannotationbyname**](id3dx11effectvariable-getannotationbyname.md)         | Eine Anmerkung anhand des Namens erhalten.<br/>                  |
| [**GetDesc**](id3dx11effectvariable-getdesc.md)                                 | Hier erhalten Sie eine Beschreibung.<br/>                          |
| [**GetElement**](id3dx11effectvariable-getelement.md)                           | Ein Array Element erhalten.<br/>                       |
| [**Getmembership byindex**](id3dx11effectvariable-getmemberbyindex.md)               | Einen Strukturmember nach Index erhalten.<br/>            |
| [**Getmembership byname**](id3dx11effectvariable-getmemberbyname.md)                 | Einen Strukturmember anhand des Namens erhalten.<br/>             |
| [**Getmembership bysemantic**](id3dx11effectvariable-getmemberbysemantic.md)         | Einen Strukturmember nach Semantik erhalten.<br/>         |
| [**Getparametenconstantbuffer**](id3dx11effectvariable-getparentconstantbuffer.md) | Einen konstanten Puffer erhalten.<br/>                      |
| [**Getrawvalue**](id3dx11effectvariable-getrawvalue.md)                         | Abrufen von Daten<br/>                                   |
| [**GetType**](id3dx11effectvariable-gettype.md)                                 | Typinformationen erhalten.<br/>                       |
| [**IsValid**](id3dx11effectvariable-isvalid.md)                                 | Vergleichen Sie den Datentyp mit den gespeicherten Daten.<br/> |
| [**"Strawvalue"**](id3dx11effectvariable-setrawvalue.md)                         | Legen Sie Daten fest.<br/>                                   |



 

## <a name="remarks"></a>Bemerkungen

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

 

 





