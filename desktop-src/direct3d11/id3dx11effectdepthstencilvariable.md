---
title: ID3DX11EffectDepthStencilVariable-Schnittstelle (D3dx11effect. h)
description: Eine tiefen Schablone-Variablen-Schnittstelle greift auf den Status der tiefen Schablone zu.
ms.assetid: 8fb1be19-eed4-4d69-bbbe-94484531eba2
keywords:
- ID3DX11EffectDepthStencilVariable-Schnittstelle Direct3D 11
- ID3DX11EffectDepthStencilVariable Interface Direct3D 11, beschrieben
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
ms.openlocfilehash: 4d7aa520df0c13c81435421d5f605f901a61da6e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961717"
---
# <a name="id3dx11effectdepthstencilvariable-interface"></a>ID3DX11EffectDepthStencilVariable-Schnittstelle

Eine tiefen Schablone-Variablen-Schnittstelle greift auf den Status der tiefen Schablone zu.

## <a name="members"></a>Member

Die **ID3DX11EffectDepthStencilVariable** -Schnittstelle erbt von [**ID3DX11EffectVariable**](id3dx11effectvariable.md). **ID3DX11EffectDepthStencilVariable** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DX11EffectDepthStencilVariable** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                                         | BESCHREIBUNG                                                               |
|:-----------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------|
| [**Getbackingstore**](id3dx11effectdepthstencilvariable-getbackingstore.md)                   | Einen Zeiger auf eine Variable mit dem Status der tiefen Schablone erhalten.<br/> |
| [**Getdepthstencilstate**](id3dx11effectdepthstencilvariable-getdepthstencilstate.md)         | Einen Zeiger auf eine tiefen Schablone-Schnittstelle erhalten.<br/>                    |
| [**Setdepthstencilstate**](id3dx11effectdepthstencilvariable-setdepthstencilstate.md)         | Legt den Status der tiefen Schablone fest.<br/>                                  |
| [**Undosetdepthstencilstate**](id3dx11effectdepthstencilvariable-undosetdepthstencilstate.md) | Stellt einen zuvor festgelegten tiefen Schablone Zustand wieder her.<br/>                  |



 

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

 

 





