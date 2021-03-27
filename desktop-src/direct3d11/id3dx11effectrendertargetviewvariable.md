---
title: ID3DX11EffectRenderTargetViewVariable-Schnittstelle (D3dx11effect. h)
description: Eine Renderziel-View-Schnittstelle greift auf ein Renderziel zu.
ms.assetid: 35c4e1da-05a8-4f1c-8730-58e3c90ad213
keywords:
- ID3DX11EffectRenderTargetViewVariable-Schnittstelle Direct3D 11
- ID3DX11EffectRenderTargetViewVariable Interface Direct3D 11, beschrieben
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
ms.openlocfilehash: 5c5b20f83639fd973016bbe263d9d21dae7b295c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982203"
---
# <a name="id3dx11effectrendertargetviewvariable-interface"></a>ID3DX11EffectRenderTargetViewVariable-Schnittstelle

Eine Renderziel-View-Schnittstelle greift auf ein Renderziel zu.

## <a name="members"></a>Member

Die **ID3DX11EffectRenderTargetViewVariable** -Schnittstelle erbt von [**ID3DX11EffectRasterizerVariable**](id3dx11effectvariable.md). **ID3DX11EffectRenderTargetViewVariable** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DX11EffectRenderTargetViewVariable** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                                     | BESCHREIBUNG                                |
|:-------------------------------------------------------------------------------------------|:-------------------------------------------|
| [**GetRenderTarget**](id3dx11effectrendertargetviewvariable-getrendertarget.md)           | Renderziel.<br/>            |
| [**GetRenderTargetArray**](id3dx11effectrendertargetviewvariable-getrendertargetarray.md) | Ein Array von renderzielen erhalten.<br/> |
| [**"Zielort"**](id3dx11effectrendertargetviewvariable-setrendertarget.md)           | Legen Sie ein Renderziel fest.<br/>            |
| [**"Tartrendertargetarray"**](id3dx11effectrendertargetviewvariable-setrendertargetarray.md) | Legen Sie ein Array von Renderingzielen fest.<br/> |



 

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

[**ID3DX11EffectRasterizerVariable**](id3dx11effectvariable.md)
</dt> <dt>

[Effekte 11-Schnittstellen](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[D3DX-Schnittstellen](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





