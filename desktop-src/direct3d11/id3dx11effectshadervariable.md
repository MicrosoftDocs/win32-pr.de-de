---
title: ID3DX11EffectShaderVariable-Schnittstelle (D3dx11effect. h)
description: Eine Shader-Variable-Schnittstelle greift auf eine Shader-Variable zu.
ms.assetid: e547a5e9-7b60-4a85-806d-272be55d12e7
keywords:
- ID3DX11EffectShaderVariable-Schnittstelle Direct3D 11
- ID3DX11EffectShaderVariable Interface Direct3D 11, beschrieben
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bcbb011591f715b4bac57dfa34f640ea90278f6b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104995925"
---
# <a name="id3dx11effectshadervariable-interface"></a>ID3DX11EffectShaderVariable-Schnittstelle

Eine Shader-Variable-Schnittstelle greift auf eine Shader-Variable zu.

## <a name="members"></a>Member

Die **ID3DX11EffectShaderVariable** -Schnittstelle erbt von [**ID3DX11EffectVariable**](id3dx11effectvariable.md). **ID3DX11EffectShaderVariable** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DX11EffectShaderVariable** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                                                           | BESCHREIBUNG                                            |
|:-----------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------|
| [**Getcomputeshader**](id3dx11effectshadervariable-getcomputeshader.md)                                         | Einen Compute-Shader erhalten.<br/>                       |
| [**Getdomainshader**](id3dx11effectshadervariable-getdomainshader.md)                                           | Einen Domänen-Shader erhalten.<br/>                        |
| [**Getgeometryshader**](id3dx11effectshadervariable-getgeometryshader.md)                                       | Einen Geometry-Shader erhalten.<br/>                      |
| [**Gethullshader**](id3dx11effectshadervariable-gethullshader.md)                                               | Einen Hull-Shader erhalten.<br/>                          |
| [**GetInputSignatureElementDesc**](id3dx11effectshadervariable-getinputsignatureelementdesc.md)                 | Erhalten Sie eine Beschreibung der Eingabe Signatur.<br/>         |
| [**GetOutputSignatureElementDesc**](id3dx11effectshadervariable-getoutputsignatureelementdesc.md)               | Hier erhalten Sie eine Beschreibung der Ausgabe Signatur.<br/>        |
| [**GetPatchConstantSignatureElementDesc**](id3dx11effectshadervariable-getpatchconstantsignatureelementdesc.md) | Hier erhalten Sie eine Beschreibung für eine patchkonstante Signatur.<br/> |
| [**Getpixelshader**](id3dx11effectshadervariable-getpixelshader.md)                                             | Einen PixelShader erhalten.<br/>                         |
| [**Getshaderdebug**](id3dx11effectshadervariable-getshaderdesc.md)                                               | Eine shaderbeschreibung erhalten.<br/>                   |
| [**Getvertexshader**](id3dx11effectshadervariable-getvertexshader.md)                                           | Einen Vertex-Shader erhalten.<br/>                        |



 

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

[**ID3DX11EffectVariable**](id3dx11effectvariable.md)
</dt> <dt>

[Effekte 11-Schnittstellen](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[D3DX-Schnittstellen](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





