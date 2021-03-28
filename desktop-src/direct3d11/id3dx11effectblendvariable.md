---
title: ID3DX11EffectBlendVariable-Schnittstelle (D3dx11effect. h)
description: Die Blend-Variable-Schnittstelle greift auf Blend-Status zu.
ms.assetid: 8a6e6e7e-2f1e-4e16-8d28-ffc7f3f018d6
keywords:
- ID3DX11EffectBlendVariable-Schnittstelle Direct3D 11
- ID3DX11EffectBlendVariable Interface Direct3D 11, beschrieben
topic_type:
- apiref
api_name:
- ID3DX11EffectBlendVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57a0a8a3ec0c2a3d92dfc9579fff8b3769dcfc5d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961761"
---
# <a name="id3dx11effectblendvariable-interface"></a>ID3DX11EffectBlendVariable-Schnittstelle

Die Blend-Variable-Schnittstelle greift auf Blend-Status zu.

## <a name="members"></a>Member

Die **ID3DX11EffectBlendVariable** -Schnittstelle erbt von [**ID3DX11EffectVariable**](id3dx11effectvariable.md). **ID3DX11EffectBlendVariable** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DX11EffectBlendVariable** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                    | BESCHREIBUNG                                          |
|:--------------------------------------------------------------------------|:-----------------------------------------------------|
| [**Getbackingstore**](id3dx11effectblendvariable-getbackingstore.md)     | Einen Zeiger auf eine Blend-State-Variable erhalten.<br/>  |
| [**Getblendstate**](id3dx11effectblendvariable-getblendstate.md)         | Einen Zeiger auf eine Blend-State-Schnittstelle erhalten.<br/> |
| [**Setblendstate**](id3dx11effectblendvariable-setblendstate.md)         | Legt den Blend-Status eines Effekts fest.<br/>             |
| [**Undosetblendstate**](id3dx11effectblendvariable-undosetblendstate.md) | Kehrt einen zuvor festgelegten Blend-Status zurück.<br/>     |



 

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

 

 





