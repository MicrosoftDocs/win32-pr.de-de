---
title: ID3DX11EffectGroup-Schnittstelle (D3dx11effect. h)
description: Die ID3DX11EffectGroup-Schnittstelle greift auf eine Effekt Gruppe zu. Die Lebensdauer eines ID3DX11EffectGroup-Objekts entspricht der Lebensdauer seines übergeordneten ID3DX11Effect-Objekts.
ms.assetid: f5a35c47-0bac-4559-bd6c-5e8bc7699e10
keywords:
- ID3DX11EffectGroup-Schnittstelle Direct3D 11
- ID3DX11EffectGroup Interface Direct3D 11, beschrieben
topic_type:
- apiref
api_name:
- ID3DX11EffectGroup
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5970506b850d164a4018cd371e19bfab6cd3624
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982281"
---
# <a name="id3dx11effectgroup-interface"></a>ID3DX11EffectGroup-Schnittstelle

Die **ID3DX11EffectGroup** -Schnittstelle greift auf eine Effekt Gruppe zu.

Die Lebensdauer eines **ID3DX11EffectGroup** -Objekts entspricht der Lebensdauer seines übergeordneten [**ID3DX11Effect**](id3dx11effect.md) -Objekts.

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DX11EffectGroup** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                  | BESCHREIBUNG                                                   |
|:------------------------------------------------------------------------|:--------------------------------------------------------------|
| [**Getannotationbyindex**](id3dx11effectgroup-getannotationbyindex.md) | Eine Anmerkung nach Index erhalten.<br/>                        |
| [**Getannotationbyname**](id3dx11effectgroup-getannotationbyname.md)   | Eine Anmerkung anhand des Namens erhalten.<br/>                         |
| [**GetDesc**](id3dx11effectgroup-getdesc.md)                           | Ruft eine Gruppenbeschreibung ab.<br/>                          |
| [**Gettechniquebyindex**](id3dx11effectgroup-gettechniquebyindex.md)   | Holen Sie sich eine Technik nach Index.<br/>                          |
| [**Gettechniquebyname**](id3dx11effectgroup-gettechniquebyname.md)     | Holen Sie sich eine Technik anhand des Namens.<br/>                           |
| [**IsValid**](id3dx11effectgroup-isvalid.md)                           | Testen Sie einen Effekt, um festzustellen, ob er eine gültige Syntax enthält.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Um eine **ID3DX11EffectGroup** -Schnittstelle zu erhalten, müssen Sie eine Methode wie [**ID3DX11Effect:: getgroupbyname**](id3dx11effect-getgroupbyname.md)aufrufen.

> [!Note]  
> Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit. Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen. Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Bibliothek<br/> | <dl> <dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Effekte 11-Schnittstellen](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[D3DX-Schnittstellen](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





