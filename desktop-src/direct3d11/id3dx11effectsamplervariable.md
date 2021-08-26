---
title: ID3DX11EffectSamplerVariable-Schnittstelle (D3dx11effect.h)
description: Eine Samplerschnittstelle greifen auf den Samplerzustand zu.
ms.assetid: 8d21f829-2145-45f2-a9b4-2fdc06e0a879
keywords:
- ID3DX11EffectSamplerVariable-Schnittstelle Direct3D 11
- ID3DX11EffectSamplerVariable-Schnittstelle Direct3D 11 , beschrieben
topic_type:
- apiref
api_name:
- ID3DX11EffectSamplerVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0865df924fb3a01e3c10ae015f13b4ec6e06e900dad32ff966d9bdbfed0c75e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952820"
---
# <a name="id3dx11effectsamplervariable-interface"></a>ID3DX11EffectSamplerVariable-Schnittstelle

Eine Samplerschnittstelle greifen auf den Samplerzustand zu.

## <a name="members"></a>Member

Die **ID3DX11EffectSamplerVariable-Schnittstelle** erbt von [**ID3DX11EffectVariable.**](id3dx11effectvariable.md) **ID3DX11EffectSamplerVariable** verfügt auch über diese Membertypen:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DX11EffectSamplerVariable-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                  | BESCHREIBUNG                                                         |
|:------------------------------------------------------------------------|:--------------------------------------------------------------------|
| [**GetBackingStore**](id3dx11effectsamplervariable-getbackingstore.md) | Sie erhalten einen Zeiger auf eine Variable, die den Samplerzustand enthält.<br/> |
| [**GetSampler**](id3dx11effectsamplervariable-getsampler.md)           | Hier erhalten Sie einen Zeiger auf eine Samplerschnittstelle.<br/>                    |
| [**SetSampler**](id3dx11effectsamplervariable-setsampler.md)           | Festlegen des Samplerzustands.<br/>                                       |
| [**UndoSetSampler**](id3dx11effectsamplervariable-undosetsampler.md)   | Setzen Sie einen zuvor festgelegten Samplerzustand zurück.<br/>                   |



 

## <a name="remarks"></a>Hinweise

Eine [**ID3DX11EffectVariable-Schnittstelle**](id3dx11effectvariable.md) wird erstellt, wenn ein Effekt in den Arbeitsspeicher gelesen wird.

Effektvariablen werden im Arbeitsspeicher im Hintergrundspeicher gespeichert. Wenn eine Technik angewendet wird, werden die Werte im Hintergrundspeicher auf das Gerät kopiert. Sie können eine dieser Methoden verwenden, um den Zustand zurück zu geben.

> [!Note]  
> Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit. Sie müssen die Quelle Effects 11 verwenden, um Ihre Effekttypanwendung zu erstellen. Weitere Informationen zur Verwendung der Quelle Effects 11 finden Sie unter [Unterschiede zwischen Effekten 10 und Effekten 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Bibliothek<br/> | <dl> <dt>Nicht verfügbar (eine Effects 11-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ID3DX11EffectVariable**](id3dx11effectvariable.md)
</dt> <dt>

[Effekte 11 Schnittstellen](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[D3DX-Schnittstellen](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





