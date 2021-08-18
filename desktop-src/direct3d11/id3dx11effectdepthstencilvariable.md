---
title: ID3DX11EffectDepthStencilVariable-Schnittstelle (D3dx11effect.h)
description: Eine Tiefenschablonenvariablenschnittstelle greift auf den Tiefenschablonenzustand zu.
ms.assetid: 8fb1be19-eed4-4d69-bbbe-94484531eba2
keywords:
- ID3DX11EffectDepthStencilVariable-Schnittstelle Direct3D 11
- ID3DX11EffectDepthStencilVariable-Schnittstelle Direct3D 11 , beschrieben
topic_type:
- apiref
api_name:
- ID3DX11EffectDepthStencilVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d743bfebfa9722261d220800a633bdc8b268a520b883c9fea11f9f7948f7bca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989770"
---
# <a name="id3dx11effectdepthstencilvariable-interface"></a>ID3DX11EffectDepthStencilVariable-Schnittstelle

Eine Tiefenschablonenvariablenschnittstelle greift auf den Tiefenschablonenzustand zu.

## <a name="members"></a>Member

Die **ID3DX11EffectDepthStencilVariable-Schnittstelle** erbt von [**ID3DX11EffectVariable**](id3dx11effectvariable.md). **ID3DX11EffectDepthStencilVariable** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DX11EffectDepthStencilVariable-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                                         | Beschreibung                                                               |
|:-----------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------|
| [**GetBackingStore**](id3dx11effectdepthstencilvariable-getbackingstore.md)                   | Abrufen eines Zeigers auf eine Variable, die den Tiefenschablonenzustand enthält.<br/> |
| [**GetDepthStencilState**](id3dx11effectdepthstencilvariable-getdepthstencilstate.md)         | Abrufen eines Zeigers auf eine Tiefenschablonenschnittstelle.<br/>                    |
| [**SetDepthStencilState**](id3dx11effectdepthstencilvariable-setdepthstencilstate.md)         | Legt den Tiefenschablonenzustand fest.<br/>                                  |
| [**UndoSetDepthStencilState**](id3dx11effectdepthstencilvariable-undosetdepthstencilstate.md) | Setzt einen zuvor festgelegten Tiefenschablonenzustand zurück.<br/>                  |



 

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



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ID3DX11EffectVariable**](id3dx11effectvariable.md)
</dt> <dt>

[Effekte 11 Schnittstellen](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[D3DX-Schnittstellen](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





