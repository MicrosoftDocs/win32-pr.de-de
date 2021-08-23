---
title: ID3DX11EffectRenderTargetViewVariable-Schnittstelle (D3dx11effect.h)
description: Eine Renderzielansichtsschnittstelle greifen auf ein Renderziel zu.
ms.assetid: 35c4e1da-05a8-4f1c-8730-58e3c90ad213
keywords:
- ID3DX11EffectRenderTargetViewVariable-Schnittstelle Direct3D 11
- ID3DX11EffectRenderTargetViewVariable-Schnittstelle Direct3D 11 , beschrieben
topic_type:
- apiref
api_name:
- ID3DX11EffectRenderTargetViewVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 645f6253de34c3c4d2306a73f827dca59ae0ce7ce97e33df63edb592b3da651a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045838"
---
# <a name="id3dx11effectrendertargetviewvariable-interface"></a>ID3DX11EffectRenderTargetViewVariable-Schnittstelle

Eine Renderzielansichtsschnittstelle greifen auf ein Renderziel zu.

## <a name="members"></a>Member

Die **ID3DX11EffectRenderTargetViewVariable-Schnittstelle** erbt von [**ID3DX11EffectRasterizerVariable.**](id3dx11effectvariable.md) **ID3DX11EffectRenderTargetViewVariable** verfügt auch über diese Membertypen:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DX11EffectRenderTargetViewVariable-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                                     | Beschreibung                                |
|:-------------------------------------------------------------------------------------------|:-------------------------------------------|
| [**GetRenderTarget**](id3dx11effectrendertargetviewvariable-getrendertarget.md)           | Hier erhalten Sie ein Renderziel.<br/>            |
| [**GetRenderTargetArray**](id3dx11effectrendertargetviewvariable-getrendertargetarray.md) | Hier erhalten Sie ein Array von Renderzielen.<br/> |
| [**SetRenderTarget**](id3dx11effectrendertargetviewvariable-setrendertarget.md)           | Legen Sie ein Renderziel fest.<br/>            |
| [**SetRenderTargetArray**](id3dx11effectrendertargetviewvariable-setrendertargetarray.md) | Legen Sie ein Array von Renderzielen fest.<br/> |



 

## <a name="remarks"></a>Hinweise

> [!Note]  
> Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit. Sie müssen die Quelle Effects 11 verwenden, um Ihre Effekttypanwendung zu erstellen. Weitere Informationen zur Verwendung der Quelle Effects 11 finden Sie unter [Unterschiede zwischen Effekten 10 und Effekten 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Bibliothek<br/> | <dl> <dt>Nicht verfügbar (eine Effects 11-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ID3DX11EffectRasterizerVariable**](id3dx11effectvariable.md)
</dt> <dt>

[Effekte 11 Schnittstellen](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[D3DX-Schnittstellen](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





