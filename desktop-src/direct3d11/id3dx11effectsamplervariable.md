---
title: ID3DX11EffectSamplerVariable-Schnittstelle (D3dx11effect. h)
description: Eine samplerschnittstelle greift auf den samplerstatus
ms.assetid: 8d21f829-2145-45f2-a9b4-2fdc06e0a879
keywords:
- ID3DX11EffectSamplerVariable-Schnittstelle Direct3D 11
- ID3DX11EffectSamplerVariable Interface Direct3D 11, beschrieben
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
ms.openlocfilehash: 7b5019022cea823566611410cd6e8fd5013380b9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104132409"
---
# <a name="id3dx11effectsamplervariable-interface"></a>ID3DX11EffectSamplerVariable-Schnittstelle

Eine samplerschnittstelle greift auf den samplerstatus

## <a name="members"></a>Member

Die **ID3DX11EffectSamplerVariable** -Schnittstelle erbt von [**ID3DX11EffectVariable**](id3dx11effectvariable.md). **ID3DX11EffectSamplerVariable** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DX11EffectSamplerVariable** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                  | BESCHREIBUNG                                                         |
|:------------------------------------------------------------------------|:--------------------------------------------------------------------|
| [**Getbackingstore**](id3dx11effectsamplervariable-getbackingstore.md) | Einen Zeiger auf eine Variable mit dem samplerstatus erhalten.<br/> |
| [**Getsampler**](id3dx11effectsamplervariable-getsampler.md)           | Einen Zeiger auf eine samplerschnittstelle erhalten.<br/>                    |
| [**Setsampler**](id3dx11effectsamplervariable-setsampler.md)           | Festlegen des samplerstatus<br/>                                       |
| [**Undosetsampler**](id3dx11effectsamplervariable-undosetsampler.md)   | Einen zuvor festgelegten samplerstatus zurücksetzen.<br/>                   |



 

## <a name="remarks"></a>Bemerkungen

Eine [**ID3DX11EffectVariable**](id3dx11effectvariable.md) -Schnittstelle wird erstellt, wenn ein Effekt in den Arbeitsspeicher gelesen wird.

Effekt Variablen werden im Sicherungs Speicher im Arbeitsspeicher gespeichert. Wenn eine Technik angewendet wird, werden die Werte im Sicherungs Speicher auf das Gerät kopiert. Sie können eine dieser Methoden verwenden, um den Status zurückzugeben.

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

 

 





