---
title: ID3DX11EffectRasterizerVariable-Schnittstelle (D3dx11effect.h)
description: Eine Rasterizer-Variable-Schnittstelle greift auf den Rasterizerzustand zu.
ms.assetid: d039e3c5-c066-4658-bead-92a5d705ed89
keywords:
- ID3DX11EffectRasterizerVariable-Schnittstelle Direct3D 11
- ID3DX11EffectRasterizerVariable-Schnittstelle Direct3D 11 , beschrieben
topic_type:
- apiref
api_name:
- ID3DX11EffectRasterizerVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4653936edc3fd2181f875b3a848e401b8fa24d318a1e48df4fa06e462ae3cf19
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118534186"
---
# <a name="id3dx11effectrasterizervariable-interface"></a>ID3DX11EffectRasterizerVariable-Schnittstelle

Eine Rasterizer-Variable-Schnittstelle greift auf den Rasterizerzustand zu.

## <a name="members"></a>Member

Die **ID3DX11EffectRasterizerVariable-Schnittstelle** erbt von [**ID3DX11EffectVariable**](id3dx11effectvariable.md). **ID3DX11EffectRasterizerVariable** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DX11EffectRasterizerVariable-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                                   | Beschreibung                                                            |
|:-----------------------------------------------------------------------------------------|:-----------------------------------------------------------------------|
| [**GetBackingStore**](id3dx11effectrasterizervariable-getbackingstore.md)               | Abrufen eines Zeigers auf eine Variable, die den Rasteriserzustand enthält.<br/> |
| [**GetRasterizerState**](id3dx11effectrasterizervariable-getrasterizerstate.md)         | Abrufen eines Zeigers auf eine Rasterizerschnittstelle.<br/>                    |
| [**SetRasterizerState**](id3dx11effectrasterizervariable-setrasterizerstate.md)         | Legt den Rasterizerzustand fest.<br/>                                  |
| [**UndoSetRasterizerState**](id3dx11effectrasterizervariable-undosetrasterizerstate.md) | Setzt einen zuvor festgelegten Rasterizerzustand zurück.<br/>                  |



 

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

 

 





