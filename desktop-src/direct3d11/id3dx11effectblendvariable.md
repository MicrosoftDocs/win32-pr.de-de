---
title: ID3DX11EffectBlendVariable-Schnittstelle (D3dx11effect.h)
description: Die Blend-Variable-Schnittstelle greift auf den Blendzustand zu.
ms.assetid: 8a6e6e7e-2f1e-4e16-8d28-ffc7f3f018d6
keywords:
- ID3DX11EffectBlendVariable-Schnittstelle Direct3D 11
- ID3DX11EffectBlendVariable-Schnittstelle Direct3D 11 , beschrieben
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
ms.openlocfilehash: e84bd65c15c40c2e7ce44092baebdef66f17f2de8c1052589a984ff15c9f4b77
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119046458"
---
# <a name="id3dx11effectblendvariable-interface"></a>ID3DX11EffectBlendVariable-Schnittstelle

Die Blend-Variable-Schnittstelle greift auf den Blendzustand zu.

## <a name="members"></a>Member

Die **ID3DX11EffectBlendVariable-Schnittstelle** erbt von [**ID3DX11EffectVariable**](id3dx11effectvariable.md). **ID3DX11EffectBlendVariable** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DX11EffectBlendVariable-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                    | Beschreibung                                          |
|:--------------------------------------------------------------------------|:-----------------------------------------------------|
| [**GetBackingStore**](id3dx11effectblendvariable-getbackingstore.md)     | Abrufen eines Zeigers auf eine Mischungszustandsvariable.<br/>  |
| [**GetBlendState**](id3dx11effectblendvariable-getblendstate.md)         | Abrufen eines Zeigers auf eine Blend-State-Schnittstelle.<br/> |
| [**SetBlendState**](id3dx11effectblendvariable-setblendstate.md)         | Legt den Blendzustand eines Effekts fest.<br/>             |
| [**UndoSetBlendState**](id3dx11effectblendvariable-undosetblendstate.md) | Setzt einen zuvor festgelegten Mischungszustand zurück.<br/>     |



 

## <a name="remarks"></a>Hinweise

Eine [**ID3DX11EffectVariable-Schnittstelle**](id3dx11effectvariable.md) wird erstellt, wenn ein Effekt in den Arbeitsspeicher gelesen wird.

Effektvariablen werden im Speicher im Sicherungsspeicher gespeichert. Wenn eine Technik angewendet wird, werden die Werte im Sicherungsspeicher auf das Gerät kopiert. Sie können eine dieser Methoden verwenden, um den Zustand zurückzugeben.

> [!Note]  
> Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte zur Verfügung. Sie müssen die Effects 11-Quelle verwenden, um ihre Effekte-Typ-Anwendung zu erstellen. Weitere Informationen zur Verwendung der Quelle Effects 11 finden Sie unter [Unterschiede zwischen Effekten 10 und Effekten 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Bibliothek<br/> | <dl> <dt>N/A (Eine Effects 11-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ID3DX11EffectVariable**](id3dx11effectvariable.md)
</dt> <dt>

[Effekte 11 Schnittstellen](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[D3DX-Schnittstellen](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





