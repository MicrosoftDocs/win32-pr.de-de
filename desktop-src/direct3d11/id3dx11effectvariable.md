---
title: ID3DX11EffectVariable-Schnittstelle (D3dx11effect.h)
description: Die ID3DX11EffectVariable-Schnittstelle ist die Basisklasse für alle Effektvariablen. Die Lebensdauer eines ID3DX11EffectVariable-Objekts entspricht der Lebensdauer des übergeordneten ID3DX11Effect-Objekts.
ms.assetid: 07f1b7d7-c266-49ae-b79a-7a645521df89
keywords:
- ID3DX11EffectVariable-Schnittstelle Direct3D 11
- ID3DX11EffectVariable-Schnittstelle Direct3D 11 , beschrieben
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
ms.openlocfilehash: d3340ba231785edb9446c8578d886fca4a28ecbb09e69230d7f8661a5650afa4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045808"
---
# <a name="id3dx11effectvariable-interface"></a>ID3DX11EffectVariable-Schnittstelle

Die **ID3DX11EffectVariable-Schnittstelle** ist die Basisklasse für alle Effektvariablen.

Die Lebensdauer eines **ID3DX11EffectVariable-Objekts** entspricht der Lebensdauer des übergeordneten [**ID3DX11Effect-Objekts.**](id3dx11effect.md)

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DX11EffectVariable-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                           | Beschreibung                                            |
|:---------------------------------------------------------------------------------|:-------------------------------------------------------|
| [**AsBlend**](id3dx11effectvariable-asblend.md)                                 | Abrufen einer Effektblendvariable.<br/>                |
| [**AsClassInstance**](id3dx11effectvariable-asclassinstance.md)                 | Abrufen einer Klasseninstanzvariablen.<br/>              |
| [**AsConstantBuffer**](id3dx11effectvariable-asconstantbuffer.md)               | Abrufen eines konstanten Puffers.<br/>                      |
| [**AsDepthStencil**](id3dx11effectvariable-asdepthstencil.md)                   | Abrufen einer Tiefenschablonenvariablen.<br/>               |
| [**AsDepthStencilView**](id3dx11effectvariable-asdepthstencilview.md)           | Abrufen einer Tiefenschablonenansichtsvariablen.<br/>          |
| [**AsInterface**](id3dx11effectvariable-asinterface.md)                         | Abrufen einer Schnittstellenvariablen.<br/>                  |
| [**AsMatrix**](id3dx11effectvariable-asmatrix.md)                               | Abrufen einer Matrixvariablen.<br/>                      |
| [**AsRasterizer**](id3dx11effectvariable-asrasterizer.md)                       | Abrufen einer Rasterisierungsvariablen.<br/>                  |
| [**AsRenderTargetView**](id3dx11effectvariable-asrendertargetview.md)           | Abrufen einer Renderzielansichtsvariablen.<br/>          |
| [**AsSampler**](id3dx11effectvariable-assampler.md)                             | Abrufen einer Samplervariablen.<br/>                     |
| [**AsScalar**](id3dx11effectvariable-asscalar.md)                               | Abrufen einer Skalarvariablen.<br/>                      |
| [**AsShader**](id3dx11effectvariable-asshader.md)                               | Abrufen einer Shadervariablen.<br/>                      |
| [**AsShaderResource**](id3dx11effectvariable-asshaderresource.md)               | Abrufen einer Shader-Ressourcenvariablen.<br/>             |
| [**AsString**](id3dx11effectvariable-asstring.md)                               | Abrufen einer Zeichenfolgenvariablen.<br/>                      |
| [**AsUnorderedAccessView**](id3dx11effectvariable-asunorderedaccessview.md)     | Abrufen einer Variablen mit ungeordneten Zugriffsansichten.<br/>      |
| [**AsVector**](id3dx11effectvariable-asvector.md)                               | Abrufen einer Vektorvariablen.<br/>                      |
| [**GetAnnotationByIndex**](id3dx11effectvariable-getannotationbyindex.md)       | Abrufen einer Anmerkung nach Index.<br/>                 |
| [**GetAnnotationByName**](id3dx11effectvariable-getannotationbyname.md)         | Abrufen einer Anmerkung anhand des Namens.<br/>                  |
| [**GetDesc**](id3dx11effectvariable-getdesc.md)                                 | Abrufen einer Beschreibung.<br/>                          |
| [**GetElement**](id3dx11effectvariable-getelement.md)                           | Abrufen eines Arrayelements.<br/>                       |
| [**GetMemberByIndex**](id3dx11effectvariable-getmemberbyindex.md)               | Abrufen eines Strukturmembers nach Index.<br/>            |
| [**GetMemberByName**](id3dx11effectvariable-getmemberbyname.md)                 | Abrufen eines Strukturmembers anhand des Namens.<br/>             |
| [**GetMemberBySemantic**](id3dx11effectvariable-getmemberbysemantic.md)         | Abrufen eines Strukturmembers nach Semantik.<br/>         |
| [**GetParentConstantBuffer**](id3dx11effectvariable-getparentconstantbuffer.md) | Abrufen eines konstanten Puffers.<br/>                      |
| [**GetRawValue**](id3dx11effectvariable-getrawvalue.md)                         | Abrufen von Daten<br/>                                   |
| [**Gettype**](id3dx11effectvariable-gettype.md)                                 | Abrufen von Typinformationen.<br/>                       |
| [**IsValid**](id3dx11effectvariable-isvalid.md)                                 | Vergleichen Sie den Datentyp mit den gespeicherten Daten.<br/> |
| [**SetRawValue**](id3dx11effectvariable-setrawvalue.md)                         | Legen Sie Daten fest.<br/>                                   |



 

## <a name="remarks"></a>Hinweise

> [!Note]  
> Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte zur Verfügung. Sie müssen die Effects 11-Quelle verwenden, um ihre Effekte-Typ-Anwendung zu erstellen. Weitere Informationen zur Verwendung der Quelle Effects 11 finden Sie unter [Unterschiede zwischen Effekten 10 und Effekten 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Bibliothek<br/> | <dl> <dt>N/A (Eine Effects 11-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Effekte 11 Schnittstellen](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[D3DX-Schnittstellen](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





